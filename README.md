# LuckMinerLV06

## Diese Seite ist noch in Entstehung

## Achtung! Nutzung auf eigene Gefahr, nur mit LuckyMiner LV06 verwenden!

Meine LuckyMiner haben alle die Leiterplatten-Revision: XSL 24001PCV11 mit Datum 2024.03.20

Die hier angebotene esp-miner.bin ändert die im NVS (kleiner Speicherbereich im ES32) geschriebene boardversion von 204 auf 0.11

### Hintergrund

Im August 2024 habe ich durch Zufall beim rum Google'n vom Minig mittels ESP32 gelesen. Da ich Hobbymäßig gerne mit ESP8266 und ESP32 rum programiere bin ich letztendlich über NerdMiner zu den LuckyMinern gestoßen.
Ich hatte mir über AliExpress ein Liligo ESP32-S3 bestellt. Angefixt vom Minig, bin ich dann auch bald auf die LuckyMinern und Bitaxe gestoßen. Zu dem Zeitpunkt kannte ich (Leider) noch nicht wirklich die Unterschiede und habe dann, aber auch ein wenig verständlich, drei LuckyMiner LV06 zu je ca. 70€ erworben.
Zu dem Zeitpunkt hatte ich nur Shops gefunden die für einen Bitaxe Ultra zwischen 170€ - 240€ haben wollten, und das dann auch noch mit Bitcoin Zahlung. Und ca. 200€ zu um die 600€ sind halt für 'Ich spiel da mal ein wenig rum' schon ein krasser Preisunterschied.
Das Bitaxe OpenSource Projekt ist schon mega krass, aber wer bitte soll PCB's selber bestellen und SMD's auflöten. Ja ich habe vor 20 Jahren, als es noch keine ESP's gab kleine Schaltungen selber mittels Eagle entworfen und in China (itead) fertigen lassen, und hinterher auch selber draht und SMD Bauteile verlötet. Heute möchte ich mir das aber nicht mehr antun.

Getreu meinem Motte 'Was man flashen kann, wird geflasht' habe ich mir dann wohl irgendwelche factory bin's aufgespielt, die die Boardversion auf 204 angehoben haben. Von da an wollten die LuckyMiner nur noch sporadisch funktionieren. Nach gefühlen 20 mal 'Strom an / Strom aus' liefen die dann komischer weise bis zur nächsten Spannungsunterbrechung einwandfrei.

#### Was hat das mit der Boardversion auf sich?
Ich bin nun nicht der mega Profi, und ich habe auch keine Lust noch tiefer in den Code einzusteigen (ich will ja nur ein wenig Minen), aber wie ich das sehe wurde nach den ersten Boardrevisionen 0.11/0.12 usw. bei den 2xx Board's noch ein Mosfet zu einem Spannungsregler verbaut der als Power_Enabled bezeichnet wird und über den GPIO10 des ESP32 angesteuert wird. Im Sourcecode finden sich einige Stellen wo das Powermanagement duch die Boardversion gesteuert wird. Wahrscheinlich hat der LuckMiner den Mosfet nicht, da er auf der Leiterplattenrevision 0.11 aufbaut und startet dann nicht, da die Software auf irgend eine Rückmeldung wartet. Merkwürdig ist nur das es nach 10 -20 mal Steckerziehen dann doch los geht. Evtl ein Bug? Oder so gewollt :)


