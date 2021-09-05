## Kerala IoT Challenge

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies** in Kerala is launching our prestigious program  **“Kerala IoT Challenge 2021”**,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### About Me
> Hello Folks! I'm [**Arjun Krishna**](http://arjunkrishna.in/). I'm a Post Graduation Student in Computer Applications (MCA) from [**Kristu Jyoti College of Management and Technology**](http://www.kristujyoticollege.com), Changanacherry. I have been exploring the world of IoT since my graduation life started. My life around IoT started to change when I got unrestricted access to the Mini IoT Lab that we setup at our [**Inovus Labs IEDC**](https://inovus-labs.web.app/). Happy to say, I'd almost tried out around 95% of components at the lab. I'm here to learn more on IoT; and thus awaiting for the future Levels of **Kerala IoT Challenge**. 

## IoT Challenge Experiments

### Experiment 1 - Hello World LED Blinking

![Hello World LED Blinking](https://user-images.githubusercontent.com/44474792/132120834-bddf79e5-99d3-4d99-a355-b5776fd7c1a0.jpg)
#### Code
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### Experiment 2 - Traffic Light

![Traffic Light](https://user-images.githubusercontent.com/44474792/132121020-4329f96c-e525-4472-aad3-e703826993d2.jpg)
#### Code
```ino
void setup() 
{
   pinMode(13, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(8, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(5000);
  digitalWrite(13, LOW);
  
  for(int i=0; i<3; i++)
  {
    delay(500);
    digitalWrite(10, HIGH);
    delay(500);
    digitalWrite(10, LOW);
  }
  
  delay(500);
  digitalWrite(8, HIGH);
  delay(5000);
  digitalWrite(8, LOW);
}
```

### Experiment 3 - LED Chasing Effect

![image](https://user-images.githubusercontent.com/44474792/132120873-538e171f-9ffd-4356-aa7f-45576711db21.jpg)
#### Code
```ino
void setup()
{
   for (int i = 7; i < 13; i ++) 
   {
     pinMode(i, OUTPUT);
   }
}
void loop()
{
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, LOW);
     delay(200);
   }
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, HIGH);
     delay(200);
   }  
}
```

### Experiment 4 - Button Controlled LED

![image](https://user-images.githubusercontent.com/44474792/131449487-aa3968f7-22d9-46e4-bbdf-28320b440122.jpg)
#### Code
```ino
int x;
void setup()
{
  pinMode(11, OUTPUT);
  pinMode(7, INPUT);
}
void loop()
{
  val=digitalRead(7);
  if(x == LOW)
  {
    digitalWrite(11, LOW);
  }
  else
  {
    digitalWrite(11, HIGH);
  }
}
```

### Experiment 5 - Buzzer

![image](https://user-images.githubusercontent.com/44474792/132120819-7dca413d-2dbe-41b3-9929-c44915715aa0.jpg)
#### Code
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### Experiment 6 - RGB LED

![image](https://user-images.githubusercontent.com/44474792/131454311-4759b60a-1a38-41d7-81ea-0f67c87642ba.png)
#### Code
```ino
int red = 11;
int blue =10;
int green =9;
int x;
void setup() {
  pinMode(red, OUTPUT);
  pinMode(blue, OUTPUT);
  pinMode(green, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(x=255; x>0; x--)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
for(x=0; x<255; x++)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
 Serial.println(x, DEC);
}
```

### Experiment 8 - Flame Sensor

![image](https://user-images.githubusercontent.com/44474792/132122467-26653513-32ed-4e38-ad54-cf36b7edd49d.jpg)
#### Code
```ino
const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
```

### Experiment 9 - LM35 Temperature Sensor

![image](https://user-images.githubusercontent.com/44474792/132123183-a7430048-f9c6-4c4f-8406-485e2f29fe5d.png)
![image](https://user-images.githubusercontent.com/44474792/132123315-9d2945a6-47d8-4f57-9b11-d961f9e8ccdf.png)
#### Code
```ino
const int lm35_pin = A1;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int temp_adc_val;
  float temp_val;
  temp_adc_val = analogRead(lm35_pin);
  temp_val = (temp_adc_val * 4.88);
  temp_val = (temp_val/10);
  Serial.print("Temperature = ");
  Serial.print(temp_val);
  Serial.print(" Degree Celsius\n");
  delay(1000);
}
```

### Experiment 10 - IR Remote Control using TSOP

![image](https://user-images.githubusercontent.com/44474792/132123811-9a9b2e0c-fa46-4071-afa0-cce80012e10d.png)
#### Code
```ino
#include <IRremote.h>
 
int RECV_PIN = 3;
int c=0;
IRrecv irrecv(RECV_PIN);
decode_results results;

void setup()
{
  pinMode(9, OUTPUT);
  Serial.begin(9600);
  irrecv.enableIRIn();
}

void loop() {
  if (irrecv.decode(&results)) {
    Serial.println(results.value);
    irrecv.resume();
    if(results.value==YOUR VALUE1) {
      digitalWrite(9,HIGH);
    }
    else if(results.value==YOUR VALUE2) {
    digitalWrite(9,LOW);
    }
  }
}
```

### Experiment 11 - Potentiometer analog Value Reading

![image](https://user-images.githubusercontent.com/44474792/132124333-56134c03-b7e2-4573-af4b-6006ee8935ce.jpg)
#### Code
```ino
int potpin = 0;
int ledpin = 13;
int val = 0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
  digitalWrite(ledpin, HIGH);
  delay(50);
  digitalWrite(ledpin, LOW);
  delay(50);
  val = analogRead(potpin);
  Serial.println(val);
}
```

### Experiment 12 - Segment Display

![image]()
#### Code
```ino
// To be filled
```

## IoT Challenge Assignments

### Assignment 1 - Automatic Night Lamp

![image]()
#### Code
```ino
const int LED = 13;  
const int LDR = A0;  

void setup() {
  Serial.begin(9600);
  pinMode(LED, OUTPUT); 
  pinMode(LDR, INPUT);   
}

void loop()
{
  int ldrStatus = analogRead(LDR);  
  if (ldrStatus <= 400) {
    digitalWrite(LED, HIGH);               
    Serial.println("Room is DARK - LED ON");
  }
  else {
    digitalWrite(LED, LOW);         
    Serial.println("Room is BRIGHT - LED OFF");
    }
}
```
