# Inheritance

## 1. Penjelasan Inheritance

Inheritance atau pewarisan merupakan salah satu konsep pada OOP (Object Oriented Programming) dimana suatu objek dapat menurunkan attribute atau method nya ke objek yang lain.

## 2. Cara Membuat Inheritance

### 2.1 Membuat Class Parent

Pertama, buatlah sebuah class yang akan dijadikan sebagai parent class

```java
// Hero.java
class Hero
{
  public String name;
  public int health;

  public void getDamage() {
    this.health -= 100;
  }

  public void showInfo() {
    System.out.println("name : " + this.name);
    System.out.println("health : " + this.health);
  }
}
```

### 2.2 Extends Class Parent ke Class Children

Kemudian, kita tinggal membuat children class bernama `Mage` yang akan mewarisi parent class `Hero`. Semua attribute dan method yang dimiliki oleh class `Hero` akan diwariskan kepada class `Mage`

```java
// Mage.java

class Mage extends Hero
{
  public void healing() {
    // mengakses attribute health yang diwariskan dari class Hero
    this.health += 20;
  }
}
```

### 2.3 Membuat Object dari Class Children

Selanjutnya, kita bisa membuat objek dari class `Mage`. Dari objek yang dibuat, kita bisa mengakses attribute dan method yang dimiliki oleh class `Hero`

```java
// Program.java

class Program
{
  public static void main(String[] args)
  {
    Mage mage1 = new Mage();

    mage1.name = "magician red";
    mage1.health = 100;

    // mage terkena damage
    mage1.getDamage();

    // mage melakukan healing
    mage1.healing();

    // menampilkan informasi mage
    mage1.showInfo();
  }
}
```
