# beee-project-sem1
BEEE lab projects programming code
const int trigPin=13;
const int echoPin=12;
long duration;
int distance;
#include<LiquidCrystal.h>
LiquidCrystal LCD(11,10,9,2,3,4,5);
#define trigPin 13
#define echoPin 12

void setup() {
  pinMode(trigPin,OUTPUT);
  pinMode(echoPin,INPUT);
  Serial.begin(9600);
  pinMode(trigPin,OUTPUT);
  pinMode(echoPin,INPUT);
  LCD.begin(16,2);
  LCD.print("HEIGHT MEASURE:");
 }

void loop() {
digitalWrite(trigPin,LOW);
delayMicroseconds(2);
digitalWrite(trigPin,HIGH);
delayMicroseconds(10);
digitalWrite(trigPin,LOW);
duration=pulseIn(echoPin,HIGH);
distance=duration*0.034/2;
Serial.print("Distance:");
Serial.println(distance);
long duration,distance;
digitalWrite(trigPin,LOW);
delayMicroseconds(2);
digitalWrite(trigPin,HIGH);
delayMicroseconds(10);
digitalWrite(trigPin,LOW);
duration=pulseIn(echoPin,HIGH);
distance=(duration/2)/29.1;
LCD.setCursor(0,1);
LCD.print(" ");
LCD.setCursor(0,1);
LCD.print(distance);
LCD.print("cm");
delay(250);
 }
