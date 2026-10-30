# Vagtflow

En lille editor til at bygge tidslinjer for vagtfunktioner – fx ASA-vagten – og gemme dem som PDF i A4 eller A5 til udprint.

## Brug

Åbn `index.html` i en browser. Der er ingen installation eller server.

- **Faser og trin:** Tilføj faser (fx "Eftermiddag", "Morgen") som overskrifter og trin med tidspunkt, titel, beskrivelse, ikon og farve.
- **Punkter:** Linjer i beskrivelsen, der starter med `-` eller `•`, bliver til punktopstilling.
- **PDF:** Vælg A4 eller A5, stående eller liggende, og tryk "Gem som PDF". Lange flows deles over flere sider mellem trinene.
- **Visningstilstand:** Skjuler editoren, så kun tidslinjen vises.

## Data

Flows gemmes kun i den browser, du bruger (`localStorage`). Brug "Backup og import" til at kopiere dine flows som JSON og flytte dem til en anden computer eller browser.

Skriv aldrig patientoplysninger i flows – de er beregnet til arbejdsgange.

## Teknik

Én selvstændig HTML-fil. PDF'en laves i browseren med [html2canvas](https://html2canvas.hertzen.com/) og [jsPDF](https://github.com/parallax/jsPDF), som hentes fra cdnjs.
