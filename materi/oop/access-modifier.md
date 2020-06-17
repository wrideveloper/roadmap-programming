# Access Modifier

## 1. Pendahuluan
Access Modifier berfungsi untuk mengatur akses level antara class. 
Access modifier ini digunakan untuk class, variable, fungsi dan constructor.

Jenis-jenis access modifier :
1. Default
2. Private
3. Public
4. Protected

## 2. Default Access Modifier
Default Access Modifier mengatur hak akses object yang hanya bisa diakses oleh class lain apabila terdapat di package yang sama.

Untuk Menggunakan Default, kita tidak perlu mendeklarasikan access modifier untuk class, variabel atau fungsi yang akan digunakan. 

Contohnya sebagai berikut :

```java
// Hero.java
package player;
  class Hero{ // class default
    int level = 0; // variable default
    void display(){ // fungsi default
        System.out.println("constructor Hero");
  }
}

// MainLevel.java
package level;
import player.*;
  class MainLevel{ //
    public static void main(String args[]){
      //Inisialisasi dari class Hero
      Hero hero = new Hero();
      hero.display();
    }
  }
```

**Output Kode** : Kode tidak bisa dijalankan karena berada di package yang berbeda.

**Kesimpulan** : Object dengan Default Access Modifier dapat diakses oleh semua class dari package yang sama.

## 3. Public Access Modifier
Public Access Modifier mengatur hak akses object supaya dapat diakses oleh class dari package manapun.

Untuk menggunakan access modifier public, kita perlu mendeklarasikan `public` pada class, variabel atau fungsi yang akan digunakan.

contohnya sebagai berikut :

```java
// Hero.java
package player;
public class Hero { // class public
    public int level = 0; // variable public
    public void display() { // fungsi public
        System.out.println("level is " + level);
    }
}

// MainLevel.java
package level;
import player.*;
class MainLevel {
  public static void main(String args[]) {
    // Inisialisasi dari class Hero
    Hero hero = new Hero();
    hero.display();
  }
}
```
**Output Kode** :
```level is 0```

**Kesimpulan** : Object dengan Public Access Modifier dapat diakses oleh semua class dari semua package.

## 4. Private Access Modifier
Private Access Modifier mengatur hak akses object supaya dapat diakses oleh class dari package manapun.

Untuk menggunakan access modifier private, kita perlu mendeklarasikan `private` pada class, variabel atau fungsi yang akan digunakan.

contohnya sebagai berikut :

```java
// Hero.java
package player;
public class Hero { // class public
    public int level = 0; // variable public
    public void display() { // fungsi public
        System.out.println("level is " + level);
    }
}

// MainLevel.java
package level;
import player.*;
class MainLevel {
  public static void main(String args[]) {
    // Inisialisasi dari class Hero
    Hero hero = new Hero();
    hero.display();
  }
}
```
**Output Kode** :
```level is 0```

**Kesimpulan** : Object dengan Public Access Modifier dapat diakses oleh semua class dari semua package.

## 5. Protected Access Modifier
Protected Access Modifier mengatur hak akses object supaya dapat diakses oleh class yang menjadi turunan.

> Berikut adalah penjelasan dari class turunan (*inheritance*)

Untuk menggunakan access modifier protected, kita perlu mendeklarasikan `protected` pada variabel, fungsi atau constructor yang akan digunakan.

** ``protected`` tidak dapat digunakan pada class.

contohnya sebagai berikut :

```java
// Hero.java
package player;
public class Hero {
    protected int level = 0; // protected variable
    protected Hero() { // protected constructor
        level = 1;
    }
    protected void display() { // protected methods
        System.out.println("level is " + level);
    }
}

// MainLevel.java
package level;
import player.*;
class MainLevel extends Hero {
  public static void main(String args[]) {
    MainLevel main = new MainLevel();
    main.display();
  }
}
```
**Output Kode** :
```level is 1```

**Kesimpulan** : Object dengan Protected Access Modifier hanya dapat diakses oleh sub-class atau class turunan.

## 6. Kesimpulan Access Modifier~

Access Modifier | Class | Package | Subclass | Global
------------ | ------------ | ------------ | ------------ | ------------
**Public** | Yes | Yes | Yes |Yes
**Protected** | Yes | Yes | Yes | No
**Default** | Yes | Yes | No | No
**Private** | Yes | No | No | No
