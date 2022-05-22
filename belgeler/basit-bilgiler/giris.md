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
- [Kabuk nedir?](#kabuk-nedir)
- [GUI nedir?](#gui-nedir)
	- [Masaüstü Ortamı, Pencere Yöneticisi, Widget Kütüphanesi](#masaüstü-ortamı-pencere-yöneticisi-widget-kütüphanesi)

## İşletim sistemi nedir?
*İşletim sistemi,* bir bilgisayar sisteminin ve kaynaklarının çalışmasını
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
Bir *işletim sisteminin çekirdeği*, asla göremeyeceğiniz bir şeydir. Temel olarak
diğer programların yürütülmesini sağlar. Donanım ve yazılımlar tarafından oluşturulan
olayları işler ve kaynaklara erişimi yönetir.

Donanım olay işleyicileri *(event handler / interrupt handler)* örneğin az önce
bastığınız tuşun numarasını alır.

*Sistem çağrıları*, dosyaları açmak, diğer programları başlatmak vb. için kullanıcı
uzayındaki programlar tarafından çağrılır. Her sistem çağrısı işleyicisi, iletilen
argümanların geçerli olup olmadığını kontrol etmeli ve ardından işlemi gerçekleştirmelidir.

Çoğu kullanıcı programı doğrudan sistem çağrılarını çağırmaz, bunun yerine sistem çağrısını çağırma gibi
işleri yapan standart bir kütüphane kullanır. (Örneğin, C fonksiyonu `fopen()` sonunda dosyayı gerçekten açan bir sistem çağrısını çağırır)

## Kabuk nedir?
*Kabuk*, genellikle bir işletim sistemi dağıtımına entegre edilen ve insanlara
arayüz sunan özel bir programdır. Kullanıcılara görünme şekli sistemden sisteme
değişiklik gösterebilir (komut satırı, dosya gezgini vb.), ancak konsept her zaman aynıdır:
- Kullanıcının başlatılacak bir program seçmesine izin verme ve isteğe bağlı olarak ona oturuma özel argümanlar verme
- Dizinlerin içeriğini listelemek, dosyaları taşımak ve kopyalamak gibi yerel depolamadaki işlemlere izin verme.

Bu eylemleri tamamlamak için kabuğun " 'x' dosyasını aç; 'y' dosyasını aç ve eğer yoksa oluştur; X'ten içerik oku; Y'ye yaz; kapat" gibi bir çok sayıda sistem çağrısı yapması gerekebilir.

Modern kabuklar ayrıca aşağıdakiler gibi çeşitli özelliklere sahiptir:
- **Otomatik Tamamlama:** TAB (veya tercih edilen başka bir tuş) tuşuna basıldığında,
kullanıcının yazdığı sözcük geçerli bir kabuk komutu, dosya, dizine veya başka bir şeye
tamamlanır. Otomatik tamamlama tuşuna birden çok basmak, diğer tamamlama olasılıkları
arasında geçiş yapar.
- **Karakter Ekleme:** Kullanıcı, yön tuşlarını kullanarak girdiği şeyde hareket edebilir.
Bir cümlenin ortasına yeni karakterler yazabilir.
- **Kabuk Geçmişi:** Yukarı ve aşağı ok tuşlarını kullanarak kullanıcı önceki girdilerde
gezinebilir.
- **Kaydırma:** Konsolun yüksekliğinden daha fazla satır olduğunda, çıktı bir arabelleğe
kaydedilir ve kullanıcının konsolda yukarı ve aşağı kaydırmasına izin verilir.
- **Betik Oluşturma:** Bazı kabukların özel betik dilleri vardır. Betik dillerine örnek
olarak Bash veya DOS batch verilebilir.

## GUI nedir?
Grafiksel Kullanıcı Arayüzü, herhangi bir işletim sisteminin en görünür kısmıdır.
Rolü basit bir çizim kütüphanesinin ötesine geçer; ayrıca şunları yapabilir:
- Kullanıcı girdi olaylarını (klavye, fare vb.) yakalama ve bunları uygun nesneye gönderme.
- Ekranın hangi bölümlerinin yeniden çizilmesi gerektiğini belirleyerek neyin ekranda nerede
gösterileceğine ilişkin dahili bilgileri güncelleme.
- Gerekli kısımları yeniden çizerek görünen ekran içeriğini güncelleme.
- Bunları doğal, sezgisel ve kullanıcıya duyarlı bir şekilde yapma.

### Masaüstü Ortamı, Pencere Yöneticisi, Widget Kütüphanesi
Bir KDE veya Windows oturumuna başladığınızda, bu bir m*asaüstü ortamı*dır,
yani tüm alt düzey işlevler için ortam sağlayan bir grafik kabuk.

Sistemin çalışan çeşitli programların pencerelerini, yeniden
boyutlandırma/kapama araçlarını, pencere kenarlıklarını, kaydırma
çubuklarını vb. düzenlemekten sorumlu kısmı *Pencere Yöneticisi*'dir.

Son olarak elemanların çizimini, belgelerin ekranda gösterilmesini vb.
sağlayan alt sistemimiz var; buna genellikle widget kütüphanesi denir
Ancak, widget kütüphanelerine genellikle bildirimsel diller biçiminde
alternatifler vardır (örneğin, Qt'nin QML'si, Mozilla'nın XULU'u)

## Neden bir işletim sistemi geliştiriyorsunuz?
İnsanların işletim sistemi geliştirmeyi seçmelerinin çeşitli nedenleri vardır.
Her bireysel geliştiricinin kendine ait olabilir, ancak bazı nedenler 
geliştiriciler arasında ortaktır:
- **Makine üzerinde tam kontrole sahip olmak:** Bir uygulama veya başka bir kullanıcı uzayı programı geliştirirken, geliştirici başkaları tarafından yazılan kodu dikkate almalıdır: işletim sistemi, kütüphaneler, diğer programlar, vb. Bir makinede çalışan tek kodun kendinize ait olması kesinlikle güzel bir duygudur!
- **Araştırma:** Oldukça az sayıda işletim sistemi proje ödevi veya araştırma projesi olarak başlatılır. Araştırma projeleri genellikle mevcut işletim sistemlerini geliştirmek için yapılır. Ayrıca başlangıç seviyesindeki yaygın bir hata, bir işletim sistemini sıfırdan yazmak için gereken süreyi hafife almaktır.
- **Mevcut işletim sistemlerini değiştirmek için:** Belki de geliştiricinin istediği belirli bir özelliğe sahip değillerdir. Belki de genellikle berbattırlar (Linux bloattır, Windows kararsızdır, vb.).
- **Çünkü eğlenceli:** Düşük seviyeli programlama eğlenceli ve heyecan verici bir iştir, çünkü her şeyi kendinizin yapması gerekir. Bu daha zor görünebilir, ancak aynı nedenlerle daha da eğlencelidir. Her şeyin nasıl çalıştığını ve programınızın en içteki işleyişini biliyorsunuz.