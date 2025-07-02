// PendTech  
// Anti sleep alarm for drivers

const int sensorPin = 2;     // Pin connected to the IR sensor (or eye detection sensor)
const int motorPin = 8;      // Pin connected to the motor
const int buzzerPin = 9;     // Pin connected to the buzzer

void setup() {
  pinMode(motorPin, OUTPUT);   // Set motorPin as an OUTPUT
  pinMode(buzzerPin, OUTPUT);  // Set buzzerPin as an OUTPUT
  pinMode(sensorPin, INPUT);   // Set sensorPin as an INPUT

  digitalWrite(motorPin, HIGH);  // Motor ON by default
  digitalWrite(buzzerPin, LOW);  // Buzzer OFF by default
}

void loop() {
  // Read sensor input
  if (!digitalRead(sensorPin)) {
    // Eyes closed
    digitalWrite(buzzerPin, HIGH); // Turn ON buzzer
    digitalWrite(motorPin, LOW);   // Turn OFF motor
  } else {
    // Eyes open
    digitalWrite(buzzerPin, LOW);  // Turn OFF buzzer
    digitalWrite(motorPin, HIGH);  // Turn ON motor
  }

  delay(100); // Optional debounce delay
}
