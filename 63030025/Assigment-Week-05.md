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

![image](https://user-images.githubusercontent.com/92078990/167910675-a5d1ebca-b773-449a-9bac-2c66d1657073.png)
![image](https://user-images.githubusercontent.com/92078990/167914288-e5623d5d-3ce4-4a5a-8d66-7fe3df5a5718.png)
![image](https://user-images.githubusercontent.com/92078990/167916780-5e479aef-f58b-4667-b440-f7b77e4c14bd.png)

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

![image](https://user-images.githubusercontent.com/92078990/167916998-c99bde8d-064f-4c47-bc27-aecf216928d4.png)
![image](https://user-images.githubusercontent.com/92078990/167917122-7cdffeb0-a268-4a75-b6fd-b802f414fa42.png)
![image](https://user-images.githubusercontent.com/92078990/167918414-018197ab-a66b-4dde-b414-e66f0d9313b8.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้


#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสคือการทำ Inheritance ####

``` puml
@startuml 
"Base class" <|-- "Derived class"
@enduml 
```

![image](https://user-images.githubusercontent.com/92078990/167917599-30a9603a-db36-49b7-809b-47a0b5eef7fc.png)g)
![image](https://user-images.githubusercontent.com/92078990/167917841-072f5dde-6e7c-484e-90c7-b53c3e553f69.png)
![image](https://user-images.githubusercontent.com/92078990/167918065-fcae4794-2326-49e5-9599-eafc76b26b4a.png)



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


![image](https://user-images.githubusercontent.com/92078990/167918741-41f5ccfc-4752-4215-8924-4ff2e605162d.png)

^^^ บันทึกผลของนักศึกษาลงไปแทนภาพนี้

#### หมายเหตุ การใช้ลูกศรสามเหลี่ยมที่มีหัวโปร่งใสและเส้นประคือการทำ Instantiation (สร้างวัตถุ) ####


``` puml
@startuml 
"Base class" <|.. "Derived class"
@enduml 
```
![image](https://user-images.githubusercontent.com/92078990/167919409-9de635dc-d085-48e4-8b58-f7ef3bbf285b.png)
![image](https://user-images.githubusercontent.com/92078990/167919262-8d4e0663-acf7-4041-9218-8e1ab607a2b7.png)
![image](https://user-images.githubusercontent.com/92078990/167919481-921573d2-b1f1-4f56-bb88-15de4814d30e.png)


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
![image](https://user-images.githubusercontent.com/92078990/167919809-7a61bdff-04ff-4fe0-982f-e93b0784c282.png)
![image](https://user-images.githubusercontent.com/92078990/167919957-79f7ffec-e373-4d04-a992-d91010d52c3b.png)
![image](https://user-images.githubusercontent.com/92078990/167920018-d5198831-b9e1-44e7-9e10-ebbf5238ca3b.png)


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
' Todo: ทำให้สมบูรณ์


@enduml 
![image](https://user-images.githubusercontent.com/92078990/167920699-f95ec164-7571-4864-9214-7d1e260d9414.png)
``

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
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92078990/167920761-63c93ec6-423a-4f9b-b5de-57b0a2a40cb7.png)

### 2.3 สไลด์หมายเลข 51 ###

``` puml
@startuml 

class Car{}
class Engine{}
class Wheel{}
class AirConditionner{}

Car <|-- "1..1" Engine
Car <|-- "2..4" Door
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92078990/167920803-469080b6-05d3-498d-b852-02538e6237fe.png)

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

![image](https://user-images.githubusercontent.com/92078990/167920886-ce0763b5-b051-48c0-9643-43aeacb804d6.png)



### 2.4 Aggregation ของคลาส หนังสือ  (สไลด์หมายเลข 54) ###

``` puml
@startuml 

class Book{}
class Cover{}
Book <|-- "2..2" Cover
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92078990/167920934-367e99b4-79e2-4e85-ac35-e2620bc62782.png)


### 2.5 เพิ่ม Attribute และ Method ให้กับ Class หนังสือ   (สไลด์หมายเลข 56) ###

``` puml
@startuml 

class Book{
    - ISBN 
    - Name
    + Read()
    + Print()
}
 
' Todo: ทำให้สมบูรณ์

@enduml 
```
![image](https://user-images.githubusercontent.com/92078990/167921023-e0c1adc7-f5d2-4709-92c2-ee581fb4f46b.png)


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
![image](https://user-images.githubusercontent.com/92078990/167921173-35bbcbb0-3b53-4a09-bc02-29a4900325be.png)


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
![image](https://user-images.githubusercontent.com/92078990/167921220-21cd2a84-0aee-455c-b31b-3c8c844bde66.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
![image](https://user-images.githubusercontent.com/92078990/167921269-d6c127fc-2a36-4ca1-a7dc-c4c170cbdaee.png)


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###

![image](https://user-images.githubusercontent.com/92078990/167921300-f4f21278-07f3-4fae-9c91-102be1c60cbe.png)

---
