# Smart-traffic-control
#Automatic accident prevention By Smart Traffic control
#include <Servo.h> 

Servo myservo1;
 Servo myservo2;
 Servo myservo3;
 Servo myservo4;
 Servo myservo5; 
Servo myservo6;

 #define r1 2
 #define g1 3 

#define r2 4
 #define g2 5

 #define r3 6
 #define g3 7

 int pos = 0;

 void setup()
 {
 Serial.begin(9600);
 pinMode(r1, OUTPUT); 
pinMode(g1, OUTPUT); 
pinMode(r2, OUTPUT); 
pinMode(g2, OUTPUT);
 pinMode(r3, OUTPUT); 
pinMode(g3, OUTPUT);

 digitalWrite(r1, LOW);
 digitalWrite(g1, LOW); 
digitalWrite(r2, LOW); 
digitalWrite(g2, LOW);
 digitalWrite(r3, LOW); 
digitalWrite(g3, LOW);

 myservo1.attach(8); 
myservo2.attach(9); 
myservo3.attach(10); 
myservo4.attach(11);
 myservo5.attach(12);
 myservo6.attach(13);

 delay(50); 
digitalWrite(r1, HIGH);
 digitalWrite(r2, HIGH);
 digitalWrite(r3, HIGH);
 delay(1000);

 } 
void loop()
 {
 digitalWrite(r2, LOW);
 digitalWrite(r3, LOW); 
digitalWrite(g2, HIGH); 
digitalWrite(g3, HIGH);

 for (pos =50; pos >=0; pos -= 1)
          { // goes from 0 degrees to 90 degrees
           // in steps of 1 degree
             myservo3.write(pos);                                                                 // tell servo to go to position in variable 'pos' 
                    delay(15);
 } 
for (pos = 50; pos >=0; pos -= 1)
           { // goes from 0 degrees to 90 degrees
            // in steps of 1 degree
              myservo4.write(pos);                                                                 // tell servo to go to position in variable 'pos'
                    delay(15); 
} 
for (pos = 0; pos <= 50; pos += 1)
            { // goes from 90 degrees to 0 degrees
                myservo1.write(pos);                                                              // tell servo to go to position in variable 'pos'
                    delay(15);
 }
 for (pos = 0; pos <= 50; pos += 1)
             { // goes from 90 degrees to 0 degrees
                myservo2.write(pos);                                                                 // tell servo to go to position in variable 'pos' 
                    delay(15);
 }
 for (pos = 0; pos <= 50; pos += 1)
              { // goes from 90 degrees to 0 degrees
                myservo5.write(pos);                                                                 // tell servo to go to position in variable 'pos'
                     delay(15);
 } 
for (pos = 0; pos <= 50; pos += 1)
                 { // goes from 90 degrees to 0 degrees
                  myservo6.write(pos);                                                                 // tell servo to go to position in variable 'pos'
 delay(15);

 }

 delay(5000);
 digitalWrite(g2, LOW); 
digitalWrite(g3, LOW);
 digitalWrite(r2, HIGH);
 digitalWrite(r3, HIGH); 
delay(1000); 
digitalWrite(r1, LOW);
 digitalWrite(g1, HIGH); 
for (pos = 0; pos <= 50; pos += 1)
        { // goes from 90 degrees to 0 degrees 
         myservo5.write(pos);                                                                  // tell servo to go to position in variable 'pos'
             delay(15);
 }
 for (pos = 0; pos <= 50; pos += 1)
          { // goes from 90 degrees to 0 degrees
          myservo4.write(pos);                                                                 // tell servo to go to position in variable 'pos'
            delay(15);
 }
 for (pos = 0; pos <= 50; pos += 1)
           { // goes from 90 degrees to 0 degrees
          myservo1.write(pos);                                                                  // tell servo to go to position in variable 'pos'
            delay(15);
 }
 for (pos = 50; pos >= 0; pos -= 1)
            { // goes from 0 degrees to 90 degrees
            // in steps of 1 degree
           myservo2.write(pos);                                                                    // tell servo to go to position in variable 'pos' 
            delay(15);
 
}
for (pos = 50; pos >= 0; pos -= 1)
            { // goes from 0 degrees to 90 degrees
             // in steps of 1 degree
            myservo3.write(pos);                                                                   // tell servo to go to position in variable 'pos' 
            delay(15);
 }
for (pos = 50; pos >= 0; pos -= 1)
            { // goes from 0 degrees to 90 degrees
            // in steps of 1 degree
          myservo6.write(pos);                                                                // tell servo to go to position in variable 'pos'
           delay(15);
 }
 delay(5000);
 digitalWrite(g1, LOW);
 digitalWrite(r1, HIGH); 
delay(1000); 
digitalWrite(r3, LOW);
 digitalWrite(r2, LOW); 
digitalWrite(g3, HIGH); 
digitalWrite(g2, HIGH);
 for (pos = 0; pos <= 50; pos += 1)
         { // goes from 90 degrees to 0 degrees
         myservo2.write(pos);                                                                  // tell servo to go to position in variable 'pos'
           delay(15);
 } 
for (pos = 0; pos <= 50; pos += 1)
            { // goes from 90 degrees to 0 degrees 
          myservo3.write(pos);                                                                // tell servo to go to position in variable 'pos'
 delay(15);
 
} 
for (pos = 0; pos <= 50; pos += 1)
              { // goes from 90 degrees to 0 degrees 
                 myservo6.write(pos);                                                               // tell servo to go to position in variable 'pos'
              delay(15);
 } 
for (pos = 50; pos >= 0; pos -= 1)
              { // goes from 0 degrees to 90 degrees 
            // in steps of 1 degree myservo5.write(pos);                              // tell servo to go to position in variable 'pos' 
               delay(15);
 
}
for (pos = 50; pos >= 0; pos -= 1)
         { // goes from 0 degrees to 90 degrees 
          // in steps of 1 degree myservo4.write(pos);                                 // tell servo to go to position in variable 'pos'
             delay(15); 
}
for (pos = 50; pos >= 0; pos -= 1)
          { // goes from 0 degrees to 90 degrees 
          // in steps of 1 degree 
          myservo1.write(pos);                                                                      // tell servo to go to position in variable 'pos'
 delay(15);

 }
 delay(5000); }

