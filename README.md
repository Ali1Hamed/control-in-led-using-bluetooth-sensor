# //control-in-led-using-bluetooth-sensor
//this program to control in led using bluetooth sensor 
//  this program to control in led using bluetooth sensor 
//  

int led =6; // define the led pin 
char val;   // variable to read data in it
void setup() {
  Serial.begin(9600);     // start serial 
  pinMode(led,OUTPUT);    // made led pin as output pin 

}

void loop() {
  val=Serial.read();    // read 1 or 2 from the sensor 
  // if the value is 1 make led on
  if(val=='1')          
  {
    digitalWrite(led,HIGH);
  }
  // if the value is 1 make led off
  else if(val=='2')
  {
    digitalWrite(led,LOW);
  }
}
