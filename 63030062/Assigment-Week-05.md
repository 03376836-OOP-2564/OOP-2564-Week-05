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
![Slide19](./im/slide_19.png)

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
![Slide20](./im/slide_20.png)

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
![Slide21](./im/slide_21.png)

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

![Slide22](./im/slide_22.png)
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
```
![Slide44](./im/slide_44.png)

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
![Slide45](./im/slide_45.png)
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
![Slide51](./im/slide_51.png)
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
Book <|-- "2..2" Cover
' Todo: ทำให้สมบูรณ์

@enduml 
```
![Slide54](./im/slide_54.png)
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
Code  

@startuml 

class Book {  
    - ISBN   
    - Name  
    + Read()  
    + Print()  
}

Class Cover {  
    - CoverType  
    + Flip()  
}

Class Introduction {  
    - CoverTypeTextMessage  
    - AuthorName  
    + Read()  
}

Class Index {  
    - TextMessage  
    + Read()  
}

Class Chapter {  
    - ContentChapter  
    + Read()  
}

Class Bibligraphy {
    - TextMessage  
    + Read()  
}

Class Page {  
    - ContentofPage  
    + Filp()  
    + Read()  
}

Class Picture {  
    - Image  
    + See()  
}

Class Font {  
    - Charater  
    + Spell()  
}

Book o-- Cover  
Book o-- Introduction  
Book o-- Index  
Book o-- Chapter  
Book o-- Bibligraphy  
Chapter o-- Page  
Page o-- Picture  
Page o-- Font  

@enduml 
![Slide56](./im/slide_56.png)

### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
![Slide71](./im/slide_71.png)

### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
![Slide76](./im/slide_76.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
![Slide78](./im/slide_78.png)

### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###
![Slide95](./im/slide_95.png)

---