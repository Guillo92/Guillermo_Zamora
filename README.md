# Guillermo_Zamora
Guillermo Xavier Zamora  Limaico
// NOMBRE: GUILLERMO ZAMORA
// FECHA : 16//11//2016


// este programa es un contador de o al 99 con pulsador 
// declaracion de variables
int A = 13;
int B = 12;
int C = 11;
int D = 10;
int cont = 0;
int puls = 7;
int unid = 9;
int dece = 8;
int contd=0;
int contu=0;
void setup() {
  // entradas y salidas del arduino 
  pinMode (A, OUTPUT);
  pinMode (B, OUTPUT);
  pinMode (C, OUTPUT);
  pinMode (D, OUTPUT);
  pinMode (unid, OUTPUT);
  pinMode (dece, OUTPUT);
  pinMode (puls, INPUT);
}

void loop() {
if(digitalRead(puls)==HIGH && cont <=99){     // Condición if cuando el pulsador esta en alto y cont < 99
  contd=cont/10;                               
          digitalWrite(unid,LOW);                //unidades alto
          digitalWrite(dece,HIGH);              // unidades bajo 
          Display(contd);                       // llamado al metodo
          delay(50);                                  // retardo
          contu=cont-(contd*10);      
          digitalWrite(unid,HIGH);              
          digitalWrite(dece,LOW);               
          Display(contu);                 
          delay(50);                                 
  cont= cont +1;                            
  }
}
void Display (int numero) {                                 //metodo 
  switch (numero) {                                    
    case 0:                                          // casos del 1 al 9
      digitalWrite(A, LOW);
      digitalWrite(B, LOW);
      digitalWrite(C, LOW);
      digitalWrite(D, LOW);
      break;
    case 1:                                                                    
      digitalWrite(A, HIGH);
      digitalWrite(B, LOW);
      digitalWrite(C, LOW);
      digitalWrite(D, LOW);
      break;
    case 2:
      digitalWrite(A, LOW);
      digitalWrite(B, HIGH);
      digitalWrite(C, LOW);
      digitalWrite(D, LOW);
      break;
    case 3:
      digitalWrite(A, HIGH);
      digitalWrite(B, HIGH);
      digitalWrite(C, LOW);
      digitalWrite(D, LOW);
      break;
    case 4:
      digitalWrite(A, LOW);
      digitalWrite(B, LOW);
      digitalWrite(C, HIGH);
      digitalWrite(D, LOW);
      break;

    case 5:

      digitalWrite(A, HIGH);
      digitalWrite(B, LOW);
      digitalWrite(C, HIGH);
      digitalWrite(D, LOW);
      break;


    case 6:
      digitalWrite(A, LOW);
      digitalWrite(B, HIGH);
      digitalWrite(C, HIGH);
      digitalWrite(D, LOW);
      break;

    case 7:
      digitalWrite(A, HIGH);
      digitalWrite(B, HIGH);
      digitalWrite(C, HIGH);
      digitalWrite(D, LOW);
      break;

    case 8:
      digitalWrite(A, LOW);
      digitalWrite(B, LOW);
      digitalWrite(C, LOW);
      digitalWrite(D, HIGH);
      break;

    case 9:
      digitalWrite(A, HIGH);
      digitalWrite(B, LOW);
      digitalWrite(C, LOW);
      digitalWrite(D, HIGH);
      break;

  }
}




