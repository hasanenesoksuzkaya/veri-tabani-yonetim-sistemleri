1-) Geleneksel Dosyalama Sistemlerinin Çalışma Şeklini Açıklayarak Bildiğiniz Programlama Dili İle TXT Dosyadan Veri Okuyan Ve Yazan Bir Program Geliştiriniz ?

Geleneksel Dosyalama Sistemlerinin Çalışma Şekli :

Geleneksel dosyalama sistemleri, verilerin düzenli bir şekilde saklanması ve erişilmesi için kullanılan yöntemlerdir.

Bu sistemler genellikle aşağıdaki temel bileşenlerden oluşur :

1. Dosya Yapısı : Dosyalar, belirli bir yapıda düzenlenir. Bu yapılar genellikle hiyerarşik bir düzende, klasörler ve alt klasörler şeklinde organize edilir. Her dosya, bir isim ve uzantı ile tanımlanır.
2. Veri Erişimi : Kullanıcılar, dosyalara erişmek için dosya yollarını kullanır. Örneğin, C:\Klasör\Dosya.txt gibi bir yol, belirli bir dosyaya ulaşmak için kullanılır.
3. Dosya Yönetimi : Dosyaların oluşturulması, silinmesi, taşınması ve kopyalanması gibi işlemler, dosya yönetim sistemleri tarafından gerçekleştirilir. Bu işlemler genellikle bir grafik kullanıcı arayüzü (GUI) veya komut satırı arayüzü (CLI) aracılığıyla yapılır.
4. Veri Güvenliği : Geleneksel dosyalama sistemleri, dosyaların güvenliğini sağlamak için çeşitli yöntemler kullanır. Bu yöntemler arasında dosya izinleri, şifreleme ve yedekleme işlemleri bulunur.
5. Performans : Dosya sistemleri, verilerin hızlı bir şekilde erişilmesini sağlamak için optimize edilmiştir. Bu, dosya sisteminin yapısına ve kullanılan depolama aygıtına bağlıdır.
Geleneksel dosyalama sistemleri, genellikle yerel bilgisayarlarda veya sunucularda kullanılır ve verilerin düzenli bir şekilde saklanmasını sağlar. Ancak, bulut tabanlı dosya sistemleri ve veritabanları gibi daha modern çözümler, daha fazla esneklik ve erişilebilirlik sunmaktadır.

TXT Dosyadan Veri Okuyan Ve Yazan Program :

Şematik Kısım :

![image](https://github.com/user-attachments/assets/1dbd6299-151e-42b4-9642-9249eb11710f)

Kod Kısmı :

![image](https://github.com/user-attachments/assets/f4055423-68f2-4052-8817-1740115b0428)

Bu kod, belirtilen veri.txt dosyasından veri okur ve kullanıcıdan alınan yeni veriyi dosyaya ekler.

1.Çıktı :

![image](https://github.com/user-attachments/assets/6a244d47-5fb5-4aaa-8d07-b8118f3f035e)

2.Çıktı :

![image](https://github.com/user-attachments/assets/9d6e386b-4021-40f1-acfe-ea20d4f2ace4)

veri.txt Dosyasının İçeriği :

![image](https://github.com/user-attachments/assets/6e8ba86d-b711-4f38-b74f-4cc82f9d1e63)

2-) Geleneksel Dosyalama Sistemleri İle Veri Tabanı Yönetim Sistemlerinin Benzerlikleri Ve Farklılıkları Nelerdir ?

Geleneksel dosyalama sistemleri ile veri tabanı yönetim sistemleri (VTYS) arasında bazı benzerlikler ve farklılıklar bulunmaktadır.

Benzerlikler:

1. Veri Saklama : Her iki sistem de verileri saklamak için kullanılır. Dosyalama sistemleri dosyaları, VTYS ise tabloları kullanarak verileri depolar.
2. Veri Erişimi : Her iki sistem de kullanıcılara verilere erişim sağlar. Kullanıcılar dosyalara veya veritabanı sorgularına erişebilir.
3. Veri Yönetimi : Her iki sistem de verilerin yönetimi ile ilgilidir. Dosyalama sistemleri dosyaların düzenlenmesi, VTYS ise verilerin düzenlenmesi ve ilişkilerin yönetilmesi ile ilgilenir.
   
Farklılıklar:

1. Veri Yapısı : Geleneksel dosyalama sistemleri genellikle düz dosya yapısına sahiptir. Veri tabanı yönetim sistemleri ise ilişkisel veya nesne yönelimli yapılar kullanarak daha karmaşık veri ilişkileri sunar.
2. Veri Bütünlüğü : VTYS, veri bütünlüğünü sağlamak için çeşitli kısıtlamalar ve kurallar sunar. Geleneksel dosyalama sistemlerinde bu tür bir kontrol genellikle yoktur.
3. Erişim Hızı ve Performans : VTYS, büyük veri setleri üzerinde daha hızlı sorgulama ve erişim sağlar. Geleneksel dosyalama sistemleri, büyük veri setlerinde performans sorunları yaşayabilir.
Veri Güvenliği : VTYS, kullanıcı yetkilendirmesi ve veri şifreleme gibi güvenlik özellikleri sunar. Geleneksel dosyalama sistemlerinde bu tür güvenlik önlemleri genellikle sınırlıdır.
5. Veri Yedekleme ve Kurtarma : VTYS, veri yedekleme ve kurtarma işlemlerini otomatikleştirebilir. Geleneksel dosyalama sistemlerinde bu işlemler genellikle manuel olarak yapılır.
Bu benzerlikler ve farklılıklar, hangi sistemin kullanılacağına karar verirken dikkate alınması gereken önemli unsurlardır.

3-)VTYS nin Geleneksel Sisteme Göre Üstün Özellikleri Nelerdir ?

Veri Tabanı Yönetim Sistemleri (VTYS), geleneksel dosyalama sistemlerine göre birçok üstün özellik sunar. İşte bu üstün özelliklerden bazıları :

1. Veri Bütünlüğü ve Tutarlılığı : VTYS, veri bütünlüğünü sağlamak için çeşitli kısıtlamalar (örneğin, birincil anahtar, yabancı anahtar) ve kurallar sunar. Bu, verilerin tutarlı ve hatasız olmasını sağlar.
2. Veri Erişimi ve Sorgulama : VTYS, SQL gibi güçlü sorgulama dilleri kullanarak veriye hızlı ve etkili bir şekilde erişim sağlar. Kullanıcılar karmaşık sorgular yazarak verileri kolayca filtreleyebilir ve analiz edebilir.
3. Veri Güvenliği : VTYS, kullanıcı yetkilendirmesi ve veri şifreleme gibi güvenlik özellikleri sunar. Bu, verilerin yetkisiz erişimden korunmasını sağlar.
4. Veri Yönetimi ve Organizasyonu : VTYS, verileri tablolar halinde düzenler ve ilişkisel yapılar kullanarak veri yönetimini kolaylaştırır. Bu, veri ilişkilerini daha iyi anlamayı ve yönetmeyi sağlar.
5. Yedekleme ve Kurtarma : VTYS, veri yedekleme ve kurtarma işlemlerini otomatikleştirebilir. Bu, veri kaybı riskini azaltır ve sistemin güvenilirliğini artırır.
6. Çok Kullanıcılı Erişim : VTYS, birden fazla kullanıcının aynı anda verilere erişmesine ve işlem yapmasına olanak tanır. Bu, işbirliği ve veri paylaşımını kolaylaştırır.
7. Veri Paylaşımı ve Dağıtımı : VTYS, verilerin farklı kullanıcılar ve uygulamalar arasında kolayca paylaşılmasını sağlar. Bu, veri entegrasyonunu ve iş süreçlerini optimize eder.
8. Performans ve Ölçeklenebilirlik : VTYS, büyük veri setleri üzerinde daha iyi performans sunar ve gerektiğinde ölçeklenebilir. Bu, büyüyen veri ihtiyaçlarına yanıt vermeyi kolaylaştırır.
9. Veri Analizi ve Raporlama : VTYS, veri analizi ve raporlama için çeşitli araçlar ve özellikler sunar. Bu, işletmelerin verilerden daha fazla değer elde etmesine yardımcı olur.

Bu özellikler, VTYS'nin geleneksel dosyalama sistemlerine göre daha etkili ve verimli bir veri yönetim çözümü sunmasını sağlar.

4-)Veri Tabanının Görevini Açıklayarak Kullanıldığı Alanlara Örnek Veriniz ?

Veri tabanının temel görevi, verileri düzenli bir şekilde saklamak, yönetmek ve bu verilere hızlı ve güvenli bir şekilde erişim sağlamaktır.
Veri tabanları, verilerin bütünlüğünü, tutarlılığını ve güvenliğini sağlamak için çeşitli mekanizmalar sunar. Ayrıca, kullanıcıların verileri sorgulamasına, analiz etmesine ve raporlamasına olanak tanır.
Veri tabanları, finans sektöründe bankalar ve finansal kuruluşlar tarafından müşteri bilgilerini, hesap hareketlerini ve kredi bilgilerini saklamak için kullanılır.
E-ticaret alanında online mağazalar, ürün bilgilerini, müşteri siparişlerini ve envanter durumunu yönetmek için veri tabanlarından yararlanır.
Sağlık sektöründe hastaneler ve klinikler, hasta kayıtlarını, tedavi geçmişlerini ve laboratuvar sonuçlarını saklamak için veri tabanları kullanır. 
Eğitim kurumları, öğrenci kayıtlarını, ders programlarını ve notları yönetmek amacıyla veri tabanlarından faydalanır. 
Telekomünikasyon şirketleri, müşteri bilgilerini, fatura verilerini ve çağrı kayıtlarını saklamak için veri tabanları kullanırken, 
sosyal medya platformları kullanıcı profillerini, paylaşımları ve etkileşimleri yönetmek için veri tabanlarına başvurur. 
Hava yolu şirketleri de uçuş bilgilerini, rezervasyonları ve müşteri bilgilerini saklamak için veri tabanlarından yararlanır.
Ve bunlar gibi birçok örnek verilebilir.

5-)Tablo Satır Ve Sütun Kavramlarını Açıklayınız ?

Veri tabanı yönetim sistemlerinde (VTYS), tablo, verilerin düzenli bir şekilde saklandığı temel yapıdır. Tablo, satır ve sütunlardan oluşur.
Tablo : Belirli bir veri kümesini temsil eden bir yapıdır. Her tablo, belirli bir konu veya nesne hakkında bilgi tutar. Örneğin, bir "Müşteriler" tablosu, müşteri bilgilerini içerebilir.
Sütun : tablodaki verilerin belirli bir özelliğini temsil eder. Her sütun, belirli bir veri türüne sahiptir (örneğin, metin, sayı, tarih). Sütunlar, tablodaki her bir kaydın (satırın) belirli bir özelliğini tanımlar. 
Örneğin, "Müşteri Adı", "Müşteri ID", "E-posta" gibi sütunlar olabilir.
Satır : tablodaki bir kaydı temsil eder. Her satır, tablodaki sütunlarda tanımlanan özelliklere karşılık gelen verileri içerir. 
Örneğin, bir müşteri kaydı, "Müşteri ID", "Müşteri Adı" ve "E-posta" sütunlarına karşılık gelen bilgileri içeren bir satırdır.

6-)Birincil Anahtar Ve Yabancıl Anahtar Kavramlarını Ve Farklılıklarını Yazınız ?

Birincil Anahtar (Primary Key) ve Yabancı Anahtar (Foreign Key) veritabanı tasarımında önemli kavramlardır.

Birincil Anahtar (Primary Key) : bir tablodaki her kaydı benzersiz bir şekilde tanımlayan bir veya daha fazla sütundur. Birincil anahtarın değeri her zaman benzersiz olmalıdır ve NULL değer içeremez.

Özellikler :
1. Her kayıt için benzersiz bir kimlik sağlar.
2. NULL değer içeremez.
3. Genellikle tablo oluşturulurken tanımlanır ve genellikle bir sütun veya sütunlar grubu olarak belirlenir.

Yabancı Anahtar (Foreign Key) : bir tablodaki bir sütunun, başka bir tablodaki bir birincil anahtara referans verdiği bir ilişkidir. Yabancı anahtar, iki tablo arasında bir ilişki kurar.

Özellikler :
1. Bir tablodaki sütun, başka bir tablodaki birincil anahtarın değerini referans alır.
2. Yabancı anahtar, NULL değer içerebilir (eğer ilişki isteğe bağlıysa).
3. İlişkili tablolardaki verilerin tutarlılığını sağlamak için kullanılır.

Farklılıklar :
1. Amaç :
Birincil anahtar, bir tablodaki kayıtları benzersiz bir şekilde tanımlamak için kullanılır.
Yabancı anahtar, iki tablo arasında ilişki kurmak için kullanılır.

3. Benzersizlik :
Birincil anahtar her zaman benzersiz olmalıdır.
Yabancı anahtar, birincil anahtarın değerini referans alabilir, ancak kendisi benzersiz olmak zorunda değildir.

NULL Değer :
Birincil anahtar NULL değer içeremez.
Yabancı anahtar NULL değer içerebilir.

Kullanım :
Birincil anahtar, genellikle tablo oluşturulurken tanımlanır.
Yabancı anahtar, ilişkili tablolarda tanımlanır ve veri bütünlüğünü sağlamak için kullanılır.

7-)Veritabanı Kullanıcı Türleri Nelerdir ?

Veritabanı kullanıcı türleri genellikle aşağıdaki gibi sınıflandırılabilir :

1. Yönetici Kullanıcı (Admin User) : Veritabanının tüm yönetimsel işlemlerini gerçekleştirebilen, tüm verilere erişim hakkına sahip olan kullanıcıdır. Genellikle veritabanı oluşturma, silme, yedekleme gibi işlemleri yapabilir.
2. Geliştirici Kullanıcı (Developer User) : Uygulama geliştirme sürecinde veritabanını kullanan, sorgular yazabilen ve veritabanı yapısını değiştirebilen kullanıcıdır. Genellikle belirli izinlere sahiptir.
3. Son Kullanıcı (End User): Veritabanını kullanan, ancak veritabanı yapısını değiştirme yetkisi olmayan kullanıcıdır. Genellikle sadece veri okuma ve yazma işlemleri yapabilir.
4. Veri Analisti (Data Analyst) : Veritabanındaki verileri analiz eden ve raporlar oluşturan kullanıcıdır. Genellikle sorgular yazma ve veri çekme yetkisine sahiptir.
5. Okuyucu Kullanıcı (Read-Only User) : Veritabanındaki verilere sadece okuma izni olan kullanıcıdır. Veri değiştirme yetkisi yoktur.

Bu kullanıcı türleri, veritabanı yönetim sistemine ve organizasyonun ihtiyaçlarına göre değişiklik gösterebilir.

8-)Örnek Bir Veri Tabanı İçin Kullanıcılar Belirleyerek Yetkilendirmelerini Şematik Olarak Gösteriniz ?

![image](https://github.com/user-attachments/assets/c215c6ee-60db-40ea-9827-ac6940f29028)

Veritabanı kullanıcıları ve yetkilendirmelerini şematik olarak göstermek için aşağıdaki gibi bir yapı oluşturabiliriz. Bu örnek, kullanıcıların rollerini ve bu rollerin hangi yetkilere sahip olduğunu gösterir.
Kullanıcılar ve Yetkilendirme Şeması
Açıklamalar :
Kullanıcılar : Veritabanına erişim sağlayan bireylerdir. Örneğin, Admin, Kullanıcı1 ve Kullanıcı2.
Roller : Kullanıcıların sahip olduğu yetki gruplarıdır. Örneğin, Yönetici, Editör ve Görüntüleyici.
Yetkiler : Kullanıcıların belirli işlemleri gerçekleştirme yetenekleridir. Örneğin, yazma, okuma ve silme yetkileri.
Bu şemada, her kullanıcının bir rolü vardır ve her rol belirli yetkilere sahiptir. Örneğin, Admin rolü tüm erişim yetkisine sahipken, Görüntüleyici rolü yalnızca okuma yetkisine sahip olabilir.

9-)Veritabanı İle VTYS Farkları Nelerdir ?

1. Tanım :
Veritabanı : Verilerin saklandığı yapı.
VTYS : Veritabanlarını yöneten yazılım.

İşlev :
Veritabanı : Verileri depolar ve düzenler.
VTYS : Veritabanına erişim sağlar ve yönetir.

4. Kullanım :
Veritabanı : Verilerin depolanması için kullanılır.
VTYS : Kullanıcıların veritabanı ile etkileşimde bulunmasını sağlar.

6. Veri Yönetimi :
Veritabanı : Fiziksel veri yapısını içerir.
VTYS : Veri yönetimi ve güvenliği ile ilgili işlemleri gerçekleştirir.

10-)İlişkisel Veri Modelini Açıklayınız ?

İlişkisel veri modeli, verilerin tablolar (ilişkiler) şeklinde düzenlendiği bir yapıdır. Temel bileşenleri şunlardır :

1. Tablolar : Veriler, satır ve sütunlardan oluşan tablolarda saklanır.
2. Satırlar : Her satır, bir veri kaydını temsil eder.
3. Sütunlar : Her sütun, belirli bir veri türünü temsil eder.
4. Anahtarlar : Birincil Anahtar: Her kaydı benzersiz tanımlayan sütun.
5. Yabancı Anahtar : Bir tablodaki sütunun, başka bir tablodaki birincil anahtara referansı.
6. İlişkiler : Tablolar arasındaki bağlantılar, yabancı anahtarlar ile kurulur.

Bu model, veri bütünlüğünü sağlamak ve karmaşık sorgular yapabilmek için yaygın olarak kullanılır.

11-)Bir Öğrenci Bilgi Sistemi İçin Kullanılacak Veritabanı,Tablolar Ve Tablolar Arasındaki İlişkileri Belirleyiniz ?

Bir öğrenci bilgi sistemi için kullanılacak veritabanı tasarımı aşağıdaki gibi olabilir. Bu tasarımda, temel tablolar ve tablolar arasındaki ilişkiler belirlenmiştir :

1. Tablolar :

Öğrenciler
ogrenci_id (PK, int)
ad (varchar)
soyad (varchar)
tc_no (varchar)
dogum_tarihi (date)
email (varchar)

2. Dersler :
ders_id (PK, int)
ders_adi (varchar)
kredi (int)
ogretmen_id (FK, int)
Öğretmenler
ogretmen_id (PK, int)
ad (varchar)
soyad (varchar)
email (varchar)

4. Kayıtlar :
kayit_id (PK, int)
ogrenci_id (FK, int)
ders_id (FK, int)
yil (int)
donem (varchar)

İlişkiler :

Öğrenciler ile Kayıtlar arasında bire çok (1:N) ilişki vardır. Bir öğrenci birden fazla derse kayıt olabilir.
Dersler ile Kayıtlar arasında bire çok (1:N) ilişki vardır. Bir ders birden fazla öğrenci tarafından alınabilir.
Öğretmenler ile Dersler arasında bire çok (1:N) ilişki vardır. Bir öğretmen birden fazla dersi verebilir.


