# butten the led and led matrix
 smart method electrony  TASK 1

 LINK To The design " https://www.tinkercad.com/things/3aV5SXBUZju-button-of-led/editel"
 ```
 //int button = 0;
void setup()
{
  pinMode(7, OUTPUT);
  pinMode(4,INPUT_PULLUP);
}

void loop()
{
  int button=digitalRead(4);
   if (button == HIGH) {
     digitalWrite(7, LOW);
  } else {
    digitalWrite(7, HIGH);
  }
}
```


 # led matrix
smart method electrony TASK 1

link to design "https://www.tinkercad.com/things/dog0dbyVgJ7-led-matrix/editel"

```
#define ROW1 13
#define ROW2 12
#define ROW3 11
#define ROW4 10
#define ROW5 9
#define ROW6 8
#define ROW7 7
#define ROW8 6

#define COL1 2
#define COL2 3
#define COL3 4
#define COL4 5
#define COL5 A3
#define COL6 A2
#define COL7 A1
#define COL8 A0

const int row[] = {ROW1, ROW2, ROW3, ROW4, ROW5, ROW6, ROW7, ROW8};
const int col[] = {COL1, COL2, COL3, COL4, COL5, COL6, COL7, COL8};

int A [8][8] = {{1,1,1,0,0,1,1,1},
                {1,1,0,1,1,0,1,1},
                {1,0,1,1,1,1,0,1},
                {1,0,1,1,1,1,0,1},
                {1,0,0,0,0,0,0,1},
                {1,0,1,1,1,1,0,1},
                {1,0,1,1,1,1,0,1},
                {1,0,1,1,1,1,0,1}};


void setup() {

  for (int i = 2; i <= 13; i++) {
  	pinMode(i, OUTPUT);
    digitalWrite(i, LOW);
  }
  pinMode(A0, OUTPUT);
  digitalWrite(A0, LOW);
  pinMode(A1, OUTPUT);
  digitalWrite(A1, LOW);
  pinMode(A2, OUTPUT);
  digitalWrite(A2, LOW);
  pinMode(A3, OUTPUT);
  digitalWrite(A3, LOW);
}

void loop() {
	drow(A);
  	
  	
}

void drow(int matrix[8][8]){
  for (int c=0; c<8; c++){
  	digitalWrite(col[c], HIGH);
    for (int r = 0; r < 8; r++){
    	digitalWrite(row[r],255*matrix[r][c]);
     // delay(1);
    }
    for (int r = 0; r < 8; r++){
    	digitalWrite(row[r], HIGH);
     //delay(2);
    }
    digitalWrite(col[c], LOW);
  }
}
```




 
