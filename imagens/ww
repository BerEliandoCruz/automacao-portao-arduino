//=====================================
// PINOS DOS MOTORES
//=====================================
const int motorInterno_p = 12;
const int motorInterno_n = 13;

const int motorExterno_p = 10;
const int motorExterno_n = 11;

//=====================================
// BOTÕES
//=====================================
const int botaoInterno = 8;
const int botaoExterno = 7;

//=====================================
// LEDS
//=====================================
const int ledVerdeInterno = 5;
const int ledVermelhoInterno = 4;

const int ledVerdeExterno = 3;
const int ledVermelhoExterno = 2;

//=====================================
// BUZZER
//=====================================
const int buzzer = 6;

//=====================================
// ESTADOS
// 0 = FECHADO
// 1 = ABERTO
//=====================================
int st_portao_interno = 0;
int st_portao_externo = 0;

//=====================================
// ABRE PORTÃO INTERNO
//=====================================
void abre_portao_interno()
{
  // Vermelho durante abertura
  digitalWrite(ledVerdeInterno, LOW);
  digitalWrite(ledVermelhoInterno, HIGH);

  // Som durante abertura
  tone(buzzer, 1000);

  // Liga motor
  digitalWrite(motorInterno_p, HIGH);
  digitalWrite(motorInterno_n, LOW);

  delay(3000);

  // Desliga motor
  digitalWrite(motorInterno_p, LOW);
  digitalWrite(motorInterno_n, LOW);

  // Desliga som
  noTone(buzzer);

  // Intervalo entre vermelho e verde
  delay(500);

  // Portão aberto
  st_portao_interno = 1;

  // Acende verde
  digitalWrite(ledVerdeInterno, HIGH);
  digitalWrite(ledVermelhoInterno, LOW);

  // Bip de confirmação
  tone(buzzer, 2000);
  delay(500);
  noTone(buzzer);
}

//=====================================
// FECHA PORTÃO INTERNO
//=====================================
void fecha_portao_interno()
{
  // Vermelho durante fechamento
  digitalWrite(ledVerdeInterno, LOW);
  digitalWrite(ledVermelhoInterno, HIGH);

  tone(buzzer, 500);

  digitalWrite(motorInterno_p, LOW);
  digitalWrite(motorInterno_n, HIGH);

  delay(3000);

  digitalWrite(motorInterno_p, LOW);
  digitalWrite(motorInterno_n, LOW);

  noTone(buzzer);

  st_portao_interno = 0;
}

//=====================================
// ABRE PORTÃO EXTERNO
//=====================================
void abre_portao_externo()
{
  digitalWrite(ledVerdeExterno, LOW);
  digitalWrite(ledVermelhoExterno, HIGH);

  tone(buzzer, 1000);

  digitalWrite(motorExterno_p, HIGH);
  digitalWrite(motorExterno_n, LOW);

  delay(3000);

  digitalWrite(motorExterno_p, LOW);
  digitalWrite(motorExterno_n, LOW);

  noTone(buzzer);

  delay(500);

  st_portao_externo = 1;

  digitalWrite(ledVerdeExterno, HIGH);
  digitalWrite(ledVermelhoExterno, LOW);

  tone(buzzer, 2000);
  delay(500);
  noTone(buzzer);
}

//=====================================
// FECHA PORTÃO EXTERNO
//=====================================
void fecha_portao_externo()
{
  digitalWrite(ledVerdeExterno, LOW);
  digitalWrite(ledVermelhoExterno, HIGH);

  tone(buzzer, 500);

  digitalWrite(motorExterno_p, LOW);
  digitalWrite(motorExterno_n, HIGH);

  delay(3000);

  digitalWrite(motorExterno_p, LOW);
  digitalWrite(motorExterno_n, LOW);

  noTone(buzzer);

  st_portao_externo = 0;
}

//=====================================
// SETUP
//=====================================
void setup()
{
  pinMode(motorInterno_p, OUTPUT);
  pinMode(motorInterno_n, OUTPUT);

  pinMode(motorExterno_p, OUTPUT);
  pinMode(motorExterno_n, OUTPUT);

  pinMode(botaoInterno, INPUT);
  pinMode(botaoExterno, INPUT);

  pinMode(ledVerdeInterno, OUTPUT);
  pinMode(ledVermelhoInterno, OUTPUT);

  pinMode(ledVerdeExterno, OUTPUT);
  pinMode(ledVermelhoExterno, OUTPUT);

  pinMode(buzzer, OUTPUT);

  // Estado inicial: fechado
  digitalWrite(ledVerdeInterno, LOW);
  digitalWrite(ledVermelhoInterno, HIGH);

  digitalWrite(ledVerdeExterno, LOW);
  digitalWrite(ledVermelhoExterno, HIGH);
}

//=====================================
// LOOP PRINCIPAL
//=====================================
void loop()
{
  if (digitalRead(botaoInterno) == HIGH)
  {
    if (st_portao_interno == 0)
      abre_portao_interno();
    else
      fecha_portao_interno();

    delay(500);
  }

  if (digitalRead(botaoExterno) == HIGH)
  {
    if (st_portao_externo == 0)
      abre_portao_externo();
    else
      fecha_portao_externo();

    delay(500);
  }
}
