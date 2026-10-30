# Vagtflow

En lille editor til at bygge tidslinjer for vagtfunktioner – fx ASA-vagten – og gemme dem som PDF i A4 eller A5 til udprint.

**[Åbn editoren](https://alangeland.github.io/vagtflow/)** · [Se koden i index.html](index.html)

## Brug

Åbn editoren via linket ovenfor, eller download [index.html](index.html) og åbn filen i en browser. Der er ingen installation eller server.

- **Faser og trin:** Tilføj faser (fx "Eftermiddag", "Morgen") som overskrifter og trin med tidspunkt, titel, beskrivelse, ikon og farve.
- **Punkter:** Linjer i beskrivelsen, der starter med `-` eller `•`, bliver til punktopstilling.
- **PDF:** Vælg A4 eller A5, stående eller liggende, og tryk "Gem som PDF". Lange flows deles over flere sider mellem trinene.
- **Visningstilstand:** Skjuler editoren, så kun tidslinjen vises.

## Eksempel: ASA-vagt

Editoren starter med ASA-vagten som eksempel, delt i to faser:

- **Eftermiddag (inden 17:00):** Fordel ufordelte patienter på Cetrea mellem lunge, gastro, infektion, endokrinologi og nyre, og opret stuegangsaktivitet på Cetrea-tavlen.
- **Morgen:** Find patient til Hobro og skriv gennemgangsnotat, meld patienten til Hobro kl. 07.30, og til morgenkonferencen printes stuegangsseddel via Skyprint, dårlige patienter præsenteres, og antal indlagte nævnes.

Har du allerede egne flows, kan du hente eksemplet ind med knappen **Indlæs ASA-eksempel**. Det ligger også som [asa-vagt.json](asa-vagt.json), som kan indsættes under "Backup og import".

## Data

Flows gemmes kun i den browser, du bruger (`localStorage`). Brug "Backup og import" til at kopiere dine flows som JSON og flytte dem til en anden computer eller browser.

Skriv aldrig patientoplysninger i flows – de er beregnet til arbejdsgange.

## Teknik

Én selvstændig HTML-fil. PDF'en laves i browseren med [html2canvas](https://html2canvas.hertzen.com/) og [jsPDF](https://github.com/parallax/jsPDF), som hentes fra cdnjs.
