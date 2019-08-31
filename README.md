# Ultra-sonic

```cpp
 int trig = 8;
 int echo = 9;
void setup() {
  // put your setup code here, to run once:
 Serial.begin(9600);
 pinMode(trig, OUTPUT);
 pinMode(echo, INPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
 digitalWrite(trig, LOW);
 digitalWrite(echo, LOW);
 delayMicroseconds(1);
 digitalWrite(trig, HIGH);
 delayMicroseconds(10);
 digitalWrite(trig, LOW);
 unsigned long duration = pulseIn(echo, HIGH);
 float distance = duration / 29.0 / 2.0;
 Serial.print(distance);
 Serial.println("cm");
 delay(200);

}
```
