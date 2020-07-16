# Input dan Output

## 1. Pendahuluan

Pada materi sebelumnya kita sudah mengenal variabel dan tipe data. Nah pada materi kali ini kita akan mengenal yang namanya input dan output. Pada sebelumnya kita membuat program biodata namun program tersebut masih tergolong statis maksutnya adalah jika kita ingin mengubah nilai dari variabelnya kita harus mengedit kodingan secara manual. Nah maka dari itu kali ini kita akan membuat suatu program yang dinamis, memasukan nama dengan cara mengetikan nama kita secara manual pada layar dan nanti output atau hasil yang dikeluarkan sesuai dengan inputan yang kita buat.

Pada Java kita membutuhkan suatu kode yang isinya memanggil suatu class yang nantinya kita gunakan untuk memasukan suatu data pada variabel yang telah kita buat. Kodenya seperti berikut

```java
import java.util.Scanner;
```

## 2. Membuat Program dengan Input dan Output

Program yang kita buat adalah Biodata, mengganti program statis biodata yang telah kita buat kemarin menjadi dinamis.

```java
package javaapp;
import java.util.Scanner;
public class Biodata {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String nama, hobby;
        int usia;
        double tinggi, berat;

        System.out.println("--Program Biodata--");
        System.out.print("Masukan Nama: ");
        nama = sc.nextLine();
        System.out.print("Masukan Hobby: ");
        hobby = sc.nextLine();
        System.out.print("Masukan Usia: ");
        usia = sc.nextInt();
        System.out.print("Masukan Tinggi: ");
        tinggi = sc.nextDouble();
        System.out.print("Masukan Berat: ");
        berat = sc.nextDouble();

        System.out.println("--Biodata Anda--");
        System.out.println("Nama: "+nama);
        System.out.println("Hobby: "+hobby);
        System.out.println("Usia: "+usia);
        System.out.println("Tinggi: "+tinggi);
        System.out.println("Berat: "+berat);
    }
}
```

```bash
Outout:
--Program Biodata--
Masukan Nama: Ardan
Masukan Hobby: Bersepeda
Masukan Usia: 20
Masukan Tinggi: 172.5
Masukan Berat: 65.3
--Biodata Anda--
Nama: Ardan
Hobby: Bersepeda
Usia: 20
Tinggi: 172.5
Berat: 65.3
```

Pada program diatas kita sudah bisa menerima inputan dan mengeluarkannya dalam output. Hal yang harus diperhatikan adalah sebagai berikut `Scanner sc = new Scanner(System.in);` sc disini merupakan variabel bebas yang dapat kita ganti apa saja. Contohnya `Scanner input = new Scanner(System.in);`. Lalu hal kedua yang harus diperhatikan adalah `alamat = keyboard.nextLine();` alamat merupakan suatu variabel bertipe data String, maka dari itu ia menggunakan `nextLine()`, jika bertipe int `nextInt()`, bertipe double `nextDouble()` dan seterusnya. Peletakan `import java.util.Scanner;` sesudah package. Perbedaan `System.out.println` dan `System.out.print` adalah jika kita menggunakan `println` maka kita akan membuat baris baru namun jika `print` biasa maka tidak akan membuat baris baru.
