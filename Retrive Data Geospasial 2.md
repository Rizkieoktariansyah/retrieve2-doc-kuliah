Retrive Data Geospasial 2

<img src="./media/image1.png" width="368" height="221" />

Latar Belakang

Dalam beberapa situs telah tersedia data berupa data shapefile cpntphnya ESRI. Namun file tersebut masih harus memerlukan bantuan software pendukungnya seperti QGIS dan Phyton karena file tersebut maih belum bisa diolah secara langsung. Pada shapefile terdapat file shp dan juga dbf.

Dalam sebuah file geometri terdapat beberapa bagian yaitu :

-   Poin

    Poin ini berupa sebuah titik. Poin ini biasa digunakan untuk menunjukan sebuah lokasi di pera

-   Poliline

    Poliline ini berupa garis garis, biasa digunakan untuk menunjukan batas-batas suatu lokasi

-   Polygon

    Polygon ini berupa garis garis juga tetapi dia mempertemukan titik awal dan titik akhir

Lalu untuk me-retrieve data geospasial, kita bisa melakukannya menggunakan python. Caranya adalah dengan melakukan import shapefile terlebih dahulu lalu select/view record data shapefilenya.

-   **membaca semua geometri record**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    baca.shapes()

-   **membaca geometri record ke-n (sebagai contoh kita gunakan record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    baca.shape(0)

-   **membaca record atribut shapefile, shapeType (record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    atribut = baca.shape(0)
    atribut.shapeType

-   **membaca record atribut shapefile, parts (record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    atribut = baca.shape(0)
    atribut.parts

-   **membaca record atribut shapefile, bbox (record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    atribut = baca.shape(0)
    atribut.bbox

-   **membaca record atribut shapefile, points (record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    atribut = baca.shape(0)
    atribut.points

-   **membaca semua data record**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    baca.records()

-   **membaca data record ke-n (record ke-0)**
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    baca.record(0)

-   **mencari data record tertentu **
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    for a in sf.records():
    if a\[8\] == "Indonesia":
    print a
    - disini saya memeberi contoh menampilkan data record yang bernama “Indonesia” dan jika ada makan akan ditampilkan data recordnya Indonesia

    <img src="./media/image2.png" width="324" height="174" />

-   **mengetahui urutan data record **
    import shapefile
    baca = shapefile.Reader("cultural.shp")
    1=0
    for a in sf.records():
    if a\[8\] == "Indonesia":
    print i
    i = i+1

<!-- -->

-   kode ini akan memperlihatkan urutan keberapa data record “Indonesia” berada

    <img src="./media/image2.png" width="354" height="189" />

Kesimpulan

Untuk mengelola sebuah shapefile maka masih diperlukan sebuah software seperti QGIS dan Phyton. Kita dapat membaca record shapefile menggunakan python dengan **shapes() **dan **records()**.
