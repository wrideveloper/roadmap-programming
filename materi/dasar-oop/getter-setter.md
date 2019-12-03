# Getter dan Setter

## 1. Penjelasan

### 1.1. Penjelasan Getter

Getter merupakan method yang digunakan untuk mengambil nilai dari suatu attribute yang dimiliki oleh object

### 1.2. Penjelasan Setter

Setter merupakan method yang digunakan untuk memberikan nilai pada suatu attribute yang dimiliki oleh object

## 2. Cara Membuat Getter dan Setter

```java
// Hero.java

class Hero
{
  public String name;

  // ubah attribute health menjadi private
  private int health;

  // tambahkan method getter untuk health
  public int getHealth() {
    return this.health;
  }

  // tambahkan method setter untuk health
  public void setHealth(int health) {
    this.health = health;
  }
}
```

## 3. Cara Menggunakan Getter dan Setter

Setelah method getter dan setter dibuat pada suatu class, maka kita bisa menggunakannya pada method main seperti berikut

```java
// Program.java

class Program {
  public static void main(String[] args) {
    Hero hero1 = new Hero();
    hero1.name = "star platinum";

    // baris berikut akan menimbulkan error karena attribute health private
    hero1.health = 100;

    // memberikan nilai pada health hanya bisa lewat setter
    hero1.setHealth(100);
    // mengambil nilai dari health hanya bisa lewat getter
    System.out.println(hero1.getHealth());
  }
}
```

## 4. Kenapa Butuh Getter dan Setter

Terkadang kita perlu membatasi akses dari suatu attribute, misalnya, hanya bisa dibaca saja (get) atau diubah saja (set)

Sebagai contoh, attribute `health` seharusnya hanya bisa di ubah nilainya menggunakan method `getDamage`, dan tidak bisa diubah secara langsung
