# Tentang Project Ini
Menampilkan peta Jawa Barat, Kota-kota di Jawa Barat dan ~~Jalan Tol di Jawa Barat~~ Jalan antar Kota  
_Jalan antar Kota merupakan gabungan Jalan Tol, Jalan Raya dan Jalan Lainnya (jika ada)_

## File CSV
### roadpoint.csv
CSV ini berisikan data koordinat kota dan jalan penghubungnya, terdapat 4 kolom yaitu:
1. **nama**: berisikan nama kota / jalan
2. **tipe**: jenis data, diisikan _city_ untuk menampilkan data sebagai **Node** Kota atau _road_ untuk menampilkan data sebagai **Edges** Jalan antar Kota
3. **length**: berisikan jarak jalan untuk tipe data _road_, **untuk tipe data _city_ kolom ini tidak digunakan**
4. **koord**: berisikan titik koordinat data, berupa 1 titik `[Longitude] [Latitude]` dipisahkan dengan _spasi_ ` ` untuk tipe data _city_, atau berupa banyak titik koordinat `[Longitude] [Latitude]` untuk tipe data _road_ di mana setiap titiknya koordinatnya dipisahkan dengan _koma_ `,`  

tollpoint.csv hanya digunakan untuk mendukung argumen bahwa jalan tol tidak dapat menghubungkan setiap Node Kota

## Library Used
```
pandas
matplotlib.pyplot
geopandas
shapely.geometry
adjustText
```

### Install Library:
```
pip install pandas
pip install matplotlib
pip install geopandas
pip install shapely
pip install adjustText
```

### Untuk Pengguna Windows - Kalau gagal install geopandas:
```
pip install pipwin
pipwin install gdal
pipwin install fiona
pip install geopandas
```

### Sumber Data:
[Shapefile - Jawa Barat](https://www.indonesia-geospasial.com/2020/04/download-shapefile-shp-batas-desa.html)  
[List Kota di Jawa Barat](https://id.wikipedia.org/wiki/Daftar_kabupaten_dan_kota_di_Jawa_Barat)  
[Titik Koordinat Kota dan Jalan Tol](https://maps.google.com/)