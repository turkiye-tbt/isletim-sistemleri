# Başlangıç Hataları
"Kendi işletim sistemini yapma" fikri sizi buraya kadar getirdi demek...
Bu belgeler, girişiminizde size yol gösterici olur!

Bununla birlikte, yeni gelenlerin belirli hatalar yapması veya
konuya neyin dahil olduğu ve yaygın yanılgılara sahip olması oldukça
yaygındır. Bu kötü değildir - birçok kişi bu başlangıç hatalarını
yaptı ve birçoğu gelecekte de yapacak. Bu sayfa, sağlanan bilgileri
incelemeden önce ne hakkında olduğunu bildiğinizden emin
olmanızı sağlar.

- [Burası ne **DEĞİLDİR?**](#burası-ne-değildir)
- [Zor Bir Gerçek](#zor-bir-gerçek)
	- [... hakkında eğitim var mı?](#-hakkında-bir-eğitim-var-mı)
- [Kapsam](#kapsam)
	- [Ticari İşletim Sistemi Geliştirme](#ticari-işletim-sistemi-geliştirme)
	- [Cehaletten Kaçının](#cehaletten-kaçının)
- [Tasarım](#tasarım)
	- [GUI Tasarımı](#gui-tasarımı)
	- [Popülerlik](#popülerlik)
	- [Bellek kullanımı](#bellek-kullanımı)
	- [İşletim Sistemi Öykünmesi](#işletim-sistemi-öykünmesi)

## Burası ne **DEĞİLDİR**?
Burası, kopyalayıp yapıştırabileceğiniz öğreticilerin yanı sıra takıldığınız
zaman soru sorabileceğiniz bir yer gibi görünebilir, **burası öyle bir yer değildir**.
Kendi işletim sisteminizi yazmaya başlamadan önce tamamen kendi ağırlığınızı taşımanızı
ve deneyimli bir geliştirici olmanızı bekliyoruz. Ayrıca, işletim sistemi tasarımı hakkında
bir şeyler okumanızı ve seçtiğiniz platformla ilgili belgeleri incelemenizi bekliyoruz.
Bu Belgeler'in, genel olarak programlama becerilerine yönelik bir rehber ya da,
*kendi işletim sisteminiz için bir tür eksiksiz rehber* olmasını **beklemeyin**.

Burada bulduğunuz şey, sizden önce gelenlerin, teknik belgeleri, mevcut kaynak kodları okuyarak
ve deneme-yanılma yöntemini kullanarak bunları öğrenenlerin geride bıraktığı belgelerdir.

Burada bulabilecekleriniz, yolunuzda size yardımcı olabilecek küçük ipuçları ve yol
işaretleridir, *işletim sistemi geliştirmenin tam bir haritası* değil, olmamalı da.	

Bir yığının ne olduğu veya bir hata ayıklayıcının nasıl kullanılacağı hakkında henüz
bir fikriniz yoksa, bunu size açıklamak için elimizden geleni yapmayacağız. Açıkladığımız
şeylerin konulara genel bir giriş değil, çoğunlukla işletim sistemleriyle ilgili olduklarını
göreceksiniz. Bu bir kusur değil, tasarım gereği. Genel programlama aydınlanması arıyorsanız,
bir işletim sistemi geliştiricisi olmayı arzu etmeden önce [StackOverflow](https://stackoverflow.com)
gibi genel programlama sitelerini ziyaret etmelisiniz.

Bu Belgeler, yeni başlayanlar için bir el kitabı olarak genişletilmeyecektir, çünkü amacı bu değildir.
İnsanlar çekirdek programlamaya dalmaya hazır olduklarını hissettiklerinde ortaya çıkan *ileri düzey*
soruları yanıtlamak içindir.

### Zor Bir Gerçek
**Birkaç dilde ve ortamda uzun yıllara dayanan deneyime sahip deneyimli bir geliştirici
olmayan hiç kimse henüz işletim sistemi geliştirmeyi düşünmemelidir. Assembly dilinde ve/veya
C gibi bir sistem dilinde birkaç yıllık düşük seviyeli kodlamayı içeren on yıllık bir programlama,
konuyu üzerinde çalışacak kadar iyi anlamak için bile gerekli olan asgari miktardır.**

Kendinizin binde bir olduğunuzu düşünüyorsanız, [Dunning-Kriger Etkisi](https://tr.wikipedia.org/wiki/Dunning-Kruger_etkisi)'ni okuyun ve konuyu tekrar düşünün.

Bu Belgeler'e katkıda bulunanların çoğu çok daha erken başladığı doğru olsa da, çoğumuz için bu,
deneyim eksikliğinden kaynaklanan bir hataydı. Bu grubun öncülerinin çoğu, küçük bir işletim
sistemi projesinin bile saf ölçeği ve karmaşıklığından habersizdi, kendilerini neyin içine
soktuklarına dair hiçbir ipucu yoktu.

### ... hakkında bir eğitim var mı?
Bu yer yeni başlayan geliştiricilere hitap etmediğinden, başka hangi yerin anlaşılması
kolay yazılar yazdığı sorusu sıklıkla sorulur. Ancak, mevcut değiller. Zor konular hafif
düzyazılarla anlatılamaz. Resmi belgeleri okumakta sorun yaşıyorsanız, pratik yapmak için
iyi bir zaman olabilir.

## Kapsam
### Ticari İşletim Sistemi Geliştirme
Böyle harika bir işletim sistemi kurmanın sizi zengin edeceğine	inanmayın. Bir şey varsa,
tarih bize göstermiştir ki en iyi işletim sistemleri hiçbir zaman ticari başarı elde edemezken,
neredeyse tamamen tasarım ve ilham eksikliğine sahip olanlar, akıllı iş hamleleri ve doğru yerde,
doğru zamanda olmaları nedeniyle çok büyük başarılar elde ettiler.

### Cehaletten Kaçının
Yeni başlayanlar genellikle "X'i yapmanın *en iyi yolu, en doğru yolu* nedir?"
yerine "X'i yapmanın *en kolay* yolu nedir?" diye sorarlar. Yeni gelen kişi bir şeyi öğrenmek
için zaman ayırmadığı, bunun yerine bir eğitimden kopyalanan daha basit bir yöntemi seçtiği
için bu tehlikelidir. Uzun vadede daha fazla soruna neden olur.

## Tasarım
### GUI Tasarımı
GUI ile ilgili herhangi bir şeyi gerçekten yaptığınız noktaya gelmeniz, sıfırdan başlayarak
muhtemelen birkaç yılınızı alacaktır. Amacınız daha iyi bir işletim sistemi yerine daha
iyi bir görünüm yaratmaksa, işletim sistemi yerine X Pencere Yöneticisi geliştirmeyi düşünebilirsiniz.

### Popülerlik
*İşletim sistemim Windows, MacOS ve Linux'tan daha popüler olacak!*

Bu son derece olası değildir. Bunu başarmak oldukça fazla zaman, para ve bilgi gerektirir.
Herkes işletim sisteminizi indirmeyecek çünkü:
- işletim sisteminin ne olduğunu veya nasıl kurulacağını bilemeyebilirler
- işletim sisteminizin güvenlik riskleri olabilir
- işletim sisteminiz çok az uygulamayı destekliyor olabilir
- işletim sisteminiz tam olarak işlevsel olmayabilir (işlevsiz komut satırı arayüzü veya kötü GUI)

Birkaç kişi sizinkini kullandığı için şanslı olmalısınız! Günümüzün popüler işletim sistemlerinin
popüler olmasının tek nedeni, daha az alternatifin olduğu on yıllar önce mevcut olmaları ve ihtiyaçlara
cevap vermeleridir.

### Bellek kullanımı
*İşletim sistemim için birkaç kilobayttan daha azını kullanmak istiyorum!*

Üzgünüm, bu muhtemelen imkansız. Bu kadar az bellek kullanan bir işletim sistemi neredeyse
kullanılamaz hâle gelecektir. Dosya sistemi sürücülerini, disk sürücülerini, USB sürücülerini vb.
unutun. Küçük bir şey geliştirmek istiyorsanız, işletim sistemi değil basit bir önyükleyici
yapın.

### İşletim Sistemi Öykünmesi
*İşletim sistemim Windows, MacOS ve Linux programlarını çalıştırabilecek!!1*

Üzgünüm ama muhtemelen olmayacak. Tek bir sistemi taklit etmek bile, özellikle Windows
veya MacOS gibi tescilli olduğunda (Linux muhtemelen üç sistemden en kolayıdır.).
[Wine](https://winehq.org), 1993'ten beri geliştirilmekte olmasına ve kullanıcı uzayında yazılmasına
rağmen hala birçok programda sorun yaşıyor.