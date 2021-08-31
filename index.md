## Kerala IoT Challenge

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies** in Kerala is launching our prestigious program  **“Kerala IoT Challenge 2021”**,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### About Me
> Hello Folks! I'm [**Arjun Krishna**](http://arjunkrishna.in/). I'm a Post Graduation Student in Computer Applications (MCA) from [**Kristu Jyoti College of Management and Technology**](http://www.kristujyoticollege.com), Changanacherry. I have been exploring the world of IoT since my graduation life started. My life around IoT started to change when I got unrestricted access to the Mini IoT Lab that we setup at our [**Inovus Labs IEDC**](https://inovus-labs.web.app/). Happy to say, I'd almost tried out around 95% of components at the lab. I'm here to learn more on IoT; and thus awaiting for the future Levels of **Kerala IoT Challenge**. 

### Experiment 1 - Hello World LED Blinking

![Hello World LED Blinking](https://user-images.githubusercontent.com/44474792/128236417-cd030db4-53f3-4dd4-9831-cca4ca870247.png)
#### Code
```ino
void setup() 
{
   pinMode(8, OUTPUT);
}
void loop() {
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### Experiment 2 - Traffic Light

![Traffic Light](https://user-images.githubusercontent.com/44474792/128236979-70b70180-38e3-4fce-954a-fa7d06d965b1.png)
#### Code
```ino
void setup() 
{
   pinMode(13, OUTPUT);
   pinMode(12, OUTPUT);
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
    digitalWrite(12, HIGH);
    delay(500);
    digitalWrite(12, LOW);
  }
  
  delay(500);
  digitalWrite(8, HIGH);
  delay(5000);
  digitalWrite(8, LOW);
}
```

### Experiment 3 - LED Chasing Effect

![image](https://user-images.githubusercontent.com/44474792/128237949-b0a613aa-065e-47d2-aa78-35d281b9a94e.png)
#### Code
```ino
int BASE = 2 ;
int NUM = 6;
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);
     delay(200);
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
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

![image](https://user-images.githubusercontent.com/44474792/131449487-aa3968f7-22d9-46e4-bbdf-28320b440122.jpg)
#### Code
```ino
int x = 8;
void setup() 
{ 
  pinMode(x,OUTPUT);
} 
void loop() 
{
  digitalWrite(x, HIGH);
}
```
