## Kerala IoT Challenge

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies** in Kerala is launching our prestigious program  **“Kerala IoT Challenge 2021”**,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### About Me
> Hello Folks! I'm [**Arjun Krishna**](http://arjunkrishna.in/). I'm a Post Graduation Student in Computer Applications (MCA) from [**Kristu Jyoti College of Management and Technology**](http://www.kristujyoticollege.com), Changanacherry. I have been exploring the world of IoT since my graduation life started. My life around IoT started to change when I got unrestricted access to the Mini IoT Lab that we setup at our [**Inovus Labs IEDC**](https://inovus-labs.web.app/). Happy to say, I'd almost tried out around 95% of components at the lab. I'm here to learn more on IoT; and thus awaiting for the future Levels of **Kerala IoT Challenge**. 

### Experiment 1 - Hello World LED Blinking

#### Circuit Diagram
![Hello World LED Blinking](https://user-images.githubusercontent.com/44474792/128217460-234ddef5-f473-461f-9da9-31f52f11faa2.png)
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

#### Circuit Diagram
![Traffic Light](https://user-images.githubusercontent.com/44474792/128217429-bde0c21a-ba47-4658-a40d-aec8922f88ab.png)
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

#### Circuit Diagram


#### Code
