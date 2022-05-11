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

![image](https://user-images.githubusercontent.com/88755456/167910698-6754522d-5278-4174-a5b1-ad03370ccea2.png)
![image](https://user-images.githubusercontent.com/88755456/167913852-29951393-85ca-4337-9acf-892c1dc1c9f2.png)
![image](https://user-images.githubusercontent.com/88755456/167915242-97f4cfe3-5ee9-41dc-8033-4f573c6670bf.png)


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

![image](https://user-images.githubusercontent.com/88755456/167915456-a4f5e94c-c6f6-4c37-ae8f-078427c75b59.png)
![image](https://user-images.githubusercontent.com/88755456/167915969-d5d7841c-b79a-44cc-af1b-77be889f3d76.png)
![image](https://user-images.githubusercontent.com/88755456/167916045-997bc81c-8991-4614-861a-b4d8ffc5542b.png)


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


![image](https://user-images.githubusercontent.com/88755456/167916327-f7b6afb5-a740-45de-92a9-9bc432bb4e36.png)
![image](https://user-images.githubusercontent.com/88755456/167916520-c3ce1346-7c5d-4481-bf32-0afcdb660a62.png)
![image](https://user-images.githubusercontent.com/88755456/167916691-9aba0056-4de7-45c1-91f2-ff5e3de6f437.png)


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

![image](https://user-images.githubusercontent.com/88755456/167916925-7057deef-5e1b-4863-bc1e-0b88b25d2cbc.png)
![image](https://user-images.githubusercontent.com/88755456/167917087-7c5ac6d1-798c-425d-904e-96ed9c691b91.png)
![image](https://user-images.githubusercontent.com/88755456/167917140-c8d522d6-834e-4cfb-afb9-3b88fd2ba3dc.png)

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
![image](https://user-images.githubusercontent.com/88755456/167917786-34a16341-8c6b-4dfa-bc90-31b3f5fbf5a7.png)

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
MotorBoat o-- SteeringWheel
MotorBoat o-- Engine
Car o-- Engine
Car o-- Door
Car o-- Wheel
Car o-- Helm
@enduml 
```
![image](https://user-images.githubusercontent.com/88755456/167917591-967f7234-b0e9-4b6c-b74f-e7c51ea2543d.png)

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
![image](https://user-images.githubusercontent.com/88755456/167917710-568eead7-026f-42ab-8dd8-4920f60705ae.png)

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
![image](https://user-images.githubusercontent.com/88755456/167917888-b9cd4a59-6eb8-4e21-bb1e-52f3f005a6c7.png)

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
![image](https://user-images.githubusercontent.com/88755456/167918098-7369152c-1f1d-4eb6-9227-a7adeb7a5dca.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
``` puml
@startuml 
class Bank_Account{
    - Bank 
    - Name
    - interest
    # debt
    + deposit()
    + withdraw()
}
class Savings_Account{
    + Pay_utility_bills()
}
class Current_Account{
    Fee
    + daily_check()
}
Bank_Account <|-- Savings_Account
Bank_Account <|-- Current_Account
@enduml
```
![image](https://user-images.githubusercontent.com/88755456/167918286-d421a71a-3a33-4b1a-a2bb-d1e59e08b087.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
``` puml
@startuml
class employee {
    # salary
    - work
    + take_leave()
}
class manager {
    - position_allowance
    + work_order()
}
employee <|-- manager
@enduml
```
![image](https://user-images.githubusercontent.com/88755456/167918392-cc9a675a-267c-4324-8c39-570ffba4d73d.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
``` puml
@startuml
class CD_Player_Music{
    - Brand
    - CD_slots
    + Play_Music()
}
class Video_Player_Music{
    - Brand
    + Player_Video()
}
class CD_Player{ }

CD_Player_Music <|-- CD_Player
Video_Player_Music <|-- CD_Player
@enduml
```
![image](https://user-images.githubusercontent.com/88755456/167918470-9d861dc3-8732-4f42-8a3b-821f600d7119.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###
``` puml
@startuml
class Mother{ }
class Have{ }
class Son{ }

Mother "1..1" -- Have
Have -- "0..n" Son
@enduml
```
![image](https://user-images.githubusercontent.com/88755456/167918584-72515ef0-25a4-4d18-a546-4302e3c1d263.png)

---
