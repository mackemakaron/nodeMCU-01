# Presentation-fredag
<h1>Översikt</h1>
<p>Här ska jag berätta och visa hur jag har fått en lampa att blinka.</p>
<h1>Mikroprocessor</h1>
<p> Mikroprocessorn (MCU - micro controller unit) som användes var Plusivo. Vi använde Arduinos IDE-program men använde Plusivos MCU och la in en ytterligare board manager url som jag googlade fram - esp 8266 (http://arduino.esp8266.com/stable/package_esp8266com_index.json). 
<br>
<h2>Hur gjorde jag? Var klickade jag?</h2>
I Arduino klickade jag på <b>File</b> i vänstra hörnet högst upp, sedan <b>Preferences</b> och under <b>Additional boards manager URLs</b> klistrade jag in URL:en för ESP 8266.
<br>
Sedan gick jag in i <b>Boards Manager</b> som finns i vänster kant.
<br>
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Sk%C3%A4rmbild%202025-11-27%20195500.png" width="200">
Därefter klickade jag på <b>Tools</b> i samma hörn, 
  <br>
  <br>
  Jag kopplade in Mikroprocessorn i en av datorns USB-portar.
  <br>
  <img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/Porten.jpg" width="200">
</p>
<h1>Här är koden</h1>
<p>
  <code>void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);}

// the loop function runs over and over again forever
void loop() 
{
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}</code>
</p>
<p>
  I koden kunde jag ändra <code>delay(1000)</code> för att ändra blinkningens hastighet.
  <h2>Fun Fact:</h2> // är kommentarer som gäller för just den raden, /* och */ är längre blockkommentarer och dom ignoreras av kompilatorn när den bygger objektkod.
</p>
<h2>Resultatet</h2>
<p>Lampan blinkar blått.</p>
<img src="https://github.com/mackemakaron/Presentation-fredag/blob/main/blinkande%20lampa.jpg" width="300">
