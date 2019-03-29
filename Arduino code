#include<Servo.h>
Servo s1z;
Servo s2z;
Servo s1y;
Servo s2y;
Servo s3z;
Servo s3y;
Servo s4z;
Servo s4y;
Servo s5z;
Servo s5y;
Servo s6z;
Servo s6y;
float h = 10.5;
float T = 0.6;
float l = 9.5;
float a = 5;
float b = 4;
float R;

void fwd();
void turn();

void setup() {
  Serial.begin(9600);
  // put your setup code here, to run once:
  s1z.attach(2);
  s2z.attach(4);
  s1y.attach(3);
  s2y.attach(13);//5
  s3z.attach(6);
  s3y.attach(7);
  s4z.attach(8);
  s4y.attach(9);
  s5z.attach(10);
  s5y.attach(11);
  s6z.attach(12);
  s6y.attach(5);//13

  s1y.write(80);
  s1z.write(80);
  s2y.write(70);
  delay(200);
  s2z.write(95);//95
  s3y.write(45);
  s3z.write(75);//75
  s4y.write(115);
  s4z.write(100 );//50
  s5y.write(60 );
  s5z.write(105);
  s6z.write(65);

  
  Serial.begin(9600);
  delay(3000);
  s6y.write(90);
}
void loopm(){
  Serial.print(s1z.read());
  Serial.print("  ");
  Serial.print(s1y.read());
  Serial.print("  ");
  Serial.print(s2z.read());
  Serial.print("  ");
  Serial.print(s2y.read());
  Serial.print("  ");
  Serial.print(s3z.read());
  Serial.print("  ");
  Serial.print(s3y.read());
  Serial.print("  ");
  Serial.print(s4z.read());
  Serial.print("  ");
  Serial.print(s4y.read());
  Serial.print("  ");
  Serial.print(s5z.read());
  Serial.print("  ");
  Serial.print(s5y.read());
  Serial.print("  ");
  Serial.print(s6z.read());
  Serial.print("  ");
  Serial.println(s6y.read());
}

void loop() {

  float t = (((float) millis()) / 1000.00)  ;
  if (((int)floor(t / T)) % 2 == 0)
  {
    float theta1 = 90 - 57.3 * (atan(h / l));

    R = sqrt(h * h + l * l);
    float theta2 = (57.3 * acos((-(b * sin(PI * t / T)) + R * cos(theta1 * PI / 180)) / (R)));
    float alphaz = (theta2 - theta1);
    float B = float((a - a * cos(3.14 * t / T)) / l);
    float alphay = B * 57.3;

    Serial.print("s2z====");
    Serial.println(80 - alphaz);
s1z.write(130);
s5z.write(110);//100
s6z.write(75);//75
 s2z.write(105);
s3z.write(85);
s4z.write(120);
    Serial.print("s2y====");
    Serial.println(alphay + 127);
  // s1y.write((57.3 * 2 * a / l) - alphaz2 + 80 - 30);
//    s2y.write((57.3 * 2 * a / l) - alphay + 60 - 30);
    //s3y.write(alphay + 45 - 30);

    float alphaz2 = 57.3 * ((a - a * cos((3.14 * (t - T)) / T)) / l);
//    s4y.write(115 + alphaz2 - 30);
s1y.write((57.3 * 2 * a / l) - alphaz2 + 70 - 40);//30

 s5y.write(60 + alphaz2 - 30);
 //   s5y.write(60 + (57.3 * 2 * a / l) - alphaz2 - 20);//30
s6y.write(90 + (57.3 * 2 * a / l) - alphaz2 - 50);//30

  }
  else
  {
    float alphaz = 57.3 * ((a - a * cos((3.14 * (t - T)) / T)) / l);

 //s1y.write(80 + (57.3 * 2 * a / l) - alphaz - 30);
//    s2y.write(60 + (57.3 * 2 * a / l) - alphaz - 30);
    //s3y.write(45  + alphaz - 30);

    float theta12 = 28;
    R = sqrt(h * h + l * l);
    float theta22 = (57.3 * acos((-(b * sin(PI * t / T)) + R * cos(theta12 * PI / 180)) / (R)));
    float alphaz2 =( theta22 - theta12);
    float B = float((a - a * cos(3.14 * t / T)) / l);
    float alphay2 = B * 57.3;

    Serial.print("s2z====");
    Serial.println(80 - alphaz2);

//    s4z.write(90 - alphaz2);
s1z.write(80);
    s5z.write(100U);
 s6z.write(55);
    

//    s4y.write(115 + (57.3 * 2 * a / l) - alphay2 - 30);

s1y.write(80 +  alphaz - 45);
    s5y.write(60 + alphay2 - 30);
  s6y.write(90+ alphay2 - 50);

 s2z.write(95);
s3z.write(65);
s4z.write(90);
  }

}

void loopk() {

  float t = (((float) millis()) / 1000.00)  ;
  if (((int)floor(t / T)) % 2 == 0)
  {
    float theta1 = 90 - 57.3 * (atan(h / l));

    R = sqrt(h * h + l * l);
    float theta2 = (57.3 * acos((-(b * sin(PI * t / T)) + R * cos(theta1 * PI / 180)) / (R)));
    float alphaz = (theta2 - theta1);
    float B = float((a - a * cos(3.14 * t / T)) / l);
    float alphay = B * 57.3;

    Serial.print("s2z====");
    Serial.println(80 - alphaz);
s1z.write(100);
s5z.write(92);
s6z.write(45);
 s2z.write(95);
s3z.write(75);

    Serial.print("s2y====");
    Serial.println(alphay + 127);
    
//    s2y.write((57.3 * 2 * a / l) - alphay + 60 - 30);
//    s3y.write(alphay + 45 - 30);

    float alphaz2 = 57.3 * ((a - a * cos((3.14 * (t - T)) / T)) / l);
//    s4y.write(115 + alphaz2 - 30);
s1y.write( alphaz2 + 80 - 30);
    s5y.write(60 +  alphaz2 - 30);
    s6y.write(120 +alphaz2 - 30);

  }
  else
  {
    float alphaz = 57.3 * ((a - a * cos((3.14 * (t - T)) / T)) / l);

    
//    s2y.write(60 + (57.3 * 2 * a / l) - alphaz - 30);
//    s3y.write(45  + alphaz - 30);

    float theta12 = 28;
    R = sqrt(h * h + l * l);
    float theta22 = (57.3 * acos((-(b * sin(PI * t / T)) + R * cos(theta12 * PI / 180)) / (R)));
    float alphaz2 =( theta22 - theta12);
    float B = float((a - a * cos(3.14 * t / T)) / l);
    float alphay2 = B * 57.3;

    Serial.print("s2z====");
    Serial.println(80 - alphaz2);

    s4z.write(90 - alphaz2);
    s5z.write(92-alphaz2);
    s6z.write(65 - alphaz2);
//    
//
//    s4y.write(115 + (57.3 * 2 * a / l) - alphay2 - 30);
s1y.write(80 + alphay2 - 30);
    s5y.write(60 + alphay2 - 30);
    s6y.write(120 + alphay2 - 30);


  }

}
