# nodemcu-01

## Översikt 
Nedan kommer jag att beskriva hur man kan testa att programmera utvecklingskortet **NodeMCU** i programmet **Arduino IDE**. I den här kursen så kommer vi att använda oss av **NodeMCU** och **Arduino IDE** för att bygga sensorer och samla in data som vi sedan kan visualisera, för kunna bygga kunskap utifrån den insamlade datan. 

## Microcontroller/NodeMCU
I kursen använder vi oss av ett **Plusivo Wireless Super Starter Kit** som innehåller en **NodeMCU**, vilket är ett utvecklingskort byggt på microcontrollern **ESP8266**, som har möjlighet till WiFi-anslutning för att skicka och ta emot data, samt går att programmera med hjälp av Arduino IDE.

<img width="829" height="820" alt="Screenshot 2025-11-27 at 14 31 39" src="https://github.com/user-attachments/assets/3e4b5148-dabc-4fb7-ba6d-f4895bb133e3" />


**ESP8266** går delvis att integrera med exempelvis en Arduino eller Raspberry Pi som ett WiFi-nätverkskort, men kan även användas fristående som en microcontroller. 
Utöver möjligheten till WiFi-anslutning så har ESP8266 flera fördelar, bland annat så är den billig och den fungerar mycket bra för IoT-projekt (Internet of Things), för hemautomation (som exempelvis att styra lampor), och kan kopplas till sensorer för att samla in data. Exempelvis kan det vara sensorer för rörelse, ljus, ljud, temperatur eller luftfuktighet. Processorn i ESP8266 är en Tensilica LX106. 

## Såhär ser vår NodeMCU ut
<img width="754" height="715" alt="Screenshot 2025-11-27 at 14 34 50" src="https://github.com/user-attachments/assets/d4383f59-3d00-4461-9d30-620310647b4d" />

Den silvriga grejen längst ned är en USB-port, som vi kommer att använda för att koppla in vår microcontroller till datorn och programmera den i Arduino IDE. 

## Arduino IDE

<img width="612" height="509" alt="arduino_ide" src="https://github.com/user-attachments/assets/0605b6f9-59e2-4cf4-b11b-b2a5d44c9593" />

**Arduino IDE** (Integrated Development Environment) är ett gratis program som används för kodredigering, kompilering och uppladdning. Med hjälp av Arduino IDE kan du skriva källkod (source code), kompilera den till maskinkod (object code) och ladda upp den till en extern enhet, som en microcontroller, via USB. Skillnaden mellan källkod (source code) och maskinkod (object code) är att källkod innehåller ord och är läsbart för människor, medan maskinkod är binär kod (ettor och nollor) som kan läsas av en dator. Man måste alltid kompilera sin källkod innan man laddar upp den, för att en dator ska kunna läsa den och köra programmet. 

## Exempel på hur källkod ser ut

<img width="600" height="469" alt="Screenshot 2025-11-27 at 14 49 38" src="https://github.com/user-attachments/assets/96e0e948-f376-4e06-ae9f-46daf8083d06" />

## Exempel på hur object code ser ut 

<img width="492" height="360" alt="binary-code" src="https://github.com/user-attachments/assets/f25e8060-ff1f-48eb-b6b6-235e3e47574b" />

## För att komma igång med Arduino IDE 
För att kunna programmera din microcontroller, behöver du först utföra följande steg i Arduino IDE: I menyn högst upp går du in på **Arduino IDE** – **Settings**. I menyn som öppnas klistrar du in följande länk: ```https://arduino.esp8266.com/stable/package_esp8266com_index.json``` 

<img width="543" height="269" alt="Screenshot 2025-11-27 at 15 39 50" src="https://github.com/user-attachments/assets/282a6fe0-d5fb-4e59-b852-9ca443200afd" />

<img width="785" height="480" alt="Screenshot 2025-11-27 at 15 40 54" src="https://github.com/user-attachments/assets/caa2d6a8-21ea-47b0-af86-c3fa7e91b58a" />

Sedan trycker du på den andra ikonen ovanifrån i menyn till vänster för att komma in på **Boards Manager**. Här kan du söka på ESP8266, och trycka på "Install". 

<img width="352" height="345" alt="Screenshot 2025-11-27 at 15 43 59" src="https://github.com/user-attachments/assets/a73580b9-80bc-46b5-a22f-c83bf7d13793" />


## Portinitialisering 
Microcontrollern går att ansluta till datorn via USB, vilket gör det möjligt att programmera den från sin dator med hjälp av Arduino IDE. Detta gör du genom att koppla in en micro USB-sladd till USB-A eller USB-C (beroende på vad du har för USB-portar på din dator).  

<img width="689" height="620" alt="Screenshot 2025-11-27 at 14 58 14" src="https://github.com/user-attachments/assets/ed9bab50-e9f0-4b9c-95b3-8abe467972c8" />

<img width="762" height="382" alt="Screenshot 2025-11-27 at 15 00 48" src="https://github.com/user-attachments/assets/539057fb-ca47-4897-afcf-881ccfd47c07" />


## Anslut rätt port i Arduino IDE 
När du har kopplat in microcontrollern till din dator via USB så ska du kunna hitta rätt port i Arduino IDE. Detta gör du i menyn högst upp, under **Tools** – **Port**. Här bör du kunna hitta namnet på rätt USB-port, till exempel "usbserial-10". 

<img width="962" height="744" alt="Screenshot 2025-11-27 at 15 06 12" src="https://github.com/user-attachments/assets/7e2538b6-cd4b-4059-9b77-f6eca16bd1ad" />

## Blink (exempelsketch) 
Projekt i Arduino IDE kallas för "sketch". Det finns olika exempelsketches som man kan kolla på och testa för att lära sig hur programmet funkar. Det första och vanligaste exemplet heter **Blink**, och som namnet antyder så är detta ett exempel på hur man får en lampa att blinka på sin microcontroller. Du hittar Blink genom att från menyn högst upp gå in på **File** – **Examples** – **Basics** – **Blink**. 

<img width="776" height="893" alt="Screenshot 2025-11-27 at 15 15 32" src="https://github.com/user-attachments/assets/762332a9-4a37-4fe8-83a4-fe658006aa5d" />

Blink kommer nu att öppnas i en ny ruta. Högst upp i koden finns det en beskrivning av vad programmet gör. En inbyggd LED-lampa kommer att blinka med en sekunds intervall. 

<img width="1511" height="787" alt="Screenshot 2025-11-27 at 15 19 07" src="https://github.com/user-attachments/assets/b52e302b-ae65-4cf4-ab88-c3560e1f24da" />

Man kan enkelt ändra intervallerna för att få lampan att blinka snabbare eller långsammare. Det gör man där det står ```delay(1000);```. Hastigheten är alltså 1000 millisekunder. Om man ändrar båda värdena till exempelvis 500 så kommer lampan att blinka i 500 millisekunder, det vill säga 0,5 sekunder. 

<img width="651" height="150" alt="Screenshot 2025-11-27 at 15 22 37" src="https://github.com/user-attachments/assets/339ffcff-e54f-43b7-b12f-0850a0c8775e" />
<img width="651" height="150" alt="Screenshot 2025-11-27 at 15 23 29" src="https://github.com/user-attachments/assets/81533553-1d79-4b66-94f7-d01fdfbcc020" />

När man är färdig med koden så behöver man trycka på **Verify** för att kompilera den. Det är den blå knappen med en bock uppe till vänster. 

<img width="360" height="105" alt="Screenshot 2025-11-27 at 15 26 31" src="https://github.com/user-attachments/assets/6465354d-8f5c-4606-8dd9-b67c6191e4ca" />

Vänta på att kompileringen ska ladda klart, och tryck sedan på den blå knappen med en högerpil precis bredvid (**Upload**), för att ladda upp koden till din microcontroller. 

<img width="385" height="141" alt="Screenshot 2025-11-27 at 15 29 24" src="https://github.com/user-attachments/assets/48790ace-a236-465b-a684-f1c5fce40939" />

När uppladdningen är färdig så bör den lilla inbyggda lampan på din microcontroller blinka i den hastighet du har angivit! 

## Koden för Blink ser ut såhär: 

```*/

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
} 
