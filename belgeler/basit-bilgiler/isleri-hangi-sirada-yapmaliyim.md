# İşleri Hangi Sırada Yapmalıyım?
Bir önyükleyici, ardından bir çekirdek yazabilir ve oradan başlayabilirsiniz.
Önyükleyiciyi atlayabilir ve GRUB gibi hazır bir önyükleyici kullanabilirsiniz
(kendi önyükleyicinizi geliştirmenin değerli bir deneyim mi yoksa zaman kaybı mı
olduğu tartışmaya açıktır). Muhtemelen işleri yapmanın doğru ya da yanlış bir
yolu yoktur.

## Başlangıç için
1. Ekranda karakterleri ve tamsayıları (hem ondalık hem de onaltılık) yazdırmak
kesinlikle bir zorunluluktur. Bu, hata ayıklamanın en temel yollarından biridir
ve hemen hemen hepimiz sürüm 0.0.1'de bir `kprint()` veya `kout()` oluşturduk.
2. Seri portlarına çıktı almak size çok fazla hata ayıklama süresi kazandıracaktır.
Kaydırma *(scrolling)* nedeniyle bilgi kaybetmekten korkmanıza gerek yok. İşletim
sisteminizi bir konsoldan test edebilecek, ilginç hata ayıklama mesajlarını
filtreleyebilecek ve bazı testleri otomatikleştirebileceksiniz.
3. Registerların içeriğini (ve belki de hatanın adresini) boşaltabilen, çalışan
ve güvenilir bir interrupt/exception işleme sistemine sahip olmak çok
faydalı olacaktır.
4. Bellek haritasını planlayın (sanal ve fiziksel): verilerin nerede olmasını
istediğinize karar verin
5. Yığın (heap): Çalışma zamanında (`malloc` ve `free`) bellek ayırma olmadan
ilerlemek neredeyse imkansızdır. En kısa sürede hayata geçirilmelidir.

Bu adımlar tamamlandıktan sonra, bir dosya sisteminiz, çoklu süreç veya
modül yükleme olmadan bile önce GUI'ye sahip olmaya karar vermek tamemen
size kalmış. Neyin neye bağlı olabileceğini belirlemeye çalışın ve
en az bağımlı olanı ilk geliştirmeye çalışın.

Örneğin, GUI, bitmap'leri ve kaynakları yüklemek için dosya sistemine bağlı
olabilir, ancak ilk GUI'nizde mutlaka bitmap'lere ihtiyacınız yoktur.