# Giriş
İşletim Sistemi geliştirmeye hoş geldiniz!

Bu alanda herkes başarılı olamaz, çoğu işletim sistemi geliştirme
"Merhaba Dünya"yı bile geçemez, ancak belki daha ileri gidip bir
sonraki Linux'u yaratacaksınız?

Hedefleriniz ne olursa olsun, işletim sistemi geliştirme programlamanın
en büyük zirvesidir. Ama yalnız değilsin. Bu wiki tamamen işletim sistemi
geliştirmeye adanmıştır. Bu sadece harika programlama becerileri ile ilgili
değil, aynı zamanda topluluk ve arkadaşlıklar geliştirmekle de ilgilidir.

Bol şanslar!

- [İşletim sistemi nedir?](#işletim-sistemi-nedir)
- [Çekirdek nedir?](#çekirdek-nedir)

## İşletim sistemi nedir?
İşletim sistemi, bir bilgisayar sisteminin ve kaynaklarının çalışmasını
kontrol eden bir yazılımdır. Diğer şeylerin yanı sıra, tüm işletim
sistemlerinde ortak olan çok önemli bir kriter vardır:
- Standartlaştırılmış (donanımdan bağımsız) giriş / çıkış arayüzü sağlayan kullanıcı programlarını yükleyebilir ve yürütebilirler.

İşletim sistemlerinin başlıca işlevleri şunları içerebilir:
- Bellek ve diğer sistem kaynaklarını yönetme.
- Güvenlik ve erişim politikaları uygulamak.
- Süreçleri zamanlama ve iş parçacıkları.
- Kullanıcı programlarını dinamik olarak başlatma ve kapatma.
- Temel bir kullanıcı arayüzü ve uygulama geliştiricileri için arabirim sağlama.

Tüm işletim sistemleri bu işlevlerin tümünü sağlamaz. MS-DOS gibi tek görevli sistemler
süreçleri zamanlamazken, bazıları bir kullanıcı arayüzüne sahip olmayabilir veya
sadece belirlenen kullanıcı programları ile çalışabilir.

Bir işletim sistemi şu **değildir:**
- Bilgisayar donanımı.
- Web tarayıcısı, oyun gibi belirli bir uygulama.
- Bir dizi yardımcı program (GNU araçları gibi).
- Bir geliştirme ortamı.
- Bir Grafiksel Kullanıcı Arayüzü (birçok modern işletim sistemi, işletim sisteminin bir parçası olarak bir GUI içerir).

Çoğu işletim sistemi bu tür araçlarla dağıtılırken, kendileri işletim sisteminin
gerekli bir parçası değildir. Linux gibi bazı işletim sistemleri, farklı uygulama
ve yardımcı programlara sahip olabilen ve sistemin bazı yönlerini farklı şekilde
düzenleyebilen, dağıtım adı verilen birkaç farklı paketlenmiş biçimde gelebilir.
Bununla birlikte, hepsi aynı temel işletim sisteminin sürümleridir ve ayrı
işletim sistemi olarak düşünülmemelidir.

## Çekirdek nedir?
Bir işletim sisteminin çekirdeği, asla göremeyeceğiniz bir şeydir. Temel olarak
diğer programların yürütülmesini sağlar. Donanım ve yazılımlar tarafından oluşturulan
olayları işler ve kaynaklara erişimi yönetir.

Donanım olay işleyicileri *(event handler / interrupt handler)* örneğin az önce
bastığınız tuşun numarasını alır.

*Sistem çağrıları*, dosyaları açmak, diğer programları başlatmak vb. için kullanıcı
uzayındaki programlar tarafından çağrılır. Her sistem çağrısı işleyicisi, iletilen
argümanların geçerli olup olmadığını kontrol etmeli ve ardından işlemi gerçekleştirmelidir.

Çoğu kullanıcı programı doğrudan sistem çağrılarını çağırmaz, bunun yerine sistem çağrısını çağırma gibi
işleri yapan standart bir kütüphane kullanır. (Örneğin, C fonksiyonu `fopen()` sonunda dosyayı gerçekten açan bir sistem çağrısını çağırır)