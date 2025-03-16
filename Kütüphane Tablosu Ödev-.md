create database kutuphane; --bir kez database oluşturulurken çalıştırılır.

use Kutuphane -- bu kütüphaneyi kullanarak tablo ekleyebiliriz

-- 1) ADRESLER Tablosu
-- Kütüphane ve üyelerin adres bilgilerini tutar

create table adresler(
adresNo int not null identity(1,1) primary key, -- Otomatik artan benzersiz adres numarası
sehir nvarchar(30),                             -- Adresin bulunduğu şehir
cadde nvarchar(30),                             -- Cadde adı
mahalle nvarchar(30),                           -- Mahalle adı
ilce nvarchar(30),                              -- İlçe adı
adresSatiri nvarchar(255),                      -- Tam adres satırı
posta_Kodu nvarchar(10),                        -- Posta kodu
ulke nvarchar(100)                              -- Ülke adı
);


-- 2) UYELER Tablosu
-- Kütüphane üyelerinin bilgilerini tutar

create table Uyeler(
Uye_No int not null identity(1,1) primary key,  -- Otomatik artan benzersiz üye numarası
Uye_Ad nvarchar(50) not null,                   -- Üyenin adı (boş olamaz)
Uye_Soyad nvarchar(50) not null,                -- Üyenin soyadı (boş olamaz)
Telefon nvarchar(20) not null,                  -- Üyenin telefon numarası (boş olamaz)
Cinsiyet nvarchar(10),                          -- Üyenin cinsiyeti
Eposta nvarchar(100),                           -- Üyenin e-posta adresi
DogumTarihi date                                -- Üyenin doğum tarihi
);

-- 3) KUTUPHANE Tablosu
-- Kütüphane bilgilerini tutar

create table Kutuphane(
Kutuphane_No int identity(1,1) not null primary key, -- Otomatik artan benzersiz kütüphane numarası
Kutuphane_Adi nvarchar(100) not null,                -- Kütüphane adı (boş olamaz)
KutuphaneIletisim nvarchar(100),                     -- Kütüphane iletişim bilgileri
Aciklama nvarchar(255),                              -- Kütüphane hakkında açıklama
adresNo int foreign key (adresNo) references adresler(adresNo) -- Kütüphanenin adres bilgisi (adresler tablosuyla ilişki)
);

-- 4) KATEGORILER Tablosu
-- Kitap kategorilerini tutar

create table Kategoriler(
Kategori_No int not null identity(1,1) primary key, -- Otomatik artan benzersiz kategori numarası
Kategori_Adi nvarchar(50) not null                  -- Kategori adı (boş olamaz)
);

-- 5) YAZARLAR Tablosu
-- Kitap yazarlarının bilgilerini tutar

create table Yazarlar(
Yazar_No int not null identity(1,1) primary key, -- Otomatik artan benzersiz yazar numarası
Yazar_Ad nvarchar(50) not null,                  -- Yazarın adı (boş olamaz)
Yazar_Soyad nvarchar(50),                        -- Yazarın soyadı
YazarBilgi nvarchar(255)                         -- Yazar hakkında bilgi
);

-- 6) KITAPLAR Tablosu
-- Kitap bilgilerini tutar

create table kitaplar(
ISBN int not null primary key,                   -- Kitabın ISBN numarası (benzersiz)
Kitap_Adi nvarchar(100) not null,                -- Kitabın adı (boş olamaz)
Yayin_Tarih date,                                -- Kitabın yayın tarihi
Sayfa_Sayisi int,                                -- Kitabın sayfa sayısı
Kutuphane_No int foreign key (Kutuphane_No) references Kutuphane(Kutuphane_No) -- Kitabın bulunduğu kütüphane (Kutuphane tablosuyla ilişki)
);

-- 7) EMANET Tablosu
-- Kitap ödünç alma işlemlerini tutar

create table emanet(
emanet_no int identity(1,1) not null primary key, -- Otomatik artan benzersiz emanet numarası
emanet_tarih date not null,                       -- Emanet alma tarihi (boş olamaz)
teslim_tarih date,                                -- Teslim tarihi (null ise henüz teslim edilmemiş)
uye_No int foreign key (uye_No) references Uyeler(Uye_No) -- Emanet alan üye (Uyeler tablosuyla ilişki)
);


-- 8) UYELERINADRESLERI Tablosu (İlişki Tablosu)
-- Üyeler ve adresler arasındaki çoka-çok ilişkiyi tutar
-- Bir üyenin birden fazla adresi olabilir, bir adres birden fazla üyeye ait olabilir

create table UyelerinAdresleri(
Uye_No int foreign key(Uye_No) references Uyeler(Uye_No),         -- Üye numarası (Uyeler tablosuyla ilişki)
adresNo int foreign key(adresNo) references adresler(adresNo),    -- Adres numarası (adresler tablosuyla ilişki)
primary key (Uye_No, adresNo)                                     -- Bileşik anahtar
);


-- 9) KITAPKATEGORI Tablosu (İlişki Tablosu)
-- Kitaplar ve kategoriler arasındaki çoka-çok ilişkiyi tutar
-- Bir kitap birden fazla kategoriye ait olabilir, bir kategori birden fazla kitabı içerebilir

create table KitapKategori(
ISBN int foreign key(ISBN) references Kitaplar(ISBN),                      -- Kitap ISBN (kitaplar tablosuyla ilişki)
Kategori_No int foreign key(Kategori_No) references Kategoriler(Kategori_No), -- Kategori numarası (Kategoriler tablosuyla ilişki)
primary key (ISBN, Kategori_No)                                            -- Bileşik anahtar
);


-- 10) KITAPYAZAR Tablosu (İlişki Tablosu)
-- Kitaplar ve yazarlar arasındaki çoka-çok ilişkiyi tutar
-- Bir kitabın birden fazla yazarı olabilir, bir yazar birden fazla kitap yazabilir

create table KitapYazar(
ISBN int foreign key(ISBN) references Kitaplar(ISBN),                -- Kitap ISBN (kitaplar tablosuyla ilişki)
Yazar_No int foreign key(Yazar_No) references Yazarlar(Yazar_No),    -- Yazar numarası (Yazarlar tablosuyla ilişki)
primary key (ISBN, Yazar_No)                                         -- Bileşik anahtar
);


-- 11) EMANETKITAP Tablosu (İlişki Tablosu)
-- Emanet ve kitaplar arasındaki çoka-çok ilişkiyi tutar
-- Bir emanet işleminde birden fazla kitap alınabilir, bir kitap farklı zamanlarda emanet alınabilir

create table EmanetKitap(
emanet_no int foreign key(emanet_no) references emanet(emanet_no),  -- Emanet numarası (emanet tablosuyla ilişki)
ISBN int foreign key(ISBN) references Kitaplar(ISBN),               -- Kitap ISBN (kitaplar tablosuyla ilişki)
primary key (emanet_no, ISBN)                                       -- Bileşik anahtar
);


-- 12) KUTUPHANEKITAP Tablosu (İlişki Tablosu)
-- Kütüphane ve kitaplar arasındaki çoka-çok ilişkiyi tutar
-- Bir kütüphanede birden fazla kitap bulunabilir, bir kitap farklı kütüphanelerde bulunabilir
-- Ayrıca her kitabın her kütüphanedeki miktarını da tutar

create table KutuphaneKitap(
Kutuphane_No int foreign key(Kutuphane_No) references Kutuphane(Kutuphane_No), -- Kütüphane numarası (Kutuphane tablosuyla ilişki)
ISBN int foreign key(ISBN) references Kitaplar(ISBN),                          -- Kitap ISBN (kitaplar tablosuyla ilişki)
Miktar int default 1,                                                          -- Kitabın kütüphanedeki miktarı (varsayılan 1)
primary key (Kutuphane_No, ISBN)                                               -- Bileşik anahtar
); 
