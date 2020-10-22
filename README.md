# CoViD-19 Dashboard für Deutschland & Bayern



## Allgemeine Version


## Freistaat Bayern mit Focus Landshut

### TEAM

- [Thomas Rogler](https://www.linkedin.com/in/tom-rogler-6405bbb1/), Initiator, Landkreis-Experte
- [Thomas Massie](https://www.linkedin.com/in/thomasmmassie/), Backend & Frontend Development
- [Thomas Hofmann](https://www.linkedin.com/in/thomas-hofmann-a2817646/), WHO, Experte

### ZIELSETZUNG

- Erstellung eines CoViD-19 Dashboards mit den wichtigsten Kennzahlen für Bayern und Landshut.
- Schneller Überblick und leicht verständlich (selbsterklärend).
- BetrachterIn bekommt ein Gefühl für die Dynamik der Pandemie.
- Vergleiche mit anderen Stadt-/Landkreisen sind möglich; dadurch kann die eigene Lage eingeordnet werden.

### DATEN

Die Daten sollen möglichst aus einer Quelle bzw. von einem Anbieter stammen, und über eine API abgerufen werden können. Dies garantiert aktuelle Daten und einen einheitlichen Standard. Deshalb beziehen wir alle Daten vom [NPGEO Corona Hub 2020](https://npgeo-corona-npgeo-de.hub.arcgis.com/), welche über die Acrgis REST API bezogen werden.

#### Datenquellen

- **aktuelle Zahlen** (neuester Stand): [RKI Corona Landkreise](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/917fc37a709542548cc3be077a786c17_0/geoservice) mit folgender Abfrage URL: https://services7.arcgis.com/mOBPykOjAyBO2ZKk/arcgis/rest/services/RKI_Landkreisdaten/FeatureServer/0/query?where=1%3D1&outFields=*&outSR=4326&f=json
- **Zeitreihen**: [RKI COVID19](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/dd4580c810204019a7b8eb3e0b329dd6_0/geoservice) mit folgender Abfrage URL: https://services7.arcgis.com/mOBPykOjAyBO2ZKk/arcgis/rest/services/RKI_COVID19/FeatureServer/0/query?where=1%3D1&outFields=*&outSR=4326&f=json
- **Intensivbettenbelegung**: [DIVI-Intensivregister auf Landkreisebene](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/8fc79b6cf7054b1b80385bda619f39b8_0/geoservice) mit folgender Abfrage URL: https://services7.arcgis.com/mOBPykOjAyBO2ZKk/arcgis/rest/services/DIVI_Intensivregister_Landkreise/FeatureServer/0/query?where=1%3D1&outFields=*&outSR=4326&f=json

### PROTOTYP

Der Prototyp befindet sich auf Tableau Public und kann [hier](https://public.tableau.com/profile/thomas.massie#!/vizhome/CoViD-19---Bayern-Prototype01---Test/Dashboard) aufgerufen werden.

Aktuell sieht dieser so aus:
![Prototyp](https://github.com/thomassie/CoViD-19---Germany/blob/main/04---Screenshots/Bildschirmfoto%202020-10-22%20um%2016.59.32.png)
![Prototyp](https://github.com/thomassie/CoViD-19---Germany/blob/main/04---Screenshots/Bildschirmfoto%202020-10-22%20um%2016.59.52.png)

### OFFENE FRAGEN

**Grundsätzliche Fragen**:

- **Ziel**: Welchen Zweck soll das Dashboard erfüllen? Wer ist die Zielgruppe?
- **Inhalte**: Welche Inhalte sollen wie vermittelt werden? Was ist das Hauptmedium? Soll Tableau in eine HTML5-Seite eingebettet werden?
- **Rechte**: Wer hält die Rechte am Dashboard?
- **Aufwandsentschädigung**: Wie sollen die Beteiligten für ihre Arbeit am Dashboard entschädigt werden?

**Allgemeine Fragen**:

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
- **Input**: Können in tableau Daten surveygesteuert hochgeladen oder redaktionell (über ein backend) gepflegt werden?
  > *TMM*: Natürlich kann eine .csv- oder .xlsx-Datei eingebettet werden. Allerdings muss die Datei manuell gepflegt und aktualisiert werden. Wer ist dazu in der Lage? Was bedeutet "surveygesteuert"?
- **Dashboard und Speicherort**: Wer aktualisiert das Dashbaord? Wer kümmert sich um einen Speicherort (Repository) von welchem aus alle zugegreifen können?
- **AJAX**: Kann Tableau AJAX? Vor einigen Jahren waren AJAX Lösungen mal ganz hip. Da konnte man sich als User - ganz individuell - seine favorosierten Seiteninhalte selbst zusammenklicken und positionieren.
  > *TMM*: Keine Ahnung. Aber Tableau funktioniert nicht so, dass man sich als Nutzer die Anordnung aussuchen kann. Ich hatte zunindest noch kein deratiges Dashboard gesehen. Zielgruppen müssen vorab definiert werden um ein effektives Dashboard zu erstellen. Ansonsten wird schlicht keine zufriedenstellende Wirking erzielt.
- **Akordeon-Effekte**: Kann Tableau Akkordeon? Ich hab mal eine typo3 extension mit einer Akordeonfunktion in Betrieb genommen. Hier konnte man sich thematische Absätze über ein plus- bzw. minusicon ein- bzw. ausblenden.
  > *TMM*: Nee. Aber man kann bestimmt Inhalte natürlich ein- bzw- ausblenden (Filter, Parameter). Das geht auch in Tabellen. Aber halt nicht mit einem Akkordeon-Effekt.
 
### AUFGABEN
 
- [ ] Stadtkreis und Landkreis Landshut zusammenlegen.
- [ ] Zeitreihen schnellstmöglich hinzufügen.
- [x] Krankebetten-Daten anpassen, d.h., eindeutige Benennung.
- [ ] Ampelfunktion anpassen: Eine Ampel besteht mind. 1 Woche bevor sie wieder heruntergesetzt werden kann. 
  > *TMM*: Höherstufen passiert sofort? Wäre ja logisch. Allerdings werden die Maßnahmen nicht automatisiert angeordnet, oder (s.o.)?
- [ ] Rechtschreibung und Termini überprüfen/korrigieren
- [x] Demografische Verteilungen der Fälle filtern (über *Dashboard Actions* auf *Worksheet* im *Viz in Tooltip*).

### ZEITERFASSUNG

- Thomas Massie: 30 Stunden (Stand 22.10.2020, 17:30 Uhr)
