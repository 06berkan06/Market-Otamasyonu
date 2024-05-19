Bunlar örnekler
![image](https://github.com/06berkan06/Market-Otamasyonu/assets/113473925/8bdd9d5f-ad5e-455e-bebd-3fd155266451)
![image](https://github.com/06berkan06/Market-Otamasyonu/assets/113473925/1277513e-9585-4879-8ede-c3c445b2439e)

benimki![image](https://github.com/06berkan06/Market-Otamasyonu/assets/113473925/ef243bdc-82ab-4105-8fb4-b0dcd3d8e978)




create database market;
use market;
create table urunler(
urun_id int primary key auto_increment not null,
urun_ismi varchar(40) not null,
kategori_id int not null,
tedarikci_id int not null,
alis_fiyat decimal(5,2) not null,
satis_fiyat decimal(5,2) not null
);
create table Tedarikciler(
tedarikci_id int primary key auto_increment not null,
tedarikcifirmaismi varchar(40) not null,
tedarikci_adres varchar(50) not null,
tedarikci_telno int not null
);
create table musteriler(
musteri_id int primary key auto_increment not null,
musteri_adi varchar(40) not null,
musteri_soyadi varchar(40) not null,
musteriler_adresi varchar(90) not null,
musteriler_telno int not null,
musteriler_email varchar(50) not null,
urun_id int not null
);
create table kategoriler(
kategori_id int primary key auto_increment not null,
kategori_adi varchar(40) not null,
calisanlar_id int not null
);
create table siparisler(
siparis_id int primary key auto_increment not null,
urun_id int not null,
musteriler_id int not null,
tarih date not null
);
create table Calisanlar(
calisanlar_id int primary key auto_increment not null,
calisanlar_adi varchar(40) not null,
calisanlar_soyadi varchar(40) not null,
calisanlar_adresi varchar(50) not null,
calisanlar_telno int not null,
calisanlar_email varchar(50) not null,
kategori_id int not null
);


