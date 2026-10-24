# DBH Inventor 2026

**Schooleigen CAD-omgeving voor Autodesk Inventor 2026**  
Don Bosco Hoboken | Afdeling Mechanica en Lassen

DBH Inventor 2026 richt Autodesk Inventor 2026 in volgens de CAD-standaarden van de school. Leerlingen en leerkrachten kunnen via één bureaubladsnelkoppeling met de juiste projectinstellingen, sjablonen en materialen werken. De toepassing controleert de beheerde schoolbestanden, kan deze zo nodig veilig herstellen en controleert op goedgekeurde stabiele updates.

> **Let op:** DBH Inventor 2026 installeert Autodesk Inventor zelf niet en verstrekt geen Autodesk-licentie. Autodesk Inventor 2026 moet al correct geïnstalleerd en gelicentieerd zijn.

## Wat bevat DBH Inventor 2026?

- Schooleigen sjablonen voor onderdelen, plaatwerk, samenstellingen, lasconstructies, tekeningen en presentaties.
- Bijbehorende **Design Data**, materialenbibliotheek en Application Options.
- Een persoonlijk Inventor-project met afzonderlijke **Werkmap** en **ContentCenter**.
- Een grafisch startprogramma dat de CAD-omgeving controleert, updates verwerkt en Inventor opstart.
- Controle en herstel van beheerde schoolbestanden, met bescherming van persoonlijke CAD-bestanden.

## Vereisten

- Een Windows-computer met een ondersteunde 64-bits omgeving.
- **Autodesk Inventor 2026**, vooraf geïnstalleerd en correct gelicentieerd.
- Een toegankelijk persoonlijk Windows-gebruikersprofiel met opslagruimte voor de Werkmap en ContentCenter.
- Internettoegang voor het ophalen van de installatiebestanden en automatische updates. Een reeds volledige en gecontroleerde installatie kan bij tijdelijke onbereikbaarheid van GitHub doorgaans lokaal starten.

De DBH-hoofdsoftware wordt **per Windows-gebruiker** geïnstalleerd. Voor de gebruikelijke installatie in het eigen profiel zijn geen beheerdersrechten vereist. Beveiligingsbeleid op beheerde schoolcomputers kan aanvullende toestemming of toelating door ICT vereisen.

## Installeren

1. Open de [GitHub Releases](https://github.com/SiDaxion/DBH-Inventor-2026/releases).
2. Kies de **nieuwste stabiele release van de hoofdsoftware** en download het bijbehorende installatiebestand (`Setup.exe`) onder **Assets**. De apart aangeduide schoolbootstrap is niet dezelfde installatie.
3. Sluit Autodesk Inventor volledig af.
4. Voer het installatiebestand uit en doorloop de stappen.
5. Start de toepassing via de bureaubladsnelkoppeling **Inventor 2026 - DBH Mechanica**.

Gebruik bij voorkeur de door school-ICT voorgeschreven installatiewijze als de computer centraal beheerd wordt.

## Starten, controleren en bijwerken

De grafische DBH-launcher doorloopt vier stappen:

**Controleren → Updates → Voorbereiden → Inventor starten**

Bij het starten controleert DBH de installatie en de beheerde schoolstandaarden. Ontbrekende of afwijkende bestanden kunnen worden hersteld vanuit een gecontroleerde lokale installatiebron. Afwijkende, niet-herkende schoolbestanden worden waar nodig eerst veilig gearchiveerd. Persoonlijke CAD-werkbestanden maken geen deel uit van deze opschoning.

DBH controleert via GitHub of er een nieuwere, goedgekeurde **stabiele** hoofdrelease beschikbaar is. Updates worden gecontroleerd op onder meer versie, bestandsgrootte en SHA-256 voordat de installatie verdergaat. Er wordt niet automatisch naar een oudere versie of een prerelease overgeschakeld.

De technische details van de opstartcontrole zijn afzonderlijk beschikbaar in de launcher.

## Persoonlijke Werkmap en ContentCenter

Persoonlijke CAD-bestanden worden gescheiden gehouden van de beheerde installatiebestanden. DBH gebruikt daarvoor een locatie onder de persoonlijke **Documenten**-map of, wanneer geschikt en beschikbaar, de **school-OneDrive**.

Bij de eerste inrichting krijgt de geschikte school-OneDrive de voorkeur. Anders wordt Windows Documenten gebruikt. Een bestaande opslaglocatie wordt niet stilzwijgend verplaatst. Als de school-OneDrive later beschikbaar komt, kan DBH een gecontroleerde migratie voorstellen met de keuzes **Migreren** en **Nu niet**.

De persoonlijke opslag heeft deze indeling:

```text
DBH_Inventor_2026/
├── Werkmap/
│   ├── Onderdelen/
│   ├── Samenstellingen/
│   ├── Tekeningen/
│   └── Presentaties/
└── ContentCenter/
```

De werkelijke locatie wordt door Windows en de bestaande DBH-configuratie bepaald. **Verplaats of verwijder deze mappen niet handmatig zonder een geschikte back-up en controle.**

De beheerde programmabestanden en technische componenten staan afzonderlijk onder `%LOCALAPPDATA%`. Een onafhankelijk archief kan daar eveneens worden bijgehouden.

## Schooluitrol en ICT

Voor centraal beheerde leerlingcomputers bestaat een **afzonderlijk onderhouden schoolbootstrap**. ICT kan hiermee de voorbereiding en eerste installatie per aangemelde Windows-gebruiker organiseren. De bootstrap en de volledige hoofdsoftware hebben een eigen versienummer en een afzonderlijke release.

De bootstrap is geen vervanging voor Autodesk Inventor 2026. Voor schooluitrol moeten ICT-beleid, gebruikersrechten, SmartScreen en andere Windows-beveiligingsmaatregelen worden gerespecteerd. Raadpleeg de technische informatie en bijbehorende bestanden van de toepasselijke [bootstraprelease](https://github.com/SiDaxion/DBH-Inventor-2026/releases).

## Verwijderen

Verwijder **DBH Inventor 2026** via **Windows-instellingen → Apps → Geïnstalleerde apps**.

De verwijderprocedure ruimt de door DBH beheerde installatie- en beheeronderdelen op. **Persoonlijke Werkmap, ContentCenter en bestanden in de school-OneDrive blijven behouden.** Ook het onafhankelijke archief wordt niet automatisch als persoonlijke werkmap behandeld. Autodesk Inventor 2026 zelf wordt niet verwijderd.

## Ondersteuning en versies

- [Releases en downloadbestanden](https://github.com/SiDaxion/DBH-Inventor-2026/releases)
- [Problemen melden of verbeteringen voorstellen](https://github.com/SiDaxion/DBH-Inventor-2026/issues)

De **releaseopmerkingen** bevatten per versie de nieuwe functies, verbeteringen, opgeloste problemen en eventuele installatieaandachtspunten. Deze README beschrijft de algemene werking en wordt alleen aangepast wanneer de productwerking of installatieprocedure structureel verandert.

Vermeld bij een foutmelding de gebruikte DBH-versie, de uitgevoerde handeling en de exacte melding. Deel geen wachtwoorden, persoonsgegevens of vertrouwelijke leerlingbestanden in openbare GitHub Issues.

---

*DBH Inventor 2026 is een schooleigen configuratie voor Autodesk Inventor 2026. Het is geen officieel Autodesk-product en bevat geen Autodesk-softwarelicentie.*
