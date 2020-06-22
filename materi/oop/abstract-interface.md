# Abstract & Interface

## 1. Abstract
### 1.1 Penjelasan

Abstract sendiri memiliki artian bahwa sesuatu yang masih belum jelas bentuknya ataupun wujudnya. Pada java sendiri class Abstract biasanya digunakan pada class parent atau induk. Saya disini membuat analogi bahwa saya akan membuat class BangunDatar. Nah pada dari kata BangunDatar sendiri muncul berbagai pertanyaan, bangun datar yang mana? Persegi? segitiga? atau lingkaran? nah inilah yang disebut dengan abstrak. Lalu pada class BangunDatar terdapat sebuah method ``getLuas()`` tentunya disini masih tidak jelas karena luas apa yang nantinya akan kita hitung? menggunakan bangun datar yang mana? maka dari itu kita dapat mengatakan bahwa method ``getLuas()`` ini masih abstract atau tidak jelas.

### 1.2 Implementasi Coding

Untuk lebih jelasnya maka kita akan langsung membuat scriptnya.

```java
//BangunDatar.java
public abstract class BangunDatar { 
    String warna;

    String getWarna() {
        return warna;
    }

    void setWarna(String warna) {
        this.warna = warna;
    }
    
    // Abstract Method
    abstract float getLuas();
}
```
Nah pada script diatas merupakan sebuah class abstract dan sebuah class abstract wajib memiliki 1 atau lebih method abstract. Untuk class bertipe abstract nantinya tidak akan bisa kita buat sebagai objek seperti ini ``BangunDatar bd = new BangunDatar()`` karena methodnya sendiri ada yang masih belum jelas mau dibuat BangunDatar yang mana dan abstract class tidak dapat diinstansiasi. Oke langsung kita buat script untuk Bangun Datar lingkaran.

```java
//Lingkaran.java
public class Lingkaran extends BangunDatar{
    private float jarijari;

    public Lingkaran(float jarijari) {
        this.jarijari = jarijari;
    }
    
    @Override
    float getLuas() {
        return(float) 3.14 * jarijari * jarijari;
    }
}
```

Pada script Lingkaran ini kita mengimplementasi BangunDatar menggunakan Inheritance (keyword: extends) pada setiap BangunDatar pasti memiliki identitas yang berbeda beda. Misalnya pada Lingkaran kita membutuhkan jari jari, untuk persegi kita membutuhkan sisi. Untuk script Lingkaran disini method ``getLuas()`` nya mengambil dari induk atau parent class yaitu si BangunDatar yang berbentuk abstract method. Kini method tersebut sudah jelas dan tidak abstract lagi, sudah jelas untuk menghitung Lingkaran. Maka dari itu kita langsung buat Main Class nya.

```java
//Main.java
public class Main {
    public static void main(String[] args) {
        // Membuat Objek
        BangunDatar lingkaran = new Lingkaran(7);

        lingkaran.setWarna("Biru");
        System.out.println("Luas Lingkaran " +lingkaran.getWarna()+  " = " +lingkaran.getLuas());
    }
}
```

Pada class main diatas kita membuat suatu Objek dari class Lingkaran, dan objek lingkaran bertipe BangunDatar. Maka jika program di run hasilnya sebagai berikut :

```
Output:
Luas Lingkaran Biru = 153.86002
```

## 2. Interface

## 2.1 Penjelasan

Interface sendiri sebenarnya tidak jauh berbeda dengan abstract, interface adalah sebuah class yang method method didalamnya tidak memiliki isi. Method didalam class interface ini wajib diimplementasikan pada class turunannya. Keuntungan menggunakan interface disini kita dapat meng-implementasikan lebih dari 1 class. Berbeda dengan abstract tadi yang cuma dapat mengimplementasikan 1 kelas induk/parent. Semua method didalam interface merupakan abstract method. 

## 2.2 Implementasi Coding

Pertama tama mari kita buat class abstract terlebih dahulu.
```java
public abstract class Hewan {
    private String nama;
    
    abstract String jenisHewan();

    public String getNama() {
        return nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }
}
```
Lalu kita buat class interfacenya, untuk interface pada java disarankan huruf depannya diberi I untuk identitas bahwa class ini bertipe interface.
```java
public interface ILangka {
    int sisaPopulasiHewan();
    String dilestarikanDi(); 
}
```
Membuat Class salah satu jenis hewan dan mengimplementasikan kedua class tersebut yang sudah kita buat (Hewan & ILangka)

```java
public class BadakJawa extends Hewan implements ILangka {
    private String warna;

    public String getWarna() {
        return warna;
    }

    public void setWarna(String warna) {
        this.warna = warna;
    }

    public BadakJawa() {
    }
    
    @Override
    public String jenisHewan() {
        return "Herbivora";
    }
    
    @Override
    public int sisaPopulasiHewan() {
        return 50;
    }

    @Override
    public String dilestarikanDi() {
        return "Ujung Kulon";
    }
}
```
Nah dengan adanya interface ini kita dapat mengimplementasi 1 atau lebih class, tidak seperti abstract kita hanya dapat mengextends 1 class saja. Dan penggunaan method yang berada didalam class interface ini sifatnya wajib. Oke mari kita buat Class Mainnya.
```java
public class Main {
    public static void main(String[] args) {
        BadakJawa badak1 = new BadakJawa();

        badak1.setNama("Lulu");
        badak1.setWarna("Abu-Abu");

        System.out.println("Nama = "+badak1.getNama());
        System.out.println("Warna = "+badak1.getWarna());
        System.out.println("Jenis Hewan = "+badak1.jenisHewan());
        System.out.println("Sisa hewan = "+badak1.sisaPopulasiHewan());
        System.out.println("Dilestarikan di = "+badak1.dilestarikanDi());
    }
}
```
```
Output
Nama = Lulu
Warna = Abu-Abu
Jenis Hewan = Herbivora
Sisa hewan = 50
Dilestarikan di = Ujung Kulon
```
Jadi kesimpulan dari interface adalah interface merupakan class yang bersifat abstract, method didalam class interface tidak dapat memiliki tubuh / body.
