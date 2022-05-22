# Adım 1

**İlk önyükleme sektörünüz!**

## Kod
Aşağıdaki kod, bir diskten önyükleme kodunun olası en küçük örneğidir.
```x86asm
; BOOT.ASM
HANG:
	JMP HANG

	TIMES 512-($-$$) DB 0
```

CPU Real Mod'da başlar ve BIOS yukarıdaki kodu `0000:7c00` adresinde yükler.
`TIMES 512-($-$$) DB 0`, NASM'ın 512 baytı sıfırla doldur deme şeklidir.

Sonunda genellikle bir önyükleme imzası (`0xAA55`) bulunur. Bazı BIOS'ların
eski sürümleri, bir diskteki önyükleme sektörünü tanımlamak için bunu arardı.
Kodu eski bir BIOS'ta veya QEMU'da çalıştırmıyorsanız, günümüzde açıkça
gereksizdir. Gerekirse, son satır şöyle değiştirilmelidir:
```x86asm
; BOOT.ASM
HANG:
	JMP HANG

	TIMES 510-($-$$) DB 0 ; artık 2 bayt daha az
	DB 0x55
	DB 0xAA
```

Başlattığınızda ve imleç boş bir ekranda mutlu bir şekilde yanıp söndüğünde, diskin
motoru kapanacak. Bunun nedeni, *interrupt*ların hâlâ üretiliyor olmasıdır. Interruptlar
bayrağını temizlemeyi deneyebilirsiniz:
```x86asm
; BOOT.ASM
CLI
HANG:
	JMP HANG

	TIMES 510-($-$$) DB 0 ; artık 2 bayt daha az
	DB 0x55
	DB 0xAA
```
Motorun kapanmadığını fark edebilirsiniz.

Döngüyü kaldırmak ve sektörü yalnızca sıfırlarla doldurmak genellikle BIOS'un önyüklemede
hata vermesine neden olur. Çoğu makinede "İşletim Sistemi Bulunamadı" yazacaktır.

## Disk görüntüsü oluşturma
Kod NASM ile derlenir ve diskete (eski), diske veya USB'ye kopyalanır. Sonra o diskten
önyükleme yapılır.

### Unix
```sh
nasm BOOT.ASM -f bin -o BOOT.BIN
````

### İkili dosyayı QEMU'da çalıştırma
Disket sürücülü eski bir makineniz yoksa, QEMU ("fda") kullanarak bir makineyi
taklit edebilirsiniz.
```sh
qemu-system-i386 -fda BOOT.BIN
````

Ancak disketleri tamamen unutmanız ve USB'lere odaklanmanız önerilir. Ayrıca kodunuzu
makinenizde test etmekten korkuyorsanız (bu akıllıca olur), QEMU'yu ("hda") kullanabilirsiniz:
```sh
qemu-system-i386 -hda BOOT.BIN
````