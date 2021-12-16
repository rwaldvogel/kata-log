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



Beispiel 1

Eingabe
```
2021 3
```

Ausgabe
```
20.12.2021
```


