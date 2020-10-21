# CoViD-19---Germany

Ein Dashboard 

## Allgemeine Version


## Freistaat Bayern mit Focus Landshut

### Team

- [Thomas Rogler](https://www.linkedin.com/in/tom-rogler-6405bbb1/)
- [Thomas Massie](https://www.linkedin.com/in/thomasmmassie/)
- [Thomas Hofmann](https://www.linkedin.com/in/thomas-hofmann-a2817646/)

### Eigenschaften

- Schneller Überblick über die wichtigsten Kennzahlen für Bayern und Landshut.
- Leicht verständlich (selbsterklärend).
- BetrachterIn bekommt ein Gefühl für die Dynamik der Pandemie.
- Vergleiche mit anderen Stadt-/Landkreisen sind möglich; dadurch kann die eigene Lage eingeordnet werden.

### Prototyp

Der Prototyp befindet sich auf Tableau Public und kann [hier](https://public.tableau.com/profile/thomas.massie#!/vizhome/CoViD-19---Bayern-Prototype01---Test/Dashboard) aufgerufen werden.

Aktuell sieht dieser so aus:
![Prototyp](https://github.com/thomassie/CoViD-19---Germany/blob/main/04---Screenshots/Bildschirmfoto%202020-10-21%20um%2000.05.37.png)

### Offene fragen
 
- **Daten**:
  - Welche Daten wollen wir nutzen und warum? 
    > *TMM*: Ich bin stark dafür nur Daten abzurufen, welche über eine API abrufbar sind und einen gewissen Mindeststandard aufweisen (z.B. identische Landkreisnamen).
- **Forecast**: Kann man die Vorhersage vom [Jülich Supercomputing Centre](https://covid19-bayesian.fz-juelich.de/) nutzen? 
   > *TMM*: So, wie ich das sehe, können wir die Vorhersagen nicht selbst erstellen, no way. Sie bieten die Daten aber auch leider nicht über eine Schnittstelle (API) an.
- **Ampel**: Die durch die Ampel kodierten Maßnahmen folgen Grenzwerten. Allerdings werden diese evtl. nicht automatisiert angeordnet bzw. wieder aufgehoben. Weiss jemand, wie diese genau wirksam werden?
- **Aufteilung**: Kann eine Tableau-Landing Page im oberen Teil ein dashboard und im unteren Teil redaktionellen Text beinhalten (vgl. Link München)?
  > *TMM*: Klar! Die Seite kann einrichtet werden wie man möchte. Oder eben verschiedene Seiten...
- **Ansichten**: Kann Tableau responsive design?
  > *TMM*: Logo! Es können diverse Anpassungen (Desktop, iPhone, iPad...) vorgenommen werden.
- **Landing Page**: Mein Wunsch wäre, dass die von uns einzurichtende Subdomain (z.B. corona.landshut.de o.ä), welche die landingpage  darstellt (framelösung).
  > *TMM*: Um das zu verstehen: Das Tableau Dashboard soll in die Website eingebettet werden? Das geht und sollte von den ITlern vor Ort problemlos umgesetzt werden können.
 
### Aufgaben
 
- [ ] Stadtkreis und Landkreis Landshut zusammenlegen.
- [ ] Zeitreihen schnellstmöglich hinzufügen.
- [x] Krankebetten-Daten anpassen, d.h., eindeutige Benennung.
- [ ] Ampelfunktion anpassen: Eine Ampel besteht mind. 1 Woche bevor sie wieder heruntergesetzt werden kann. 
  > *TMM*: Höherstufen passiert sofort? Wäre ja logisch. Allerdings werden die Maßnahmen nicht automatisiert angeordnet, oder (s.o.)?
- [ ] Rechtschreibung und Termini überprüfen/korrigieren
