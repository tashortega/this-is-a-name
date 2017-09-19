# this-is-a-name
int redledPin = 7;
int greenledPin = 6;
int secondbuttonPin = 9;

void setup() {
  Serial.begin (9600);
  pinMode(secondbuttonPin, INPUT);
  pinMode(redledPin, OUTPUT);
  pinMode(greenledPin, OUTPUT);
}
void loop() {
  int sreading = digitalRead(secondbuttonPin);


  if (sreading == HIGH) {
    digitalWrite(redledPin, HIGH);
  }
  else if (sreading == LOW) {
    digitalWrite(greenledPin, HIGH);
  }
  if (sreading == HIGH) {digitalWrite(greenledPin,LOW);}
  if (sreading == LOW) {digitalWrite(redledPin,LOW);}
}
