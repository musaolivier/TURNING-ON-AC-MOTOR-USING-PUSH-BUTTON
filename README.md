# TURNING-ON-AC-MOTOR-USING-PUSH-BUTTON
# 1.1 ABSTRACT 
This project called” TURNING ON AC MOTOR USING PUSH BUTTON” the basic control of the motor for this project will be based on “ARDUINO UNO “circuit, to turn on an ac motor by pressing a push button to transmit the signal to Arduino Uno to switch the coil of relay that will control an Ac motor to be turned on. This motor will be used in some electrical equipment and machine to convert the electrical energy into mechanical energy for the main application in various equipment such as: irrigation pumps, water heaters, lawn and garden equipment, ovens, and off-road motorized equipment.  However, the controlling of an Ac motor was existed by using the push button and a contractor, for this reason we applied the recent development to control the motor with simple Arduino that will be switching the Ac motor accordingly. 

# 1.2.	PROBLEM STATEMENT
According to the traditional system of controlling an Ac motor by using electrical contactors this system was very expensive, complex to design and difficult in monitoring. And also, the old system of controlling an ac motor it was occupying large space during installation and producing more heat in the system and less reliable. Therefore, by making improvement and an easy control of an Ac motor by using Arduino. This will reduce the cost of implementation and maintenance of a system. And this system of controlling an ac motor by using Arduino is more reliable and also it doesn’t produce more heat during it’s operation. By using this project in different purpose in home and other places.

 # BLOCK DIAGRAM OF TURNING ON AC MOTOR USING PUSH BUTTON

![image](https://user-images.githubusercontent.com/104015191/164712930-8ec6af1d-41ac-459a-8289-248ecd5cf09d.png)

When someone press a push button, it sends a digital signal to  Arduino , therefore Arduino U receives the signal from push button and sends it to a Transistor in order to switch  a relay for a low voltage(+5V) so that the relay  will activate ON an AC motor .
 
# 1.3.	CIRCUIT DIAGRAM IN FRITZING
 
![image](https://user-images.githubusercontent.com/104015191/164712539-bef9fda6-1ac3-45bf-bff2-1696c220984d.png)

# 1.4 CIRCUIT IN PROTEUS
![proteus image](https://user-images.githubusercontent.com/104015191/166152855-c27e3e65-07ed-444e-99f1-839eb1a5f419.PNG)

# 1.5 COMPLING IMAGE IN ARDUINO IDE
![arduino ide imag](https://user-images.githubusercontent.com/104015191/166152903-a2d914d4-69c6-42e0-a904-9df0dd122a0b.PNG)

# SOURCE CODE:

int pushbutton=8;
int motor=3;
int buttonstate=0;

void setup() {
  // initialize digital PIN MOTOR_ as an output.
  pinMode(8, INPUT_PULLUP);
  pinMode(3, OUTPUT);
  Serial.begin(9600);
}

// the loop function runs over and over again forever
void loop() {
  buttonstate=digitalRead(pushbutton);
  
  if (buttonstate==HIGH)
  {digitalWrite(3, HIGH);
  Serial.println("MOTOR IS ON"); 
  }
  else {
  digitalWrite(3, LOW);
  Serial.println("MOTOR IS OFF"); 
  }                   
}
