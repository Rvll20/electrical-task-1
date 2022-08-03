#include <Servo.h>

int position = 0;

int i = 0;

Servo servo_7;

void setup()
{
  servo_7.attach(7, 500, 2500);
}

void loop()
{
  position = 0;
  for (position = 1; position <= 179; position += 1) {
    servo_7.write(position);
    delay(20); // Wait for 20 millisecond(s)
  }
  for (i = 179; i >= 1; i -= 1) {
    servo_7.write(position);
  }
}
