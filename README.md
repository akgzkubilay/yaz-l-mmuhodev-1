# yazılımMuhendizliğiOdev-1

CREATE DATABASE okul;
CREATE TABLE TemizlikGörevlisi (
    ogrenci_id SERIAL PRIMARY KEY,
    ad VARCHAR(50),
    soyad VARCHAR(50),
    sinif VARCHAR(10)
);
CREATE TABLE öğrenci (
    ogretmen_id SERIAL PRIMARY KEY,
    ad VARCHAR(50),
    soyad VARCHAR(50),
    bolum VARCHAR(50)
);
CREATE TABLE Ogretmen (
    ogretmen_id SERIAL PRIMARY KEY,
    ad VARCHAR(50),
    soyad VARCHAR(50),
    bolum VARCHAR(50)
);
CREATE TABLE Ders (
    ders_id SERIAL PRIMARY KEY,
    ders_adi VARCHAR(100),
    ogretmen_id INT REFERENCES Ogretmen(ogretmen_id)
);
CREATE TABLE Sinif (
    sinif_id SERIAL PRIMARY KEY,
    sinif_adi VARCHAR(20),
    ders_id INT REFERENCES Ders(ders_id)
);
