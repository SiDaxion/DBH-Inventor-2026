# DBH Inventor 2026

**Schooleigen CAD-configuratie voor Autodesk Inventor 2026**  
Don Bosco Hoboken · Afdeling Mechanica en Lassen

DBH Inventor 2026 bevat de CAD-sjablonen, tekenstandaarden, materialenbibliotheek en projectinstellingen van Don Bosco Hoboken. Eén installatieprogramma stelt Inventor in voor de aangemelde Windows-gebruiker. Nieuwe DBH-versies worden bij het starten automatisch gecontroleerd via GitHub.

> **Belangrijk:** Dit pakket installeert **Autodesk Inventor 2026 zelf niet**. Inventor 2026 moet vooraf geïnstalleerd zijn en correct gelicentieerd worden gebruikt.

## Installeren

1. Open de pagina [Releases](https://github.com/SvenDobbels/DBH-Inventor-2026/releases).
2. Open de recentste vrijgegeven versie en download onder **Assets** het bestand `DBH_Inventor_2026_<versie>_Setup.exe`.
3. Sluit Autodesk Inventor volledig af en voer de gedownloade EXE uit.
4. Doorloop de installatie. Er zijn voor deze installatie in het eigen gebruikersprofiel geen beheerdersrechten nodig.
5. Start voortaan via de bureaubladsnelkoppeling **Inventor 2026 - DBH Mechanica**.

De installer stelt de lokale CAD-configuratie en het persoonlijke Inventor-project automatisch in. Bij een eerste overstap vanuit een oudere DBH-versie worden bestaande werkbestanden waar mogelijk gecontroleerd gekopieerd; de oude werkbestanden worden daarbij niet automatisch verwijderd.

**Voorwaarden:** Windows met Autodesk Inventor 2026 en toegang tot de persoonlijke Windows-map **Documenten**. Voor automatische updates is een internetverbinding nodig. De Documenten-map kan door Windows of de school via OneDrive zijn gesynchroniseerd.

> **Windows-beveiliging:** Omdat de installatie-EXE momenteel geen vertrouwde digitale uitgevershandtekening heeft, kan Microsoft Defender SmartScreen een waarschuwing tonen. Controleer steeds dat de download afkomstig is van deze repository. Schakel SmartScreen niet uit.

## Starten en automatische updates

Bij het openen van de DBH-snelkoppeling:

1. Controleert het startprogramma de lokaal beheerde DBH-bestanden met **SHA-256**.
2. Probeert het gewijzigde of ontbrekende installatiebestanden automatisch te herstellen.
3. Controleert het de openbare GitHub Releases op een nieuwere versie.
4. Downloadt en installeert het een beschikbare, verifieerbare update automatisch.
5. Past het de persoonlijke projectinstellingen toe en start het Autodesk Inventor 2026.

Het PowerShell-venster toont de geïnstalleerde versie, eventuele updateversie en de voortgang.

> **SLUIT HET POWERSHELL-VENSTER NIET** zolang de installatiecontrole, een update of de opstart bezig is. Het venster sluit vanzelf na een succesvolle opstart.

Als GitHub tijdelijk niet bereikbaar is, kan een **lokaal volledig gecontroleerde installatie** normaal blijven starten. Bij een onvolledige installatie of een mislukte update wordt Inventor niet met beschadigde DBH-instellingen gestart.

**OneDrive is geen updatebron.** Alleen de persoonlijke bestanden onder Documenten kunnen via OneDrive worden gesynchroniseerd. Elke Windows-gebruiker heeft een eigen lokale DBH-installatie.

## Mappenstructuur

### 1. Lokale installatie

De CAD-standaarden en scripts staan in:

`%LOCALAPPDATA%\DBH_Inventor_2026\`

```text
DBH_Inventor_2026
├── Configuratie
├── Design Data
├── Materialen
├── Templates
├── DBH_Inventor_2026.ipj      (persoonlijk gegenereerd project)
├── DBH_ProjectBasis.ipj       (projectbasis)
├── DBH_Start.ps1
├── DBH_Config.ps1
├── DBH_Controle.ps1
└── Overige DBH-configuratie- en versiegegevens
```

Hier staan **geen persoonlijke CAD-werkbestanden**. Beheerde bestanden worden bij het starten op integriteit gecontroleerd. Wijzig sjablonen of standaardbestanden daarom niet rechtstreeks in deze map.

### 2. Persoonlijke CAD-bestanden

De persoonlijke bestanden staan onder de werkelijke Windows-map **Documenten**:

`Documenten\DBH_Inventor_2026\`

```text
DBH_Inventor_2026
├── ContentCenter
└── Werkmap
    ├── Onderdelen
    ├── Samenstellingen
    ├── Tekeningen
    └── Presentaties
```

| Map | Inhoud |
| --- | --- |
| `ContentCenter` | Door Inventor gegenereerde Content Center-onderdelen |
| `Werkmap\Onderdelen` | Onderdeelbestanden (`.ipt`) |
| `Werkmap\Samenstellingen` | Samenstellingsbestanden (`.iam`) |
| `Werkmap\Tekeningen` | Tekeningen (`.idw`) |
| `Werkmap\Presentaties` | Presentaties (`.ipn`) |

**Let op:** `ContentCenter` staat **naast** `Werkmap`, niet erin.

Het daadwerkelijke pad naar Documenten wordt door Windows bepaald en kan bijvoorbeeld in een OneDrive-locatie liggen. De configuratie gebruikt daarom geen vaste Windows-gebruikersnaam.

### 3. Lokaal installatiebeheer

Technische logboeken, de launcher en herstelbestanden bevinden zich afzonderlijk in:

`%LOCALAPPDATA%\DBH_Inventor_2026_Beheer\`

```text
DBH_Inventor_2026_Beheer
├── Herstel
├── DBH_Launcher.ps1
└── Log-, status- en beheerbestanden
```

Deze map bevat geen persoonlijke CAD-projecten.

## Deïnstalleren

Open **Windows-instellingen → Apps → Geïnstalleerde apps**, zoek **DBH Inventor 2026** en kies **Verwijderen**.

De uninstaller verwijdert de door DBH beheerde lokale installatie, de bijbehorende beheerbestanden en de DBH-bureaubladsnelkoppeling. **Autodesk Inventor 2026 zelf wordt niet verwijderd.**

> **Persoonlijke bestanden blijven behouden:** `Documenten\DBH_Inventor_2026\Werkmap` en `Documenten\DBH_Inventor_2026\ContentCenter` worden niet door de uninstaller verwijderd. Verwijder ze alleen zelf, na controle dat je ze niet meer nodig hebt.

Onbekende, niet door de installer beheerde bestanden in de lokale installatiemap worden veiligheidshalve niet zomaar gewist. Daardoor kan uitzonderlijk een restmap achterblijven.

## Problemen en verbeteringen melden

Gebruik [GitHub Issues](https://github.com/SvenDobbels/DBH-Inventor-2026/issues) om een fout of verbeterpunt te melden. Vermeld bij voorkeur:

- De gebruikte DBH-versie.
- Wat je probeerde te doen.
- De exacte foutmelding en de stappen waarmee je het probleem kunt herhalen.

Voeg geen persoonsgegevens, wachtwoorden of vertrouwelijke leerlingbestanden toe aan een openbaar issue.

## Voor ICT en beheerders

De installatie vindt plaats **per Windows-gebruiker** in `%LOCALAPPDATA%`. Een stille installatie is mogelijk in de context van de aangemelde gebruiker, bijvoorbeeld:

```powershell
DBH_Inventor_2026_2.0-rc.1_Setup.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

Voer die installatie niet onder het `SYSTEM`-account uit wanneer de installatie voor het profiel van de aangemelde leerling bedoeld is. Bij gebruikersprofielen die na afmelden worden gewist, moet de installatie bij een volgende aanmelding opnieuw worden voorzien.

Voor het zelf bouwen van een installatiepakket: pak het goedgekeurde DBH-bouwpakket uit, voer `DBH_Bouw_EXE.cmd` uit en controleer het bouwrapport. Hiervoor is **Inno Setup 6.3 of nieuwer** nodig. Publiceer een nieuwe EXE pas na de nodige integriteits- en Windows-/Inventor-tests als nieuwe GitHub Release met de bijbehorende versietag.

## Versies

**Actuele bevestigde referentieversie: `2.0-rc.1`.** Dit is een releasecandidate. Downloadbare versies staan onder [Releases](https://github.com/SvenDobbels/DBH-Inventor-2026/releases); openstaande verbeterpunten onder [Issues](https://github.com/SvenDobbels/DBH-Inventor-2026/issues).

---

*DBH Inventor 2026 is een schooleigen configuratie van Don Bosco Hoboken voor gebruik met Autodesk Inventor 2026. Het is geen afzonderlijke Autodesk-softwarelicentie.*
