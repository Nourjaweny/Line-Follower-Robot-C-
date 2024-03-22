# Line-Follower-Robot-C-
This is a C++ code for a Line Following Robot using Arduino


#include <Arduino.h>
int ENABLE_1_PIN=3;   // This should be a pwm (~) pin
int MOTOR_1_INPUT_1=9;     
int MOTOR_1_INPUT_2=4;
int MOTOR_2_INPUT_1=7;
int MOTOR_2_INPUT_2=8;
int ENABLE_2_PIN=5;      // This should be a pwm (~) pin
int sensorF=12;  
int F ;
int sensorR=11;  
int R ;
int sensorL=2;  
int L ;
int sensorG=1;  
int G ;
int sensorD=12;  
int D ;
int k=0;


int MAX_MOTOR_SPEED=200 ;
int SLOW_MOTOR_SPEED=80;
int NORMAL_MOTOR_SPEED=120;




void setup() {
  pinMode(MOTOR_1_INPUT_1, OUTPUT);       // DEFINE
  pinMode(MOTOR_1_INPUT_2, OUTPUT);       // MOTOR
  pinMode(MOTOR_2_INPUT_1, OUTPUT);       // DRIVER
  pinMode(MOTOR_2_INPUT_2, OUTPUT);       // PINS
  pinMode(ENABLE_1_PIN, OUTPUT);          // AS
  pinMode(ENABLE_2_PIN, OUTPUT);          // OUTPUT
pinMode(sensorF,INPUT); // Set the pin 'sensor'(9) to INPUT Mode; our Arduino will receive data from the sensor, hence this pin should be input
pinMode(sensorR,INPUT);
pinMode(sensorL,INPUT);
pinMode(sensorD,INPUT);
pinMode(sensorG,INPUT);
Serial.begin(9600);
  
forward(NORMAL_MOTOR_SPEED);
  delay (500);
}

void forward(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}

void reverse(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed ); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, HIGH);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, HIGH);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}

void sharpright(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed+50); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, HIGH);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}
void left(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}

void sharpleft(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, HIGH);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}
void right(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}
void stopBot(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}




  
void loop() {
  F=digitalRead(sensorF);
  R=digitalRead(sensorR);
  L=digitalRead(sensorL);
  D=digitalRead(sensorD);
  G=digitalRead(sensorG);
  Serial.print(L);Serial.print(F);Serial.print(R);Serial.print(D);

  
  #include <Arduino.h>
int ENABLE_1_PIN=3;   // This should be a pwm (~) pin
int MOTOR_1_INPUT_1=9;     
int MOTOR_1_INPUT_2=4;
int MOTOR_2_INPUT_1=7;
int MOTOR_2_INPUT_2=8;
int ENABLE_2_PIN=5;      // This should be a pwm (~) pin
int sensorF=12;  
int F ;
int sensorR=11;  
int R ;
int sensorL=2;  
int L ;
int sensorG=1;  
int G ;
int sensorD=12;  
int D ;
int k=0;


int MAX_MOTOR_SPEED=200 ;
int SLOW_MOTOR_SPEED=80;
int NORMAL_MOTOR_SPEED=120;




void setup() {
  pinMode(MOTOR_1_INPUT_1, OUTPUT);       // DEFINE
  pinMode(MOTOR_1_INPUT_2, OUTPUT);       // MOTOR
  pinMode(MOTOR_2_INPUT_1, OUTPUT);       // DRIVER
  pinMode(MOTOR_2_INPUT_2, OUTPUT);       // PINS
  pinMode(ENABLE_1_PIN, OUTPUT);          // AS
  pinMode(ENABLE_2_PIN, OUTPUT);          // OUTPUT
pinMode(sensorF,INPUT); // Set the pin 'sensor'(9) to INPUT Mode; our Arduino will receive data from the sensor, hence this pin should be input
pinMode(sensorR,INPUT);
pinMode(sensorL,INPUT);
pinMode(sensorD,INPUT);
pinMode(sensorG,INPUT);
Serial.begin(9600);
  
forward(NORMAL_MOTOR_SPEED);
  delay (500);
}

void forward(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}

void reverse(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed ); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, HIGH);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, HIGH);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}

void sharpright(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed+50); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, HIGH);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}
void left(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, HIGH);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}

void sharpleft(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, HIGH);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}
void right(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, HIGH);
}
void stopBot(uint8_t speed){
  analogWrite(ENABLE_1_PIN, speed); //Left Motor Speed
  analogWrite(ENABLE_2_PIN, speed); //Right Motor Speed
  digitalWrite(MOTOR_1_INPUT_1, LOW);
  digitalWrite(MOTOR_1_INPUT_2, LOW);
  digitalWrite(MOTOR_2_INPUT_1, LOW);
  digitalWrite(MOTOR_2_INPUT_2, LOW);
}




  
void loop() {
  F=digitalRead(sensorF);
  R=digitalRead(sensorR);
  L=digitalRead(sensorL);
  D=digitalRead(sensorD);
  G=digitalRead(sensorG);
  Serial.print(L);Serial.print(F);Serial.print(R);Serial.print(D);

  
  if((L==1) && (F==0) && (R==1) )//or (L==0) && (F==1) && (R==0))
  {
    forward(NORMAL_MOTOR_SPEED);
  }
   
   
   if ((L==0) && (F==1) && (R==1))
  {
    left(NORMAL_MOTOR_SPEED);
    delay(150);
    
    
  } 
  if ((L==0) && (F==0) && (R==1))
  { stopBot(NORMAL_MOTOR_SPEED);
  delay(100);
     left(NORMAL_MOTOR_SPEED);
    delay(150);}
    
  if ((L==1) && (F==0) && (R==0))
  {
    right(NORMAL_MOTOR_SPEED);
    delay(150);
    }
   
   if ((L==1) && (F==1) && (R==0))
  {
    right(NORMAL_MOTOR_SPEED);
    delay(150);}
  if ((D==0) && (L==0) && (F==0) && (R==0))
  {
    left(NORMAL_MOTOR_SPEED);
    
    delay(300);}
  
  
  if ((D==1) && (L==0) && (F==0) && (R==0))
  {
    stopBot(NORMAL_MOTOR_SPEED);
    
    delay(700);}

    if ((D==1) && (L==1) && (F==1) && (R==0))
  {
    left(NORMAL_MOTOR_SPEED);
    
    delay(100);}
    
  if ((D==1) && (L==1) && (F==1) && (R==1))
  {
    right(NORMAL_MOTOR_SPEED);
    
    delay(50);}
      /*unsigned long currentMillis1 = millis();
  if((L==0) && (F==0) && (R==1)&&(D==0) && (millis() >= 50700) && ((millis() <= 60000)))
  {
   left(NORMAL_MOTOR_SPEED);}*/

  unsigned long currentMillis = millis();
  if((L==0) && (F==0) && (R==0)&&(D==0) && (millis() >= 39000))
  {
    forward(NORMAL_MOTOR_SPEED);}
if ((D==1) && (L==0) && (F==1) && (R==0))
  {
    right(NORMAL_MOTOR_SPEED);
    
    delay(300);}} )//or (L==0) && (F==1) && (R==0))
  {
    forward(NORMAL_MOTOR_SPEED);
  }
   
   
   if ((L==0) && (F==1) && (R==1))
  {
    left(NORMAL_MOTOR_SPEED);
    delay(150);
    
    
  } 
  if ((L==0) && (F==0) && (R==1))
  { stopBot(NORMAL_MOTOR_SPEED);
  delay(100);
     left(NORMAL_MOTOR_SPEED);
    delay(150);}
    
  if ((L==1) && (F==0) && (R==0))
  {
    right(NORMAL_MOTOR_SPEED);
    delay(150);
    }
