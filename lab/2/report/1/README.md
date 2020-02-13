<h1> TP2 </h1>

<h1>Lab 2 Introduction à la communication</h1>

<h2> Fritzing </h2>
<p> Dans cette partie nous avons réalisé, comme il a été demandé dans le sujet, d'abord la création d'un nouveau sketch puis la recherche et l'ajout du NodeMCU-32S sur Fritzing en suivant le mien du composant.</p>
<h4><p>Création d'un sketch aléatoire composé de 5 éléments.</p></h4>
<p> Notre Sketch est composé de 5 éléments que sont ESP-32S, 400 Hole Breadboard, un capteur de température (lm35), 3 fils éléctriques(jumper Wire65), une résistance 220Ω et dont voici ci-dessous l'image d'illustration </p>
<img src="https://github.com/institut-galilee/2020-smart-box/blob/master/lab/2/sketch.png"/>
<p> Cla figure ci-dessus représente onception du schéma du sketch aléatoire <p/>
<img src="https://github.com/institut-galilee/2020-smart-box/blob/master/lab/2/schematic.png"/>
<P> La figure ci-dessus représente la vue schématique du sketch.<P/>
 
<h2> La communication </h2>
<code>
 byte buzzPin = 8;

void setup() {
  // put your setup code here, to run once:
    pinMode(buzzPin,OUTPUT);
    Serial.begin(9600);
}

void loop() {
  while (Serial.available() > 0) {
    int i  = Serial.parseInt();
    byte val  = Serial.read();
    Serial.println(val);
    tone(buzzPin,val);
    delay(100);
  }

}
 </code>
<img src="https://github.com/institut-galilee/2020-smart-box/blob/master/lab/2/buzzerPassif.jpg"/>
 <P> <P/>
<img src=""/>
<P> <P/>
