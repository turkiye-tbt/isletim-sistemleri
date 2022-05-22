# Gereken Tecrübe
**Bu belgeyi atlayabileceğinizi düşünüyorsanız, muhtemelen tam sizin için!**

İşletim sistemi yazmak *yeni başlayanların* işi değildir. Aslında, bir işletim
sistemi yazmak genellikle en zor programlama görevi olarak kabul edilir. Böyle
bir projeyi düşünmeden önce bile ortalamanın üzerinde programlama becerilerine
ihtiyacınız olacak.

**Bilmeniz gereken bazı şeyler şunlardır:**
- **Temel Bilgisayar Bilimi:** Onaltılık ve ikili gösterimin yanı sıra veri yapıları,
bunların oluşturulması ve işlenmesi, arama ve sıralama algoritmaları, soyut programlama
kavramları vb. gibi benzer temel bilgileri yakından tanımanız gerekir.
- **Dil ve Kelime Bilgisi:** Teknik terimlere hakim olmanız gerekir. Yanlış terimler
kullanmak size yardım etmek isteyen kişilerin kafasını karıştıracaktır.
- **Dil ve Kelime Bilgisi, bölüm 2:** Bu sitede yer alan örneklerin ve kod parçacıklarının çoğu C (veya C++) ile yazılmıştır. Başka bir dil kullanmayı seçseniz bile, C programlanın ortak dilidir ve hakkında fikir sahibi olmanız gerekir.
- **Assembly:** Düşük seviyeli dil Assembly hakkında bilgi sahibi olmalısınız. İşletim sisteminizin çoğunu daha yüksek seviyeli bir dilde yazmayı planlıyor olsanız bile Assembly'ye kesinlikle ihtiyacınız olacak!
- **Programlama deneyimi:** Bir işletim sistemi projesiyle programlama hakkında deneyim kazanmak kötü bir fikir olarak kabul edilir. Yalnızca geliştireceğiniz dili değil, aynı zamanda sürüm kontrolü, hata ayıklama vb. konulara da aşina olmalısınız. Kısacası, işletim sistemi geliştirmeyi denemeden önce bu dilde epeyce kullanıcı uzayı programını başarıyla yazmış olmalısınız.
- **Programlama pratikleri:** Hem kod hem de kullanıcı belgelerini nasıl yazacağınızı bilmeli ve proje tamamen kişisel kullanımınız için olsa bile kodunuzun ve tasarımınızın tüm yönlerini dikkatlice belgelemeye hazır olmalısınız. Ayrıca, site dişi bir depo (ör. GitHub, GitLab, Heroku) kurma ve kullanma dahil uygun *Kod Yönetimi*
uygulamalarını öğrenmeli ve kullanmalısınız. Eğer kullanırsanız, gelecekte sizi büyük bir beladan kurtaracaktır.
- **UNIX deneyimi:** İşletim sistemi geliştirmede kullanılan araçların çoğunun Unix için geliştirildiğini ve daha sonra Windows'a taşındığını yakında fark edeceksiniz. Linux çekirdeği genellikle işlerin nasıl yapılabileceğine dair bir referans veya örnek olarak kullanılır ve hobi işletim sistemlerinin çoğu Unix ile biraz benzerlik gösterir. Unix komut satırında (tercihen Bash) deneyim sahibi olmak çok önemli bir gerekliliktir. Henüz kullanmadıysanız, bir süreliğine Linux veya BSD kullanın.
- **Araç Zinciri:** Derleyicinizin, bağlayıcınızın ve make yardımcı programınızın ayrıntılarını bilmelisiniz. Uyarıların ve hataların ne anlama geldiğini bilmelisiniz. Kullandığınız araçların belgelerine sahip olmanız ve topluluğa sormadan önce bunlara başvurmanız gerekir.
- **Emülatörler ve Sanallaştırıcılar:** Bochs, VirtualBox, QEMU gibi araçlara aşinalık, geliştirmede makul bir ilerlemeye sahip olmanın anahtarıdır. Bu araçlar, gerçek donanımınız ve test sisteminiz arasında bir arabellek sağlar. Bunlar İS (işletim sistemi) geliştirmenin özel amacı için öğrenilebilirken, bir İS projesine başlamadan önce bunların ne olduğunun ve nereden edinileceğinin kesinlikle farkında olmak isteyeceksiniz.
- **Yürütülebilir Biçimler:** Çekirdek uzayı programlamanın, uygulama geliştirme için bilinmeyen birçok ek gereksinimi vardır. Yürütülebilir ikili dosyaları ayrıştırabilmek bunlardan biridir (işletim sisteminizin uygulamaları yüklemesini ve yürütmesini istiyorsunuz, değil mi?). 