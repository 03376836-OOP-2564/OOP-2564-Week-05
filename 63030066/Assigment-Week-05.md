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

![image](https://user-images.githubusercontent.com/92080550/169567204-dff4c161-2e11-4457-8cfc-fc5106e0b876.png)


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

![image](https://user-images.githubusercontent.com/92080550/169567387-03795f9f-0692-40ab-b4d7-8b60ce133303.png)


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


![image](https://user-images.githubusercontent.com/92080550/169567499-02720639-4681-4b85-9ee0-3a7f4a6fdab8.png)

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
![image](https://user-images.githubusercontent.com/92080550/169567738-85f83229-aee0-46dc-9509-9150bad45512.png)

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
![image](https://user-images.githubusercontent.com/92080550/169567822-ddfac320-1892-4141-9f5f-e5afbad0c395.png)

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
![image](https://user-images.githubusercontent.com/92080550/169567930-5ffe1c01-0fa8-4e69-b63d-03800a9857d3.png)


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
![image](https://user-images.githubusercontent.com/92080550/169567993-550a8d02-eaa9-4655-b539-d253dcd51fff.png)

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

![image](https://user-images.githubusercontent.com/92080550/169568086-593e59cd-9bad-4851-b9d7-e5a6c01b3bad.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
![image](https://user-images.githubusercontent.com/92080550/169568218-2fbb8e85-ca92-49b2-a5f8-af3b375d9833.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
![image](https://user-images.githubusercontent.com/92080550/169568317-bcc43c3b-58d5-4c32-bc02-45b94d0b9108.png)


### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
![image](https://user-images.githubusercontent.com/92080550/169568377-cc7879fa-813f-4c82-b5fb-f3fe9585d623.png)


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###
![image](https://user-images.githubusercontent.com/92080550/169568431-27f4ead8-88a8-4dbc-8d5b-77ce1a51b70c.png)



---
