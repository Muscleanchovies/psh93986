#define CURRENT 25

// CURRENT 의 20 대신 30A 나 5A제품의 경우, 30 또는 5를 적어 주시면 됩니다.

 

void setup() {

  Serial.begin(9600);

}

 

void loop() {

  float volt = analogRead(A0) * (5.0 / 1024);

  float current = (volt - 2.5) * (CURRENT / 2);

  Serial.print("volt: \t");

  Serial.print(volt);

  Serial.print("  current: \t");

  Serial.print(current);

  Serial.println();

  delay(100);

}
