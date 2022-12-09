#include<LiquidCrystal.h>
#define CS=A7; 
float CSin;
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);
int sensitivity = 66;
int adcValue= 0;
int offsetVoltage = 2500;
double adcVoltage = 0;
double currentValue = 0;
void setup()
{
Serial.begin(9600);
lcd.begin(16,2);
pinMode(CS, INPUT);
lcd.print("--")
}

void loop()
{
  CSin=analogRead(CS);
  lcd.setcursor(0,0);
  lcd.print("Vltg");
  lcd.setcursor(5,0);
  lcd.print("Amps");

}
