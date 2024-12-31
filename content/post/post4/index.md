+++
title = "Java OOP"
date = "2024-12-06"
tags = ["Hugo", "Web Development", "Tutorial"]
author = "Trương Sĩ Gia Khánh"
image = "/KhanhBlog/images/oopjava.jpg"
+++

## OOP là gì?

![OOP in Java](/KhanhBlog/images/oopjava.jpg)

OOP (Object-Oriented Programming) hay Lập trình hướng đối tượng là một phương pháp lập trình trong đó dữ liệu và các phương thức (hoặc hành vi) được tổ chức thành các đối tượng. Java là một ngôn ngữ lập trình hướng đối tượng thuần túy, nghĩa là hầu hết các ứng dụng Java đều được xây dựng dựa trên các đối tượng. Các nguyên lý cơ bản của OOP trong Java bao gồm Encapsulation (Đóng gói), Inheritance (Kế thừa), Polymorphism (Đa hình), và Abstraction (Trừu tượng).

**1. Class và Object**

Class (Lớp) là một khuôn mẫu (blueprint) dùng để tạo ra đối tượng (object). Lớp định nghĩa các thuộc tính (fields) và phương thức (methods) của đối tượng.

Object (Đối tượng) là một thể hiện cụ thể của lớp. Một đối tượng chứa dữ liệu (trong các thuộc tính) và có thể thực hiện các hành động (thông qua các phương thức).

Ví dụ về Class và Object trong Java:

```
// Định nghĩa lớp Car
class Car {
    // Thuộc tính (Fields)
    String make;
    String model;
    int year;

    // Phương thức (Method)
    void start() {
        System.out.println("The car is starting...");
    }

    void stop() {
        System.out.println("The car is stopping...");
    }
}

public class Main {
    public static void main(String[] args) {
        // Tạo một đối tượng car1 từ lớp Car
        Car car1 = new Car();
        car1.make = "Toyota";
        car1.model = "Corolla";
        car1.year = 2020;

        // Sử dụng các phương thức của đối tượng car1
        car1.start();
        car1.stop();
    }
}
```

Trong ví dụ trên, Car là lớp (class) có các thuộc tính (make, model, year) và các phương thức (start(), stop()) và car1 là đối tượng (object) của lớp Car.

**2. Encapsulation (Đóng gói)**

Encapsulation là cơ chế bảo vệ dữ liệu của đối tượng bằng cách ẩn các chi tiết thực thi bên trong đối tượng và chỉ cung cấp giao diện công khai cho người dùng tương tác với đối tượng. Điều này giúp giảm sự phụ thuộc vào các chi tiết bên trong của đối tượng, làm cho chương trình dễ bảo trì và nâng cấp.

Trong Java, Encapsulation được thực hiện bằng cách:

Đặt các thuộc tính của lớp là private để ngăn chặn truy cập trực tiếp từ bên ngoài.
Cung cấp các phương thức getter và setter công khai để truy cập và thay đổi giá trị của các thuộc tính.
Ví dụ về Encapsulation trong Java:
```
class Person {
    // Thuộc tính private, không thể truy cập trực tiếp từ bên ngoài
    private String name;
    private int age;

    // Phương thức getter và setter cho name
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    // Phương thức getter và setter cho age
    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age > 0) { // Kiểm tra điều kiện
            this.age = age;
        } else {
            System.out.println("Age must be positive.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Tạo đối tượng person và sử dụng getter/setter
        Person person = new Person();
        person.setName("Alice");
        person.setAge(25);

        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());
    }
}
```
Ở ví dụ trên, các thuộc tính name và age là private chỉ có thể được truy cập thông qua các phương thức getter và setter công khai.

**3. Inheritance (Kế thừa)**

Inheritance là một cơ chế cho phép một lớp con (subclass) kế thừa các thuộc tính và phương thức của một lớp cha (superclass). Điều này giúp tái sử dụng mã nguồn, giảm thiểu sự lặp lại, và dễ dàng mở rộng các chức năng mới.

Lớp con có thể kế thừa các phương thức và thuộc tính từ lớp cha.

Lớp con có thể ghi đè các phương thức của lớp cha (overriding).

Ví dụ về Inheritance trong Java:
```
// Lớp cha (Superclass)
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Lớp con (Subclass) kế thừa lớp Animal
class Dog extends Animal {
    // Ghi đè phương thức eat() của lớp cha
    @Override
    void eat() {
        System.out.println("The dog eats bones.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Tạo đối tượng của lớp con
        Dog dog = new Dog();
        dog.eat();  // Phương thức eat() sẽ được ghi đè bởi lớp con
    }
}
```
Trong ví dụ trên, Dog kế thừa lớp Animal và ghi đè phương thức eat() của lớp cha. Khi gọi dog.eat(), phương thức eat() của lớp Dog được thực thi thay vì phương thức của lớp Animal.

**4. Polymorphism (Đa hình)**

Polymorphism cho phép các đối tượng khác nhau có thể trả về các hành vi khác nhau khi gọi một phương thức giống nhau. Có hai loại đa hình trong Java:

Đa hình thông qua kế thừa (Overriding): Khi một phương thức của lớp cha được lớp con ghi đè.
Đa hình thông qua giao diện (Interface): Khi nhiều lớp thực thi cùng một giao diện.
Ví dụ về Polymorphism trong Java:
```
class Animal {
    void sound() {
        System.out.println("Some generic animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Meow");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();  // Tạo đối tượng lớp cha
        Animal myDog = new Dog();        // Tạo đối tượng lớp con
        Animal myCat = new Cat();        // Tạo đối tượng lớp con

        myAnimal.sound();  // Output: Some generic animal sound
        myDog.sound();     // Output: Bark
        myCat.sound();     // Output: Meow
    }
}
```
Trong ví dụ này, các đối tượng myAnimal, myDog, và myCat đều gọi phương thức sound(), nhưng mỗi đối tượng có cách thực thi khác nhau (hành vi khác nhau) tùy vào lớp mà nó thuộc về.

**5. Abstraction (Trừu tượng)**

Abstraction giúp ẩn đi các chi tiết thực thi phức tạp và chỉ hiển thị các đặc điểm quan trọng của đối tượng. Trong Java, abstraction có thể đạt được thông qua:

Lớp trừu tượng (abstract class): Lớp không thể khởi tạo trực tiếp mà chỉ được kế thừa.
Giao diện (interface): Định nghĩa các phương thức mà các lớp con phải triển khai.
Ví dụ về Abstraction trong Java:
```
abstract class Animal {
    abstract void sound();  // Phương thức trừu tượng
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        myDog.sound();  // Output: Bark
    }
}
```

Trong ví dụ này, lớp Animal là một lớp trừu tượng với phương thức sound() không có phần thân và lớp Dog phải triển khai phương thức sound().

**6. Kết luận**

OOP trong Java giúp chương trình dễ dàng bảo trì, mở rộng và tái sử dụng mã nguồn. Các nguyên lý cơ bản như Encapsulation, Inheritance, Polymorphism, và Abstraction giúp tổ chức mã nguồn một cách có cấu trúc và dễ hiểu, đồng thời nâng cao khả năng mở rộng và giảm sự phụ thuộc giữa các thành phần trong chương trình.
