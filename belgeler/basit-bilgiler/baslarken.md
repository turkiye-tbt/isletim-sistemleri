# Başlarken
Her şeyden önce, bir işletim sistemi geliştirmek muhtemelen bir bilgisayarda
yapabileceğiniz en zorlu şeylerden biridir. Bir işletim sistemi oluşturmak,
bilgisayar bilimi içindeki çeşitli karmaşık alanlar hakkında çok fazla bilgi
gerektirir. Donanımın nasıl çalıştığını anlamanız ve karmaşık Assembly dilinin
yanı sıra daha yüksek bir dili (C, C++ veya Pascal gibi) okuyup yazabilmeniz
gerekir. Cesaretin kırıldı mı? Korkma! Çünkü tüm bunlar işletim sistemi
programlamayı eğlenceli kılan şeylerdir.

Sonunda, saatlerce uğraştıktan sonra sorunu çözdüğünüzdeki başarı hissi gibisi yoktur.

Bir işletim sistemi oluştururken izlemeniz gereken mutlak bir yol yoktur.
İlk sisteminizi kurup çalıştırdıktan sonra, bir sonraki adımda gitmek
istediğiniz yolu seçersiniz. İşletim sisteminiz tam olarak budur - sizindir.
Tüm kontrol sizde ve sınır gökyüzü!

## Zor Bir Gerçek
Gerçek şu ki, işletim sistemi geliştirme gerçekten benzersizdir, çünkü çok
fazla sabır ve dikkatli kod tasarımı gerektirir.

Önümüzdeki zorlu çalışma konusunda açıkça uyarıldınız, ancak hâlâ ilgileniyorsanız,
işletim sistemi programcısı alanına ilerleyebilirsiniz. Ara sıra kafa karışıklığı,
cesaret kırıklığı ve bazılarımız için... geçici sinir nöbetlerine kendinizi hazırlayın.
Zaman içinde ve yeterli özveriyle, kendinizi çalışan bir işletim sistemine katkıda
bulunan elit azınlığın arasında bulacaksınız. Yol boyunca cesaretiniz kırılırsa,
bu belgelerle kendinizi yenileyin. Umarım ilk etapta neden böyle çılgın bir yolculuğa
başladığınızı size hatırlatır.

Bu aşamada [Başlangıç Hataları](baslangic-hatalari.md) sayfasını da okumakta fayda var.

## Sorumluluk
İnsanlar, bilgisayar sistemlerinin bu günlerde çok hızlı olduğunu ve etkisini görmeyeceğimizi
belirterek, verimsiz yazılımlar yazmanın uygun olduğunu iddia etme eğilimindedir. Bu tür bir
zihniyet, işletim sistemi tasarımında tehlikelidir. Basit bir uygulama yaparken özensiz
kod yazmak iyi olabilir, ancak saniyede binlerce kez çağrılabilecek kritik bir kod söz konusu
olduğunda, tüm ek yükü kaldırmanız gerekir. İşletim sistemi, bilgisayarı mümkün olduğunca
az karmaşıklık ve ek yük ile çalışan uygulamalar için temel bir kaynak olarak sağlamalıdır.

## Gereken Tecrübe
Ana belge: [Gereken Tecrübe](gereken-tecrube.md)

**Bu belgeyi atlayabileceğinizi düşünüyorsanız, muhtemelen tam sizin için!**

## Geliştirme ortamınızı seçme
Yeni sisteminizi geliştirmek için bir ortama ihtiyacınız var. En popüleri GNU/Linux'tur.

- **Binutils:** Nesne dosyalarının işlenmesi için temel araçlar.
- **GCC:** GNU Derleyici Koleksiyonu. GCC derleyicisi C, C++, Fortran ve Ada gibi derleyiciler içerir.
- **Make:** Büyük bir projeye sahip olduğunuzda derleme ve oluşturma sürecini otomatikleştirmek için oldukça kullanışlı bir araç.
- **Assembler:** Örneğin NASM veya GAS. Bu, hedef CPU mimarinize bağlı olarak değişebilir.