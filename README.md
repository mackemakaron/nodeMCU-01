<h2>Översikt</h2>
<p>Jag har arbetat med en <b>NodeMCU</b>, ett utvecklingskort, vid namn <b>Plusivo</b> som har mikrokontrollern <b>ESP8266</b> och tillsammans med <b>Arduino IDE</b> använt en blinkexempelkod för att få en liten lampa att blinka.</p>

<h2>Vad gör Arduino?</h2>
<p>I Arduino skriver man in <b>Source Code</b> (det vi kan tyda) som sedan kompileras till <b>Object Code</b> (det datorn kan tyda). Source code är alltså kod vi människor skriver in med ord och kan läsa, medan object code är binär kod - ettor och nollor - som datorn kan läsa. Därefter kan man ladda upp koden till en mikrokontroller med USB, och beroende på vilken dator du har, till USB-A eller USB-C. I mitt fall hade jag USB-A.</p>

<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Porten.jpg" width="200">

<h2>Steg för steg</h2>
<p>Nu ska jag steg för steg gå igenom hur jag fick lampan att blinka.
<br>
<br>
I Arduino, vänstra hörnet högst upp, hittade jag denna meny:
<br>
<br>
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Sk%C3%A4rmbild%202025-11-27%20192022.png">
<br>
<br>
Jag klickade på <b>File -> Preferences</b> och under <b>Additional boards manager URLs</b> klistrade jag in URL för ESP8266 som jag hittade med en snabb googling.
<br>
<br>
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Sk%C3%A4rmbild%202025-11-27%20233010.png" width="200">
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Sk%C3%A4rmbild%202025-11-27%20233048.png" width="600">
<br>
<br>
I vänster kant finns <b>Boards Manager</b> som jag sedan gick in på och sökte på ESP8266. Jag installerade den.
<br>
<br>
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Sk%C3%A4rmbild%202025-11-27%20195500.png">
<br>
<br>
Därefter vände jag blicken mot denna meny igen
<br>
<br>
BILD
<br>
<br>
Sen klickade jag på <b>Tools -> Board -> esp2866 -> Generic ESP8266 Module</b>.
<br>
<br>
BILD
<br>
<br>
Jag såg sedan till att mikroprocessorn var kopplad till datorn och att Arduino använde rätt port.
<br>
<br>
BILD
</p>
<h2>Discodags!</h2>
<p>För att få lampan att blinka behövde jag använda en blinkexempelkod som man hittar under 
<br>
<b>File -> Examples -> 01.Basics -> Blink </b>. Man möts av denna kod:
<br>
<code>// the setup function runs once when you press reset or power the board
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
</code>
<br>
Arduino har två basfunktioner: <code>void setup()</code> och <code>void loop()</code>. Som kommentarerna (//) säger så körs setup en gång när Arduino startas eller återställs, medan loop körs om och om igen sålänge Arduino är på eller tills man stoppar den i koden. Koden visar att lampan tänds vid <code>HIGH</code> och släcks vid <code>LOW</code>. I koden kan jag dessutom ändra blinkningens hastighet genom att ändra värdet på <code>delay(1000)</code>. Som kommentarerna berättar så är 1000 = 1 sek. Ändrar man värdet till exempelvis 500 = 0,5 sek.
<br>
<br>
Sista steget är nu att kompilera koden och sedan ladda upp den. För att kompilera filen måste man klicka på <b>Verify</b> (bocken) och sedan på <b>Upload</b> (pilen) för att ladda upp den.
<br>
BILD
</p>
<h2>Resultat</h2>
<p>Nämen titta det lyser!</p>
BILD



