# Overloading
## 1. Pendahuluan
Overloading adalah fitur yang memperbolehkan sebuah method memiliki nama yang sama dengan tipe data parameter yang berbeda.

Terdapat 3 variasi yang bisa dilakukan untuk melakukan overloading yaitu :

1. Membedakan jumlah parameter
2. Membedakan tipe data parameter
3. Membedakan urutan data pada parameter

Overloading dapat memiliki parameter yang berbeda, namun tipe data return dari method yang menggunakan overload harus sama. Contohnya sebagai berikut :

<center>

Valid | Invalid
------|---------
Tipe data return sama | Tipe data return tidak sama
`` void display(int, int){} `` <br> `` void display(int, float){} ``| `` void display(int, int){} `` <br> `` String display(int, float){} ``

</center>

> Overloading merupakan salah satu contoh dari static polymorphism. <br>
*Baca juga : Roadmap Programming - Polymorphisme*

## 2. Penggunaan Overloading
Seperti yang sudah dijelaskan diatas overloading menggunakan nama method yang sama namun isi parameter yang berbeda.

**Example 1 : Overloading dengan perbedaan jumlah parameter**
```java
package player;
public class Hero {
    static int level = 0;
    static void display() { // overload 0 parameter
        System.out.println("level is " + level);
    }
    static void display(int up) { // overload 1 parameter
        System.out.println("level is " + up);
    }
    public static void main(String[] args) {
        display(); 
        display(2);
    }
}
```
**Output kode :** <br> 
`` level is 0 ``<br>
`` level is 1 ``

**2. Example 2 : Overloading dengan perbedaan tipe data parameter**
```java
package player;
public class Hero {
    static int level = 0;
    static void display(double exp) { // tipe data double
        System.out.println("level is " + exp);
    }
    static void display(int up) { // tipe data int
        System.out.println("level is " + up);
    }
    public static void main(String[] args) {
        display(3.2); 
        display(2);
    }
}
```
**Output kode :** <br> 
`` level is 3.2 ``<br>
`` level is 2 ``

**3. Example 3 : Overloading dengan perbedaan urutan tipe data parameter**
```java
package player;
public class Hero {
    // tipe data pertama double, kedua integer
    static void display(double exp, int up) { 
        System.out.print("need exp " + exp);
        System.out.print(" | next level " + up);
    }

    // tipe data pertama integer, kedua double
    static void display(int up, double exp) { 
        System.out.print("\ncurrent exp " + exp);
        System.out.print(" | level is " + up);
    }

    public static void main(String[] args) {
        display(3.2, 3);
        display(2, 2.3);
    }
}
```
**Output kode :** <br> 
`` need exp 3.2 | next level 3 ``<br>
`` current exp 2.3 | level is 2 ``

## 3. Quizes
Catat pada notepad untuk menyimpan jawaban berupa ekspektasi output yang dikeluarkan, jawaban yang dapat dilihat dibagian paling bawah.

Case 1 : Overloading
```java 
int mymethod(int a, int b, float c) 
int mymethod(int var1, int var2, float var3)
```

Case 2 : Overloading
```java
int mymethod(int a, int b)
int mymethod(float var1, float var2)
```

Case 3 : Overloading
```java
int mymethod(int a, int b)
int mymethod(int num)
```

Case 4 : Overloading
```java
float mymethod(int a, float b)
float mymethod(float var1, int var2)
```
Case 5 : Overloading
```java
int mymethod(int a, int b)
float mymethod(int var1, int var2)
```

### Jawaban
Case 1 : Overload tidak dapat dijalankan karena parameter memiliki tipe yang sama dan jumlahnya sama.

Case 2 : Overload dapat dijalankan karena parameter memiliki tipe data yang berbeda.

Case 3 : Overload dapat dijalankan karena parameter memiliki jumlah yang berbeda.

Case 4 : Overload dapat dijalankan karena urutan parameter berbeda.

Case 5 : Overload tidak dapat dijalankan karena tipe data return beda dan argumen yang dibutuhkan memiliki jumlah yang sama dan tipe data argumen yang sama.

> Materi Selanjutnya : Abstract