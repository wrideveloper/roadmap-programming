# Variabel & Tipe Data

## 1. Pendahuluan

Variabel adalah suatu wadah untuk menyimpan nilai sementara. Nilai yang disimpan bisa berubah ubah, tidak tetap. Aturan penamaan variabel yang cukup terkenal menggunakan gaya "`camelCase`" yang diawali dengan huruf kecil dan setiap 1 suku kata dipisah dengan huruf besar contohnya "`namaLengkap`, `sepedaGunung`". Kita tidak boleh membuat nama variabel yang sama dengan kata kunci dari Java contohnya `if,switch,for,while` dll. Lalu tipe data adalah jenis data yang disimpan pada variabel. Ada bermacam macam tipe data pada java, contohnya sebagai berikut.

- **String**: Isinya berupa karakter yang membentuk suatu teks, contohnya _Hallo Java_.

- **int**: Isinya berupa angka yang bulat contohnya _09,29,2000._

- **float**: Isinya berupa bilangan desimal contohnya _91.09_

- **double**: Isinya sama seperti float yaitu berupa bilangan desimal tapi kapasitasnya lebih besar.

- **char**: Isinya berupa suatu karakter contohnya _A_.

- **boolean**: Isinya hanya berupa nilai _true_ dan _false_

## 2. Membuat Variabel Menggunakan Java

Format penulisan variabel pada java seperti berikut.

```java
// Variabel Kosong
int jumlahRoda;
```

Pada contoh diatas kita membuat suatu variabel yang nantinya digunakan untuk menyimpan jumlah suatu roda dari kendaraan. Dan roda pasti bernilai bulat, maka dari itu kita menggunakan int untuk tipe datanya. Lalu kita coba isi variabelnya.

```java
// Variabel memiliki nilai
int jumlahRoda = 4;
```

Jika kita ingin membuat beberapa variabel kosong dengan tipe data yang sama dapat kita pisahkan dengan koma.

```java
int i, j, k;
```

## 3. Membuat Program Sederhana

Program pertama yang akan kita buat adalah Biodata.

```java
package javaapp;

public class Biodata {
    public static void main(String[] args) {
        //Membuat Variabel
        String nama, hobby;
        int usia;
        double tinggi, berat;
        // Pengisian Variabel
        nama = "Jean Pierre";
        hobby = "Melukis";
        usia = 20;
        tinggi = 172.8;
        berat = 68.4;
        // Mencetak Isi Variabel
        System.out.println("Nama: "+nama);
        System.out.println("Hobby: "+hobby);
        System.out.println("Usia: "+usia);
        System.out.println("Tinggi: "+tinggi);
        System.out.println("Berat: "+berat);
    }
}
```

Lalu untuk program kedua kita membuat program untuk menghitung luas lingkaran.

```java
package javaapp;
public class Lingkaran {
    public static void main(String[] args) {
        double phi,luas;
        int r;

        r = 14;
        phi = 3.14;

        luas = phi * r * r;

        System.out.println("Luas Lingkaran dengan jari jari "+r+" adalah "+luas);
    }
}
```
