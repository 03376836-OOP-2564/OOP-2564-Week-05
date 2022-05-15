# Assignment
 Assignment นี้เป็นการรวม Assignment ของเนื้อหาในสองสัปดาห์ที่เรียนเรื่อง Abstraction  


----
## 1. ให้นำโค้ดต่อไปนี้ไป render ให้เป็น class diagram แล้วนำผลที่ได้มาใส่ใน markdown##
   
   a. ใช้โปรแกรม plantUML บนเว็บ

   b. ใช้ extension ใน VScode
   
   c. ใช้โปรแกรม PlantUML.jar ที่ดาวน์โหลดมาทำงานแบบ offline บนเครื่องของนักศึกษาเอง

### 1.1 Code ของตัวอย่างที่ 3 (สไลด์ที่ 19) ###

``` puml
@startuml 
class Dog{}
class Cat{}
class WhiteAnimals{}
class BlackAnimals{}

WhiteAnimals <|.. whiteCat
WhiteAnimals <|.. whiteDog
BlackAnimals <|.. blackCat
BlackAnimals <|.. blackDog
Cat <|.. whiteCat
Dog <|.. whiteDog
Cat <|.. blackCat
Dog <|.. blackDog
@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 19 ####

![Slide19](./puml-codes/Slide19.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

### 1.2 Code ของตัวอย่าง ปรับปรุงการทำ Classification ของหมาและแมว (สไลด์ที่ 20) ###

``` puml
@startuml 
class Dog{}
class Cat{}

Cat <|.. whiteCat
Dog <|.. whiteDog
Cat <|.. blackCat
Dog <|.. blackDog
@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 20 ####

![Slide20](./puml-codes/Slide20.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้


#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสคือการทำ Inheritance ####

``` puml
@startuml 
"Base class" <|-- "Derived class"
@enduml 
```

![Inheritance](./puml-codes/Inheritance-example.png)

### 1.3 Classification ของ class คน (สไลด์ที่ 21) ###

``` puml
@startuml 
class Person{
    - Name
    # Lastname
    - Gender
    - Age
    + TellNameAndLastName()
    + TellGender()
    + TellAge()
}

object Somsree
object Somkuan
object Somjit
object Somsak

Person <|.. Somsree
Person <|.. Somkuan
Person <|.. Somjit
Person <|.. Somsak

@enduml 
```

#### ผลที่ได้จากการ render สไลด์ 21 ####


![Slide21](./puml-codes/Slide21.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสและเส้นประคือการทำ Instantiation (สร้างวัตถุ) ####


``` puml
@startuml 
"Base class" <|.. "Derived class"
@enduml 
```
![Instantiation](./puml-codes/Instantiation-example.png)


### 1.4 การสร้างวัตถุจาก Class คน  (สไลด์ที่ 22) ###

``` puml
@startuml 
class Person{}
object Somsree
object Somkuan
object Somjit
object Somsak

Person <|.. Somsree
Person <|.. Somkuan
Person <|.. Somjit
Person <|.. Somsak

@enduml 
```
#### ตัวอย่างผลที่ได้จากการ render สไลด์ 22 ####

![Slide22](./puml-codes/Slide22.png)

--- 
## 2. ให้แก้ไข code ไฟล์ puml เพื่อให้ได้ภาพตามสไลด์ต่อไปนี้  ##

### 2.1 สไลด์หมายเลข 44 ###

``` puml
@startuml 
class classroom{}
class Whiteboard{}
class Table{}
class Chair{}
class Student{}
class Teacher{}
classroom o-- Whiteboard
classroom o-- Table
classroom o-- Chair
classroom o-- Student
classroom o-- Teacher
@enduml 
```
![image](https://user-images.githubusercontent.com/92081957/168483704-3f6834db-fc86-4869-9353-4f1596bc3c29.png)


### 2.2 สไลด์หมายเลข 45 ###

``` puml
@startuml 
class MotorBoat{}
class Car{}
class Helm{}
class Engine{}
class Door{}
class Wheel{}
class SteeringWheel{}
MotorBoat o-- Helm
MotorBoat o-- Engine
Car o-- Engine
Car o-- Door
Car o-- Wheel
Car o-- SteeringWheel
@enduml 
```
![image](https://user-images.githubusercontent.com/92081957/168483763-ffd66448-92d4-4f53-92f6-828d69e8495b.png)


### 2.3 สไลด์หมายเลข 51 ###

``` puml
@startuml 

class Car{}
class Engine{}
class Wheel{}
class AirConditionner{}

Car o-- "1..1" Engine
Car o-- "2..4" Door
Car o-- "4..4" Wheel
Car o-- "0..1" AirConditionner

@enduml  
```
![image](https://user-images.githubusercontent.com/92081957/168483973-42ec3446-511c-4c95-a286-a30947e11d20.png)


#### หมายเหตุ การเขียน cardinality ทำได้โดยใช้รูปแบบดังต่อไปนี้ ####

``` puml
@startuml 
class Car{}
class Engine{}
Car <|-- "1..1" Engine
Car <|-- "2..4" Door
@enduml 
```
ซึ่งจะได้ไดอะแกรมดังรูป

![Cardinality-example](./puml-codes/Cardinality-example.png)


### 2.4 Aggregation ของคลาส หนังสือ  (สไลด์หมายเลข 54) ###

``` puml
@startuml 

class Book{}
class Cover{}
class Introduction{}
class List{}
class Content{}
class Bibliography{}

Book o-- "2..2" Cover
Book o-- "1..1" Introduction
Book o-- "1..1" List
Book o-- "1..N" Content
Book o-- "1..1" Bibliography

@enduml 
```
![image](https://user-images.githubusercontent.com/92081957/168484019-2275fb9e-69e9-4a3c-b7f2-87810e73407e.png)


### 2.5 เพิ่ม Attribute และ Method ให้กับ Class หนังสือ   (สไลด์หมายเลข 56) ###

``` puml
@startuml 

class Book{
    - ISBN 
    - Name
    + Read()
    + Print()
}
class Cover{
    + Typecover
    + Open()
}
class Introduction{
    - Textmessage
    - Authorname
    + Read()
}
class List{
    - Textmessage
    + Read()
}
class Content{
    - Chapter
    + Read()
}
class Bibliography{
    - Textmessage
    + Read()
}
class Paper{
    - ContentofPaper
    + Open()
    + Read()
}
class Picture{
    - Image
    + See()
}
class Font{
    - Character
    + Spell()
}
Book o-- Cover
Book o-- Introduction
Book o-- List
Book o-- Content
Book o-- Bibliography
Content o-- Paper
Paper o-- Picture
Paper o-- Font
@enduml  
```
![image](https://user-images.githubusercontent.com/92081957/168484051-c79e31ac-73d2-4b54-baee-cb6bdde87424.png)



### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###

![image](https://user-images.githubusercontent.com/92081957/168484108-77655798-c0c9-4a54-93da-412b721a48a2.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###

![image](https://user-images.githubusercontent.com/92081957/168484118-b4d7cee1-d731-42de-b126-dcf44f5c12e2.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###

![image](https://user-images.githubusercontent.com/92081957/168484129-533edecc-ccb8-4c68-9811-87cf3a5394cd.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###

![image](https://user-images.githubusercontent.com/92081957/168484154-0ffff09e-ad28-4e1f-9f15-4c0697ccf2a0.png)

---
