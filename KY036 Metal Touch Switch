/*******************************************************
KY036 Metal Touch Sensor
Connect;
AO to Arduinp pin A3
DO to Arduino pin 2
G to Arduino Gnd
Vcc to Arduino 5v
*******************************************************/
// 
//
// setup touch sensor on pin 2
const int touchPin = 2;
// setup LED on pin 13
const int ledPin = 13;
// store thetime when the last event happened
unsigned long lastEvent = 0;
// store the state of the LED
boolean ledOn = false;
void setup() {
// setup pins
pinMode(touchPin, INPUT);
pinMode(ledPin, OUTPUT);
digitalWrite(ledPin, LOW);
}
void loop() {
// read the touch sensor state
int touchState = digitalRead(touchPin);
// only interested in HIGH
if(touchState == HIGH){
// if 50ms have passed since the last HIGH pulse
// touch sensor has been touched or released
if(millis() - lastEvent >50){
// toggle LED and set the output
ledOn = !ledOn;
digitalWrite(ledPin, ledOn ? HIGH : LOW);
}
// remember when the last event happened
lastEvent = millis();
}
}
