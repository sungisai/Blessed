# Blessed
Robot Typing On Keyboard
#include <Braccio.h>
#include <Servo.h>
 
 
Servo base;
Servo shoulder;
Servo elbow;
Servo wrist_rot;
Servo wrist_ver;
Servo gripper;
const int OUT_PIN = 8;
const int SAMPLE_TIME = 800;
unsigned long millisCurrent;
unsigned long millisLast = 0;
unsigned long millisElapsed = 0;
int count = 0;

int sampleBufferValue = 0;

void setup() {
  Serial.begin(9600);
  Braccio.begin();
}

void loop() {

  millisCurrent = millis();
  millisElapsed = millisCurrent - millisLast;

  if (digitalRead(OUT_PIN) == LOW) {
    sampleBufferValue++;
  }

if (count == 0) {
  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //DEAR
//Press the letter D
  Braccio.ServoMovement(20,           98,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 8,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);
 
  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
 
  //Press the letter R
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);
 
  //Press the Space Bar
  Braccio.ServoMovement(20,           132,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 30, 0,  90,  10);


  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
}
else if (count == 1) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//PROFESSOR
//Type the word "Professor"

  //Press the letter P
  Braccio.ServoMovement(20,           135,  90, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           135,  90, 0, 30,  90,  10);
  Braccio.ServoMovement(20,           135,  90, 30, 30,  90,  10);

  //Press the letter R
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);

  //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

  //Press the letter F
  Braccio.ServoMovement(20,           95,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           95,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           95,  90, 30, 8,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

  //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter O
  Braccio.ServoMovement(20,           132,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 30, 25,  90,  10);

  //Press the letter R
  Braccio.ServoMovement(20,           90,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           90,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           90,  90, 30, 15,  90,  10);

  //Press the Space Bae
  Braccio.ServoMovement(20,           128,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 0,  90,  10);

count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 2) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//PROTON
//Type the word Proton
   //Press the letter P
  Braccio.ServoMovement(20,           135,  85, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           135,  85, 0, 30,  90,  10);
  Braccio.ServoMovement(20,           135,  85, 30, 30,  90,  10);

  //Press the letter R
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);

  //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

  //Press the letter T
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);

  //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

  //Press the letter N
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 0, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);

count++;


    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 3) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);

count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 4) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);

count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 5) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 6) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 7) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 8) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Delete keypad 6 Times
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 8, 30,  90,  10);
  Braccio.ServoMovement(20,           142,  70, 30, 30,  90,  10);
count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 9) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//Press the letter F
  //Type the word Becker
   //Press the letter B
  Braccio.ServoMovement(20,           117,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           117,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           117,  90, 30, 2,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

  //Press the letter C
  Braccio.ServoMovement(20,           97,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 30, 2,  90,  10);

  //Press the letter K
  Braccio.ServoMovement(20,           133,  90, 30, 18,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 18,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 18,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

   //Press the letter R
  Braccio.ServoMovement(20,           121,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);

  //Press the Comma
  Braccio.ServoMovement(20,           138,  90, 30, 11,  90,  10);
  Braccio.ServoMovement(20,           138,  90, 0, 11,  90,  10);
  Braccio.ServoMovement(20,           138,  90, 30, 11,  90,  10);
  count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 10) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Enter key
  Braccio.ServoMovement(20,           150,  75, 30, 27,  90,  10);
  Braccio.ServoMovement(20,           150,  75, 0, 27,  90,  10);
  Braccio.ServoMovement(20,           150,  75 , 30, 27,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 11) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//THANK

  //Press the letter T
  Braccio.ServoMovement(20,           108,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           108,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           108,  90, 30, 15,  90,  10);

   //Press the letter H
  Braccio.ServoMovement(20,           118,  90, 30, 12,  90,  10);
  Braccio.ServoMovement(20,           118,  90, 0, 12,  90,  10);
  Braccio.ServoMovement(20,           118,  90, 30, 12,  90,  10);

  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
 
  //Press the letter N
  Braccio.ServoMovement(20,           123,  90, 30, 3,  90,  10);
  Braccio.ServoMovement(20,           123,  90, 0, 3,  90,  10);
  Braccio.ServoMovement(20,           123,  90, 30, 3,  90,  10);

  //Press the letter K
  Braccio.ServoMovement(20,           132,  90, 30, 18,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 0, 18,  90,  10);
  Braccio.ServoMovement(20,           132,  90, 30, 18,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 12) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//type the word "you"
    //Press the letter Y
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);

   //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

    //Press the letter U
  Braccio.ServoMovement(20,           140,  90, 30, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 30, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 0, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 30, 20,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 13) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//type the word "for"
  //Press the letter F
  Braccio.ServoMovement(20,           102,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           102,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           102,  90, 30, 8,  90,  10);
   
   //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

    //Press the letter R
  Braccio.ServoMovement(20,           138,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 15,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;
    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 14) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

//Press the letter T
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);

  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);

  //Press the letter C
  Braccio.ServoMovement(20,           138,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 2,  90,  10);

  //Press the letter H
  Braccio.ServoMovement(20,           120,  90, 30, 12,  90,  10);
  Braccio.ServoMovement(20,           120,  90, 0, 12,  90,  10);
  Braccio.ServoMovement(20,           120,  90, 30, 12,  90,  10);

  //Press the letter I
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);

  //Press the letter N
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 0, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);

   //Press the letter G
  Braccio.ServoMovement(20,           111,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           111,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           111,  90, 30, 8,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 15) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //type the word "robotics"
   //Press the letter R
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);

   //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

  //Press the letter B
  Braccio.ServoMovement(20,           106,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           106,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           106,  90, 30, 2,  90,  10);

   //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

//Press the letter T
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);

  //Press the letter I
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);

  //Press the letter C
  Braccio.ServoMovement(20,           138,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           91,  90, 30, 2,  90,  10);

  //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 16) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

  //type the word "this"
//Press the letter T
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);

 //Press the letter H
  Braccio.ServoMovement(20,           120,  90, 30, 12,  90,  10);
  Braccio.ServoMovement(20,           120,  90, 0, 12,  90,  10);
  Braccio.ServoMovement(20,           120,  90, 30, 12,  90,  10);

  //Press the letter I
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);

   //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 17) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //type the word "semester"

 //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

   //Press the letter M
  Braccio.ServoMovement(20,           134,  90, 30, 11,  90,  10);
  Braccio.ServoMovement(20,           134,  90, 0, 11,  90,  10);
  Braccio.ServoMovement(20,           134,  90, 30, 11,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

  //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter T
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 15,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           97,  90, 30, 15,  90,  10);

  //Press the letter R
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           103,  90, 30, 15,  90,  10);

  //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 18) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //type the word "yours"
    //Press the letter Y
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);

   //Press the letter O
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 0, 25,  90,  10);
  Braccio.ServoMovement(20,           133,  90, 30, 25,  90,  10);

    //Press the letter U
  Braccio.ServoMovement(20,           140,  90, 30, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 30, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 0, 20,  90,  10);
  Braccio.ServoMovement(20,           112,  90, 30, 20,  90,  10);

   //Press the letter R
  Braccio.ServoMovement(20,           90,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           90,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           90,  90, 30, 15,  90,  10);

   //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 19) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the Enter key
  Braccio.ServoMovement(20,           150,  75, 30, 27,  90,  10);
  Braccio.ServoMovement(20,           150,  75, 0, 27,  90,  10);
  Braccio.ServoMovement(20,           150,  75 , 30, 27,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 20) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

 //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);

   //Press the letter M
  Braccio.ServoMovement(20,           134,  90, 30, 11,  90,  10);
  Braccio.ServoMovement(20,           134,  90, 0, 11,  90,  10);
  Braccio.ServoMovement(20,           134,  90, 30, 11,  90,  10);

  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);

   //Press the letter N
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 0, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);

   //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 21) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

  //Press the letter I
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);

  //Press the letter F
  Braccio.ServoMovement(20,           102,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           102,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           102,  90, 30, 8,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

  //Press the letter A
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           71,  90, 30, 8,  90,  10);

   //Press the letter N
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 0, 6,  90,  10);
  Braccio.ServoMovement(20,           113,  90, 30, 6,  90,  10);

   //Press the letter Y
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           115,  90, 30, 15,  90,  10);

  //Press the letter I
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           128,  90, 30, 23,  90,  10);

   //Press the Space Bar
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 0, 0,  90,  10);
  Braccio.ServoMovement(20,           129,  90, 30, 0,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
else if (count == 22) {

  if (millisElapsed > SAMPLE_TIME ){
    Serial.println(sampleBufferValue);
   
    if (abs(sampleBufferValue)<7000 && (sampleBufferValue >2000)){
    Serial.println("Dear ");
    Serial.println(sampleBufferValue);
    Braccio.ServoMovement(20,           0,  90, 90, 90,  90,  10);

  //type the word "saman "
 
   //Press the letter B
  Braccio.ServoMovement(20,           117,  90, 30, 2,  90,  10);
  Braccio.ServoMovement(20,           117,  90, 0, 2,  90,  10);
  Braccio.ServoMovement(20,           117,  90, 30, 2,  90,  10);

   //Press the letter L
  Braccio.ServoMovement(20,           137,  90, 30, 23,  90,  10);
  Braccio.ServoMovement(20,           137,  90, 0, 23,  90,  10);
  Braccio.ServoMovement(20,           137,  90, 30, 23,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

   //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
   //Press the letter S
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 0, 9,  90,  10);
  Braccio.ServoMovement(20,           78,  90, 30, 9,  90,  10);

  //Press the letter E
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 0, 15,  90,  10);
  Braccio.ServoMovement(20,           84,  90, 30, 15,  90,  10);

  //Press the letter D
  Braccio.ServoMovement(20,           98,  90, 30, 8,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 0, 8,  90,  10);
  Braccio.ServoMovement(20,           98,  90, 30, 8,  90,  10);
  count++;

    }
    
   
    sampleBufferValue = 0;
    millisLast = millisCurrent;


  }
  
}
}
