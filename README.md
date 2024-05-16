# Laser-Security-System

## Objective

The Laser Security System provides peripheral security to your property and alerts you with sound alarms when an someone trespasses.

### Skills Learned

- Hardware and Circuit Designing.
- Types of Sensors.
- Laser technology.
- Programming language:Arduino
-  IDE: Arduino IDE (Arduino Software)
-  Device: Arduino UNO R3

### Components Required

- Arduino UNO R3
- Breadboard
- LDR(Light Dependent Resistance)
- Laser
- Buzzer
- Resistor
- Jumper wires
- Arduino IDE

### Tools Used

- LDR
- Laser
- Buzzer

### Code:

```
int buzzer = 8;
int ldrvalue;
int state = 200;
void setup()
{
	Serial.begin(9600);
	pinMode(buzzer, OUTPUT);
}

void loop()
{
	ldrvalue = analogRead(A0);
	if (ldrvalue<state)
	{
		digitalWrite(buzzer, HIGH);
		Serial.println(ldrvalue);
		delay(500);
	}
	else 
	{
		digitalWrite(buzzer, LOW);
	}
}
```
### Circuit Diagram:
![Screenshot 2024-05-16 231150](https://github.com/GitKhushal/Laser-Security-System/assets/168212318/b34afe91-dfd3-4cd3-9685-dbda75f4b08e)
