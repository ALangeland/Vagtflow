# Vagtflow

En lille editor til at bygge tidslinjer for vagtfunktioner – fx ASA-vagten – og gemme dem som PDF i A4 eller A5 til udprint.

**[Åbn editoren](https://alangeland.github.io/Vagtflow/)** · [Se koden i index.html](index.html)

## Brug

Åbn editoren via linket ovenfor, eller download [index.html](index.html) og åbn filen i en browser. Der er ingen installation eller server.

- **Faser og trin:** Tilføj faser (fx "Eftermiddag", "Morgen") som overskrifter og trin med tidspunkt, titel, beskrivelse, ikon og farve.
- **Sortering:** Træk i ⠿ for at flytte trin og faser, eller brug pilene.
- **Punkter:** Linjer i beskrivelsen, der starter med `-` eller `•`, bliver til punktopstilling.
- **PDF:** Vælg A4 eller A5, stående eller liggende, og tryk "Gem som PDF". Lange flows deles over flere sider mellem trinene.
- **Visningstilstand:** Skjuler editoren, så kun tidslinjen vises.

## Eksempel: ASA Vagt

Editoren starter med ASA-vagten som eksempel:

- **15:00:** Overtag telefonen fra afgående vagt i ASA-konferencelokalet.
- **Inden 17:00:** Fordel ufordelte patienter med "Akut medicin" på Cetrea til lunge, gastro, infektion, endokrinologi og nyre, og opret "Aften"-stuegangsaktiviteter, så de stuegangsgående læger kan se patienterne.
- **Morgen:** Udvælg en patient til overflytning til Hobro med vurdering og overleveringsnotat, og meld patienten til medicinsk bagvagt i Hobro kl. 07.30.
- **Morgenkonference kl. 08.00:** Print stuegangsseddel via Skyprint inden konferencen, præsentér dårlige patienter fra vagten, og nævn det totale antal indlagte.

Har du allerede egne flows, kan du hente eksemplet ind med knappen **Indlæs ASA-eksempel**. Det ligger også som [asa-vagt.json](asa-vagt.json), som kan åbnes med "Åbn fil" under "Backup og import".

## Data

Ændringer gemmes automatisk i den browser, du bruger (`localStorage`), og du kan trykke **Gem flow** for at gemme med det samme. Status ved knappen viser, hvornår der sidst er gemt.

Vil du have flowet med til en anden computer eller browser, så brug **Gem flow som fil** under "Backup og import" og åbn filen igen med **Åbn fil**.

Skriv aldrig patientoplysninger i flows – de er beregnet til arbejdsgange.

## Teknik

Én selvstændig HTML-fil. PDF'en laves i browseren med [html2canvas](https://html2canvas.hertzen.com/) og [jsPDF](https://github.com/parallax/jsPDF), som hentes fra cdnjs.
