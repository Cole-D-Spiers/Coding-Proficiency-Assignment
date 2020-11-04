# Coding-Proficiency-Assignment
Question 2 (did this a little diffrent when experimenting with some stuff)

#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

long randNumber;                                                            
const int analogOutPin = 6;                                                

void setup()
{
 
  lcd.begin(16, 2);

  lcd.print("ENGINEERS GARAGE");
  lcd.setCursor(0, 1);
  lcd.print("  RANDOM NUMBER ");
 
  Serial.begin(9600);

  randomSeed(analogRead(0));
}

void loop()
{
  randNumber = random(0, 255);                                             
  Serial.println(randNumber);                                               
  analogWrite(analogOutPin, randNumber);                                 
  delay(300);
}

Question 
