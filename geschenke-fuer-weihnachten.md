# Geschenke für Weihnachten

Der Weihnachtsmann und seine Elfen hatten letztes Jahr soviel zu tun, dass sie es nur mit Ach und Krach schafften, alle Spielzeuge für alle Kinder herzustellen. In einer Overallretro haben der Weihnachtsmann, seine Frau und seine Elfen festgestellt, dass sie an ihrer Kapazitätsgrenze arbeiten. So beschlossen sie, auch Spielzeuge bei anderen Herstellern fertigen und liefern zu lassen. 

Nach langen Telefonaten mit allen möglichen Spielzeugfabriken wurde dem Weihnachtsmann ein paar Dinge klar

1. Jede Fabrik braucht unterschiedlich lange, um eine Menge an Spielzeug zu produzieren.
2. Jede Fabrik hat ihre eigene maximal Kapazität, um für den Weihnachtsmann Spielzeug herzustellen.
3. Die Lieferzeit ist auch für jede Fabrik unterschiedlich aber dank eines Spezialweihnachtscontainers unabhängig von der bestellten Menge.

Der Weichnachtsmann hat sich auch am Nordpol umgesehen und wenig überraschend festgestellt, dass die Lagerkapazitäten nicht weiter ausgebaut werden können, da eine Unterkellerung ausgeschlossen ist. Somit müssen alle Spielzeuglieferungen zwischen dem 22. und dem 24. Dezember eintreffen und direkt auf seinen Schlitten verpackt werden.

Der Spezialweihnachtscontainer ist eine großartige Erfindung, die es erlaubt mit einem einzigen Container die gesamte Spielzeuglieferung einer Fabrik an den Nordpol zu liefern. Die Gilde der transportierenden Elfen, erlaubt jedoch den anstrengenden Transport nur an Arbeitstagen. Und die Fabriken geben die Lieferzeit immer in Arbeitstagen an.

Könnt ihr dem Weihnachtsmann bei der Planung helfen?


## User story #1

Dem Weihnachtsmann ist schon geholfen, wenn er wüsste, wann eine Bestellung aufgegeben versendet werden, damit diese am 24. Dezember bei ihm eintrifft. Sollte der 24. Dezember kein Arbeitstag sein, so darf die Lieferung an dem letzten Arbeitstag vor dem 24. Dezember eintreffen.

Die Gilde der transportierenden Elfe hat folgende Arbeitstage festgelegt: 

* Montag, Mittwoch, Donnerstag, Sonntag.
* An jedem 1. Montag und Mittwoch im Monat darf gearbeitet werden.

Die Gilde hat auch folgende Feiertage definiert an denen nicht transportiert werden darf:

* Im August und September ist jeder zweite Arbeitstag ein Feiertag
* Im Dezember ist der Sonntag auch ein Feiertag
* Am 12. November
* Am 06. und 07. Dezember

Santa möchte ein einfaches Programm. Als Eingabe genügt ihm StdIn und als Ausgabe StdOut. 
Der Weihnachtsmann gibt das Jahr der Anlieferung und die Lieferzeit in Tagen in der Form `JJJJ N+` ein und als Ausgabe erhält er das Datum `TT.MM.JJJJ` an dem die Lieferung abgesendet werden muss, damit sie am 24. Dezember eintrifft (oder dem letzten Arbeitstag vor Weihnachten).



Beispiel

Eingabe
```
2021 3
```

Ausgabe
```
20.12.2021
```

## User story #2

Das einzelne Prüfen der Versanddaten pro Fabrik wird dem Weihnachtsmann zu viel. Als Weihnachstmann möchte er eine Liste der Fabriken eingeben können und die Bestellungen mit ihren Bestelldaten ausgeben können.

Pro Fabrik möchte der Weihnachtsmann deren maximale Liefermenge, die Produktionszeit in Kalendertagen und die Lieferzeit in Arbeitstagen eingeben können. Lieder kann die Fabrik den Auftrag nicht annehmen, wenn die Bestellmenge die Liefermenge überschreiten.

Als Ergebnis pro Fabrik das Bestelldatum mit der geforderten Bestellmenge erhalten. Hierbei muss das Bestelldatum einen Tag vor der ersten Produktionstag liegen.

Eingabe

```
JJJJ  - Weihnachtsjahr
X - Spielzeugmenge die im Weihnachtsjahr JJJJ am 24.12 benötigt wird
N - Anzahl der Fabriken
Liefermenge_1 Liefermenge_2 ... Liefermenge_N - Liefermengen getrennt durch ein <SPACE>
Produtionszeit_1 Produktionszeit_2 Produktionszeit_N - Produktionszeiten getrennt durch ein <SPACE>
Lieferzeit_1 Lieferzeit_2 ... Lieferzeit_N - Lieferzeiten getrennt durch ein <SPACE>
```

Augabe

```
Bestellmenge_Fabrik_1 Bestelldatum_Fabrik_1 - Ergebnis für Fabrik 1 oder "-" falls keine Bestellung aufgegeben wird
Bestellmenge_Fabrik_2 Bestelldatum_Fabrik_2 - Ergebnis für Fabrik 1 oder "-" falls keine Bestellung aufgegeben wird
...
Bestellmenge_Fabrik_N Bestelldatum_Fabrik_N - Ergebnis für Fabrik 1 oder "-" falls keine Bestellung aufgegeben wird
```


Beispiel:

Eingabe: 

```
2021
2
2
1 2
1 1
1 1
```

Ausgabe:

```
-
2 21.12.2021
```

Erklärung:

Fabrik_1 kann nicht beauftragt werden, da die Bestellmenge deren Liefermenge überschreitet.

Fabrik_2 kann beauftragt werden, da die Bestellmenge durch deren Liefermenge abgedeckt werden kann. Der 24.12.2021 ist ein Freitag. So muss die Lieferung am Do. 23.12 als letztem Gildenarbeitstag vor Weihnachten erfolgen. Die Produktion findet am 22.12. statt und die Bestellung von 2 Spielzeugen muss somit am 21.12. erfolgen.
