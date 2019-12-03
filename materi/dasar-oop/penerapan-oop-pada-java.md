# Penerapan OOP pada Java

## 1. Membuat Object

### 1.1 Membuat Class

Sebelum membuat object, kita perlu membuat class terlebih dahulu, class merupakan suatu template yang nantinya dapat digunakan untuk membuat banyak object

```java
// Hero.java

class Hero {

}
```

### 1.2. Membuat Object

Untuk membuat object, kita dapat membuat variable baru menggunakan class `Hero` yang tadi sudah kita buat

```java
// Program.java

class Program {
  public static void main(String[] args) {
    // Membuat objek Hero baru bernama hero1
    Hero hero1 = new Hero();
  }
}
```

## 2. Membuat Attribute

### 2.1. Menambahkan Attribute

Untuk membuat attribute pada suatu objek, kita perlu menambahkan variable baru pada class `Hero`

```java
// Hero.java

class Hero {
  // menambahkan attribute name
  public String name;
  // menambahkan attribute health
  public int health;
}
```

### 2.2. Mengisi Nilai Attribute

Setelah membuat attribute pada class `Hero`, kita dapat mengisi nilainya pada objek `hero1` yang sudah kita buat

```java
// Program.java

class Program {
  public static void main(String[] args) {
    Hero hero1 = new Hero();

    // mengisi nilai attribute name
    hero1.name = "star platinum";
    // mengisi nilai attribute health
    hero1.health = 100;
  }
}
```

## 3. Membuat Method

### 3.1. Menambahkan Method

Untuk membuat method pada suatu objek, kita perlu menambahkannya pada class

```java
// Hero.java

class Hero {
  public String name;
  public int health;

  // method untuk terkena damage
  public void getDamage() {
    this.health -= 30;
  }

  // method untuk menampilkan informasi hero
  public void showInfo() {
    System.out.println("name : " + this.name);
    System.out.println("health : " + this.health);
  }
}
```

### 3.2. Menggunakan Method

Setelah menambahkan method pada class `Hero`, kita dapat memanggilnya melalui objek `hero1` yang sudah dibuat

```java
// Program.java

class Program {
  public static void main(String[] args) {
    Hero hero1 = new Hero();

    hero1.name = "star platinum";
    hero1.health = 100;

    // hero terkena damage
    hero1.getDamage();
    // menampilkan informasi hero
    hero1.showInfo();
  }
}
```
