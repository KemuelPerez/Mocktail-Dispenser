# Mocktail-Dispenser
int button = A0;
int sensorValue=0;
int Selection = A1;
int n = 1;
void setup() {
  // put your setup code here, to run once:
pinMode(13,OUTPUT);

pinMode(12,OUTPUT);

pinMode(9,OUTPUT);

pinMode(7,OUTPUT);

pinMode(button,INPUT);

pinMode(Selection,INPUT);

pinMode(1,OUTPUT);

pinMode(2,OUTPUT);

Serial.begin(9600);
}



void loop() {
  // put your main code here, to run repeatedly:

//if ( n==1){
//  digitalWrite(1,HIGH);
 // digitalWrite(2,LOW);
//}
//if ( n==2){
 // digitalWrite(2,HIGH);
//  digitalWrite(1,LOW);
//}
sensorValue=analogRead(button);
  Serial.println(sensorValue);
if (sensorValue==0){


digitalWrite(13,HIGH);
delay(10000);
digitalWrite(13,LOW);
delay(2000); 

digitalWrite(12,HIGH);
delay(10000);
digitalWrite(12,LOW);
delay(2000); 
}

if (sensorValue==1022){
digitalWrite(9,HIGH);
delay(10000);
digitalWrite(9,LOW);
delay(2000); 

digitalWrite(7,HIGH);
delay(10000);
digitalWrite(7,LOW);
delay(2000); 
}
}
