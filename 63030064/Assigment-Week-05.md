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

![image](https://user-images.githubusercontent.com/92082453/167914538-af03cc77-ff2b-4005-b519-e45fc0a8eec9.png)
![image](https://user-images.githubusercontent.com/92082453/167914571-89f98acc-d212-41c0-86f6-bbce9e6c32ab.png)
![image](https://user-images.githubusercontent.com/92082453/167914804-3ef23a3a-09a3-43b4-9792-3352bd4bbf9e.png)


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

![image](https://user-images.githubusercontent.com/92082453/167914933-53f1df3e-f271-4ad0-8abf-74f2da9923d8.png)
![image](https://user-images.githubusercontent.com/92082453/167915164-985ddd65-c669-4387-bf00-db89d22ab618.png)
![image](https://user-images.githubusercontent.com/92082453/167915728-2ab5dfa5-6617-483d-8a20-a260a26f8288.png)


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

![image](https://user-images.githubusercontent.com/92082453/167915911-a3a5cb52-3821-4211-81db-e219727255c0.png)
![image](https://user-images.githubusercontent.com/92082453/167916060-c9d837b7-ad5d-42cb-bffd-174a25fa160f.png)
![image](https://user-images.githubusercontent.com/92082453/167916096-fe7b40c2-52cb-456b-8ba3-dc4301a4f3ef.png)


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
![image](https://user-images.githubusercontent.com/92082453/167916354-6f93015a-bc73-4b34-ac42-71770d4b1eb4.png)
![image](https://user-images.githubusercontent.com/92082453/167916553-e8965f52-cd3b-490a-a81d-d19a4f7eb94e.png)
![image](https://user-images.githubusercontent.com/92082453/167916662-6daefc80-91a8-441a-adbb-d9ecefad60aa.png)



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
![image](https://user-images.githubusercontent.com/92082453/167917143-f3cd722d-8819-449b-9576-1f56b04fc8f3.png)

@enduml 
```

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
![image](https://user-images.githubusercontent.com/92082453/167917237-019ca630-67f2-490b-af4d-3be2f5aa6f60.png)

@enduml 
```

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
![image](https://user-images.githubusercontent.com/92082453/167917529-12949f29-aada-4c4d-9f12-f9ad49db6122.png)


@enduml 
```

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
![image](https://user-images.githubusercontent.com/92082453/167917612-afdfc7a0-f4aa-4d44-9dba-2d23d905c0ae.png)

@enduml 
```

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
![image](https://user-images.githubusercontent.com/92082453/167917709-44a21c03-aeda-4dc2-8530-80bcdd2c46b6.png)

@enduml 
```


### 2.6 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 71 ###
![image](https://user-images.githubusercontent.com/92082453/167917803-199bf17d-1a1f-4c39-bc69-04c5ec22b270.png)


### 2.7 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 76 ###
![image](https://user-images.githubusercontent.com/92082453/167917843-deaa4304-a462-41e2-a0ed-937022f77de4.png)

### 2.8 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 78 ###
![image](https://user-images.githubusercontent.com/92082453/167917891-643ba133-47fd-49fb-a2b3-b178a6069344.png)


### 2.9 ใช้ plantUML วาดภาพตาม สไลด์หมายเลข 95 ###
![image](https://user-images.githubusercontent.com/92082453/167917942-f92b7c4f-3283-4de7-b819-a9300de0730f.png)


---
