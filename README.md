# ** **BOBOBIN** **
ถึงขยะที่ช่วยลดการสัมผัสในการทิ้งขยะ เป็นโครงงานของวิชาPhysical Computing ภาคเรียนที่1ปี2023

## บทคัดย่อ
> * โครงงาน BOBOBIN เป็นโปรเจคถังขยะเปิดเองอัตโนมัติที่พัมนาโดยภาษา C รวมถึงได้ใช้ทักษะกรต่อวงจรจากวิชา Physical Computing มาใช้พัฒนา
## วัตถุประสงค์
> * เพื่อลดการสัมผัสกับถังขยะในการทิ้งขยะ
> * เพื่อศึกษาและพัฒนาการต่อวงจร Arduino
> * เพื่อนำความรู้ภาษา C มาประยุกต์ใช้
## ข้อดี
> * ลดการสัมผัสกับถังขยะ
> * เพิ่มความสะดวกสบาย

## อุปกรณ์
> * ถังขยะ
> * breadboard
> * arduno uno
> * ultrasonic module
> * สายไฟ
> * Sg90 Micro Servo Motor
## โปสเตอร์
![Magic Bin (2)](https://github.com/Bobby715623/ProjectPhyCom/assets/118421368/79b120cc-8bc7-4720-a0d7-8caf18308ca8)



## ชิ้นงาน
![369583041_261374433132971_3270649359921496871_n](https://github.com/Bobby715623/ProjectPhyCom/assets/118421368/a93f7a47-a5fe-42cd-b357-111fd539471c)

## code สำหรับชิ้นงาน
```
#include <Servo.h>   //servo library
Servo sg90;  
int echo = 7;   
int trig = 6;    
int servopin = 8;
int distance;
int duration;



void setup() {       
    sg90.attach(8);
    pinMode(trig, OUTPUT);  
    pinMode(echo, INPUT);  
  
} 


void loop() {
  digitalWrite(trig,0);
  delay(2);
  digitalWrite(trig,1);
  delayMicroseconds(10);
  digitalWrite(trig,0); 
  duration = pulseIn(echo,1);
  distance = duration*0.034/2;

  
if ( distance<30 ) {   
 sg90.write(180);    
 delay(4500);//ระยะของServo
 Serial.print(distance);
}
 else{
  sg90.write(0);
  delay(50);
 }
```

## วิดิโอนำเสนอชิ้นงาน
https://youtu.be/KFZJvuxd8Zw

## Members
| Student ID | ชื่อ - นามสกุล |
| :--------  | :-------- |
|   65070114 |   นพรุจ บุญประสิทธิผล |
|   65070139 |   ปิยธานี ศรีทอง   |
|   65070141 |   ไผทมาศ มาดไทย  |]

