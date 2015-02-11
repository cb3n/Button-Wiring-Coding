# Button-Wiring/Coding-SOS
First Go at button wiring and coding for Arduino Red Board


Originally, I wanted to create a fading blinking light when the button was pressed.  I ran into some difficulty when I couldn't quite make the light fade when turning on and off after the button had been pressed.

In order to wire the button to the breadboard I found a tutorial / walk-through on Arduino's site showing the proper layout and wiring schematics.  I would like to learn more about how to properly wire these on my own, as to build that confidence and necessary ability.  When trying to code the blinking light, I settled on creating an S.O.S beacon through proper delays and turning the light on and off.  I wanted to try and figure out a way to use a much simpler method such as a FOR loop, however could not code it properly.  This is another area I would like to learn more about.

Code for the SOS Arduino:

const int buttonPin = 2;     // the number of the pushbutton pin
const int ledPin =  9;      // the number of the LED pin
const int h = 1;
const int l = 0;
// variables will change:
int buttonState = 0;// variable for reading the pushbutton status
int x = 1;

void setup() {
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);    
  
  // check if the pushbutton is pressed.
  // if it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    delay(30);
    digitalWrite(ledPin, HIGH);
    delay(500);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(500);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(500);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(3000);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(3000);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(3000);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(500);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(500);
    digitalWrite(ledPin, LOW);
    delay(500);
    digitalWrite(ledPin, HIGH);
    delay(500);
  }
  else{
    digitalWrite(ledPin, LOW);
  }
 }
