# GWSW Maatregelen

<!-- gebruik voor lokaal editen -->
<script src="./builds/respec-rioned.js"></script>

<style>
  .symbolSmall{width:20px;height:20px;margin-right:1em;vertical-align:middle}
  .symbol{width:30px;height:30px;margin-right:1em;vertical-align:middle}
</style>

Vanuit Stichting RIONED is Eric Oosterom de verantwoordelijk projectmanager. Vragen over de module en de totstandkoming en vaststelling ervan kunt u stellen via gwsw@rioned.org. 

De module GWSW-Maatregelen is in opdracht van Stichting RIONED ontwikkeld door Hans van Keeken en Roel Golsteijn (beiden Kragten), in samenwerking met de werkgroep GWSW-Maatregelen (hierna te noemen “werkgroep”), bestaande uit:
- Walter Kuhn, gemeente Almere
- Leo Bloedjes, gemeente Almere
- Alex Buijs, gemeente Breda
- Eric van Gorkom, I-sago en gemeente Roosendaal
- Wouter van Riel, Infralytics en GWSW-modelleerteam namens Stichting RIONED
- Erwin Schreve, namens gemeente Leiden
- John Wouters, gemeente Rotterdam
- Steven Oterdoom, gemeente Zaandam

# Inleiding

## Achtergrond en inleiding

De afgelopen jaren heeft er een flinke inhaalslag plaatsgevonden in standaardisatie van beheer en onderhoud van de riolering. Er zijn andere normen van toepassing verklaard, er zijn nieuwe normen opgesteld, binnen het CROW heeft een actualisatie van de hoofdstukken voor rioolrenovatie, reiniging en inspectie plaatsgevonden en Stichting RIONED heeft de “Leidraad voor het visueel inspecteren van de buitenriolering volgens NEN-EN 13508-2” (document 2023-01), het rapport “Classificeren van toestandsaspecten van rioolleidingen en -putten vastgelegd volgens NEN-EN 13508-2” (document 2019-02) met de bijbehorende classificatiemethodiek en het “Model Programma van Eisen visuele inspectie” (document 2019-03) opgesteld.

Binnen het gehele proces van beheer, onderhoud en vervanging van de riolering heeft een opdrachtgever te maken met verschillende stakeholders. Dit kunnen afdelingen zijn binnen de eigen organisatie, externe adviseurs en/of uitvoerende partijen. Om alle deelprocessen in goede banen te leiden, is een goede data-uitwisseling essentieel. Het gaat er hierbij om welke informatie er bij welk proces heen en terug gestuurd moet worden. Hierbij is ***heen*** de informatie waarmee de actienemer de actie uit kan voeren en ***terug*** het resultaat van de uitgevoerde actie.

Door gebruik te maken van gestandaardiseerde open data en eenduidige terminologie is het mogelijk om op een efficiënte en vergelijkbare wijze de informatie uit te wisselen. Dit vereenvoudigt en verbetert de processen.

Het Gegevenswoordenboek Stedelijk Water (GWSW) is de open datastandaard waar Stichting RIONED met en namens alle relevante partijen aan werkt. Met het GWSW worden komende jaren alle objecten en hun gegevens, hun onderlinge relaties, en de beheeractiviteiten binnen het domein stedelijk water eenduidig gedefinieerd en vastgelegd ten behoeve van soepele gegevensuitwisseling en beter beheer. Meer informatie daarover vindt u via [www.riool.net/gwsw](http://www.riool.net/gwsw).

De riolering en een deel van de afvalwaterketen kan al worden beschreven met het GWSW (o.a. Basis en Minimale Dataset, Rib en RibX, Hyd). GWSW-Maatregelen is in het verleden al een keer in concept opgesteld, maar is destijds niet vastgesteld.

Vanuit gebruikers is aan Stichting RIONED gevraagd om het GWSW geschikt te maken om als bron te dienen voor de uitwisseling op het gebied van maatregelen. Dit wordt beschreven in GWSW-Maatregelen, waarvan dit document de specificatie is. GWSW-Maatregelen is opgebouwd uit meerdere onderdelen:

1. Semantiek (uniforme termen en definities, woordenboek, de taal van mensen gestructureerd zodat applicaties/machines het ook kunnen gebruiken) en ordening in een soortenboom;

2. Registratie van objecten/projecten/maatregelen (= minimale datasets en optionele velden), bedoeld voor uitwisselen en delen;

3. Validatie van (project)datasets (=kwaliteitseisen, conformiteitsklassen).

Onderdelen 1 en 2 zijn uitgewerkt in hoofdstukken 2 en 3/4, onderdeel 3 is nog niet uitgewerkt in dit document. Dat volgt na vaststelling van onderdeel 2.

Dit beschrijvende document is begin 2023 opgeleverd door de werkgroep voor toetsing door een grotere groep rioleringsbeheerders, adviseurs en aannemers in het voorjaar van 2023. Vervolgens zal in een aantal proefprojecten bij enkele gemeenten in samenwerking met de daar werkzame marktpartijen de specificatie van GWSW-Maatregelen getoetst worden op werkbaarheid en volledigheid. Ook zal getoetst worden welke potentiële knelpunten in beheer- en andere software zou kunnen optreden. Belangstellenden om ook in hun situatie een proefneming te doen, kunnen zich melden via gwsw@rioned.org.

Beoogd is eind 2023 een verbeterde versie van deze specificatie van GWSW-Maatregelen op te leveren voor consultatie en uiteindelijk vaststelling in een volgende versie van het Gegevenswoordenboek Stedelijk Water.

De algemene beschrijving van het GWSW model vindt u op [data.gwsw.nl](https://data.gwsw.nl/). De datamodellen GWSW-Basis en Minimale Dataset (operationeel beheer), GWSW-Rib en RibX (inspectie en reiniging van leidingen, putten en kolken), GWSW-Hyd (hydraulische modellering), GWSW-Kengetallen (afvalwaterprognoses) en GWSW-Geo (GIS-toepassingen) zijn al eerder vastgestelde onderdelen van het GWSW. Een set van basistools rondom GWSW vindt u op [apps.gwsw.nl](http://apps.gwsw.nl/). Voor de details van het datamodel zie [data.gwsw.nl/maatregelen](https://data.gwsw.nl/maatregelen).

## Scope
De scope van GWSW-maatregelen is beperkt tot activiteiten aan bestaande objecten. Het aanleggen van objecten valt vooralsnog buiten de scope van GWSW-Maatregelen en kan in een later stadium als uitbreiding worden meegenomen.

## Leeswijzer

In hoofdstuk 2 zijn de maatregeltypen beschreven. De conclusie uit de werkgroep overleggen is dat de omschrijving van de maatregelen zo vereenvoudigd als mogelijk plaats dient te vinden, doch gebruik te maken van een nadere uitsplitsing van maatregelen indien daar behoefte aan is.

In hoofdstuk 3 zijn de verschillende processtappen beschreven in het beheer, onderhoud, renovatie en vervanging van de riolering en op welke momenten data -uitwisseling plaats vindt.

In hoofdstuk 4 zijn de processtappen nader beschreven en is per processtap aangegeven welke informatie er heen en terug gestuurd dient te worden om deze processen in goede banen te leiden. De informatie behoefte is in tabelvorm uitgewerkt.

## Uitwisselformaat

Dit document bevat een specificatie van de <u>inhoudelijke</u> gegevensbehoefte en gegevensuitwisseling bij de verschillende processtappen rondom het kiezen en uitvoeren van maatregelen in en aan de openbare riolering. Het beschrijft het ‘wat’. Oftewel welke informatie en data de beheerders en marktpartijen minimaal nodig hebben om hun werk goed te kunnen doen. Deze gegevensbehoefte zal worden gemodelleerd in het Gegevenswoordenboek Stedelijk Water. Vervolgens zal gespecificeerd worden hoe uitwisseling van deze data binnen de werkprocessen (processtappen) van beheerders en marktpartijen zal plaatsvinden. Daarbij zal verkend worden of naast het standaard RDF formaat (OroX) voor alle GWSW gerelateerde informatie, ook een ander formaat zoals XML (RibX) noodzakelijk is om in uitwisselingsbehoefte te voorzien.

# Omschrijving maatregelen

In de eerste (concept-)versie van GWSW-maatregelen voor vrijverval rioolleidingen van een aantal jaren geleden zijn onder de activiteit Maatregel onderstaande maatregeltypen c.q. activiteiten gegroepeerd.

**Maatregeltypen/activiteiten:**

- Aanleggen
- Buiten gebruik stellen
- Conserveren
- Onderhouden
- Onderzoeken
- Renoveren
- Repareren
- Vervangen
- Verwijderen

Binnen elk maatregeltype is een verdere uitsplitsing gemaakt naar de beschrijvende maatregel. De beschrijving van deze maatregelen is opgebouwd uit de samenvoeging van de maatregel met het object of met het toestandsaspect.

Zo is bijvoorbeeld bij het maatregeltype vervangen onderscheid gemaakt in de subtypes:

-   Rioolput vergroten
-   Rioolput vervangen
-   Vrijverval rioolleiding vervangen
    -   Sleufloos vervangen
        -   Pipe bursting
        -   Pipe eating

In de aanloop naar de actualisatie van GWSW-Maatregelen is binnen de werkgroep nagedacht in hoeverre deze concept opzet bruikbaar is. Door het maatregeltype “vervangen” te koppelen aan een object conform de decompositie van GWSW‑basis, én gebruik te maken van de headergegevens uit het GWSW-RibX, ligt de maatregel automatisch vast. Ditzelfde geldt voor maatregeltypen aan toestandsaspecten. Door het subtype “vrijmaken leidingprofiel” van het maatregeltype “Onderhouden” te koppelen aan een toestandsaspect, ligt ook hiermee automatisch vast dat het gaat om het verwijderen van een doorgestoken inlaat, wortels, afzetting of dergelijke.

De conclusie uit de werkgroep is dat door de maatregel op een zo hoog mogelijk niveau in de soortenboom te beschrijven en deze te koppelen aan een object of aan een toestandsaspect, er een flinke vereenvoudiging kan plaatsvinden. Dit komt de leesbaarheid ten goede en GWSW-Maatregelen is hierdoor toekomstbestendiger omdat niet bij elke wijziging in objecttypen ook meteen de mogelijkheden binnen GWSW-Maatregelen hoeven te worden aangepast.

# Processtappen

## Te onderscheiden processtappen

Binnen het proces van beheer, onderhoud, renovatie en vervangen van de riolering zijn een aantal generieke processtappen te onderscheiden. Als voorbeeld zijn in onderstaande afbeelding acties aan een kolkaansluitleiding opgenomen.

<img src="media/image7.png" style="width:5.90486in;height:2.31667in" />

Afbeelding: Voorbeeld acties aan kolkaansluitleiding (Afbeelding afkomstig van Wouter van Riel.)

Vanuit bovenstaande afbeelding kunnen generieke processtappen 1 t/m 7 worden samengevat die gelden voor zowel rioolleidingen als rioolputten:

1.  Initiëren reiniging en inspectie
2.  Uitvoeren reiniging en inspectie en aanleveren waarnemingen
3.  Beoordelen inspecties en opstellen maatregeladvies
4.  Vaststellen definitieve maatregel
5.  Opstellen contract
6.  Uitvoeren maatregelen
7.  Verwerken in beheerdata

Tijdens het uitvoeren van deze processtappen dient er informatie via een uitwisselbestand heen en terug te worden uitgewisseld. De stappen zijn in de navolgende paragraaf tekstueel uitgewerkt. Stappen 1 en 2 zijn uitvoerig in het GWSW-RibX beschreven en worden hier niet herhaald. Voor deze stappen wordt verwezen naar het huidige GWSW-RibX.

Stap 7, het verwerken van de gegevens in de beheerdata, staat in deze opsomming als laatste stap aangegeven nadat de benodigde maatregelen zijn uitgevoerd. In de praktijk zal bij elke stap telkens ook (een deel van) de beheerdata worden geactualiseerd.

## Processchema

Een voorbeeld van een processchema met de stappen 1 t/m 7 met de daarbij horende data-uitwisseling is in afbeelding 2 weergegeven. In dit schema is geen directe link tussen de verschillende processtappen opgenomen. Uitwisseling geschiedt via de data-uitwisseling plaats met een “Heen” en “Terug” bestand per processtap. Er is bewust voor gekozen om een processtap niet volledig als een stroomschema uit te werken. Processen kunnen per opdrachtgever verschillen en het uitwerken ervan behoort niet tot de scope van GWSW-Maatregelen.

<img src="media/image8.png" style="width:5.728in;height:9.16763in" />

Afbeelding: Processtappen en data-uitwisseling

Het uitgangspunt dat bij afbeelding 2 is gehanteerd, is dat de benodigde controles en hoe om te gaan met verbeteringen, binnen deze processtappen zelf plaats vindt.

Het resultaat van een voorgaande processtap wordt gebruikt als input voor een opvolgende stap. Bij het opstellen van de benodigde informatie-uitwisseling is informatie die voor een vervolgstap niet meer nodig is, buiten de informatieoverdracht gehouden. Dat houdt in dat een terug bestand uit een voorgaande processtap niet per definitie gelijk hoeft te zijn aan het heen bestand voor de volgende processtap.

Tevens geldt dat aan het initiëren van een reiniging en inspectie (stap 1) ook een contract ten grondslag kan liggen. In dat geval is eerst sprake van het opstellen van een contract (stap 5) voordat een programma reiniging en inspectie wordt geïnitieerd (stap 1). Dit geldt ook bij raamovereenkomsten met zowel reinigen en inspecteren van de riolering als onderhoud/renovatie.

## Processtappen en informatieoverdracht

De processtappen uit hoofdstuk 3 zijn in hoofdstuk 4 nader uitgewerkt. Per processtap is ook aangegeven welke benodigde informatie er uitgewisseld dient te worden.

Bij de uit te wisselen informatie in de navolgende paragrafen is telkens in de laatste kolom onder “betreft” aangegeven om welk soort informatie het gaat:

- H = Headerinformatie van het object
- T = Informatie van het toestandsaspect
- P = Projectinformatie

> **TOELICHTING:** Kolom “veld” in tabellen 2 t/m 6 is tijdelijk en bevat informatie voor de modelleurs. Dit is informatie welke straks in het definitieve beschrijvend document niet meer terug komt.

In de tabellen met informatie-uitwisseling staan de vullingsvoorschriften in twee kolommen:

- “Heen”: de veldvulling in een vooraf aangeleverd bestand.
- “Terug”: de veldvulling in een terug te ontvangen bestand (resultaten van het proces).

De kolommen “Heen” en “Terug” gebruiken de volgende codes:

<table>
<caption>Codering voor de vullingsvoorschriften</caption>
</table>

| Code | Voorschrift veldvulling in bestand                                          |
|:-----|:----------------------------------------------------------------------------|
|      | Geen code in kolom “Heen”: Niet vooraf invullen                             |
|      | Geen code in kolom “Terug”: Niet achteraf invullen (terug zonder wijziging) |
| O    | Optioneel                                                                   |
| A    | Altijd                                                                      |


Als voor de kolom “Heen” geldt dat het gegeven verplicht is (A) en het gegeven ontbreekt in het terug te ontvangen bestand, dan moet de opdrachtgever met de opdrachtnemer afspraken maken over de levering. Wanneer het gegeven voor zowel “Heen” als “Terug” verplicht is (A) en het “Heen”-gegeven is fout of ontbreekt (nieuw object, niet vooraf ingevuld), dan moet de opdrachtnemer dit gegeven – als het bekend is – altijd bij de uitvoering van het proces corrigeren of aanvullen.

Stap 1: Initiëren reiniging en inspectie.
-----------------------------------------

Reiniging en inspectie zijn reeds beschreven in het GWSW-RibX. Zie het uitwisselbestand conform paragraaf 6.3, 6.4 en 6.5 (resp. inspectie leidingen, putten en kolken) uit de beschrijving van het GWSW-RibX ([www.riool.net/ribx](http://www.riool.net/ribx)). Uit analyse van deze tabellen blijkt dat er bij leidingen geen verschil is tussen een rioolleiding en een aansluitleiding. Het GWSW-RibX voor een rioolleiding is identiek aan dat van een aansluitleiding en kent alleen afwijkende veldcodes. In de inhoud van de velden zit geen tegenstrijdigheid.

Tussen een rioolput en een kolk zijn wel verschillen. In de beschrijving van het GWSW-RibX komen velden voor die alleen bij een rioolput gelden en velden die alleen bij een kolk gelden. Overige velden komen met elkaar overeen. Uitzonderingen hierop zijn:

-   Van veld CBG respectievelijk EBG is bij een put informatie terug <u>optioneel</u> en bij een kolk <u>verplicht</u>

-   Van veld CCK respectievelijk ECK is bij een put informatie terug <u>optioneel</u> en bij een kolk <u>verplicht</u>

-   Veld CCM respectievelijk ECM heeft bij een put een andere betekenis dan bij een kolk.

Behoudens deze uitzondering zitten er geen tegenstrijdigheden in de inhoud van de velden.

Uit de analyse van de informatie uit stap 1 blijkt dat er voor de vervolgstappen in het GWSW-Maatregelen alle benodigde informatie uitgewisseld wordt. Er is in deze processtap geen behoefte om extra informatie uit te wisselen.

Stap 2: Uitvoeren reiniging en inspecties en aanlevering waarnemingen.
----------------------------------------------------------------------

Stap 2 is eveneens reeds beschreven in het GWSW-RibX. De opdrachtnemer levert na de uitvoering van de werkzaamheden een gevuld GWSW-RibX bestand aan de opdrachtgever. Deze bestaat uit headergegevens, waarnemingen en meetgegevens. Hoe om te gaan met wijzigingen ten opzichte van de heen informatie staat in de beschrijving van het GWSW-RibX verwoord. Bij de kolken zijn aanvullende tabellen gedefinieerd waarin ook al maatregelen opgenomen kunnen worden.

Ook uit de analyse van stap 2 blijkt dat er voor de vervolgstappen in het GWSW-Maatregelen alle benodigde informatie uitgewisseld wordt. Er is in deze stap geen behoefte om extra informatie uit te wisselen.

Stap 3: Uitvoeren beoordeling en opstellen maatregeladvies
----------------------------------------------------------

De opdrachtnemer ontvangt van de opdrachtgever het gevuld GWSW-RibX bestand met headergegevens, waarnemingen en meetgegevens. Om de beoordeling uit te kunnen voeren, dienen de randvoorwaarden door de opdrachtgever te worden aangeleverd. De randvoorwaarden bestaan uit de beoordelingscriteria voor ingrijp- en waarschuwingsmaatstaven en worden eventueel aangevuld met externe zaken zoals hydraulische knelpunten, voorgenomen wegreconstructies en dergelijke. Aan de hand hiervan kan de beoordeling plaatsvinden. De benodigde acties worden op objectniveau (voor het gehele object) of op het niveau van een toestandsaspect (plaatselijke schade) aangegeven. Het resultaat van stap 3 is een maatregeladvies.

Tabel : Informatie-uitwisseling stap 3

<table>
<caption>sdf</caption>
<thead>
<tr class="header">
<th><strong>Stap 3: beoordelen inspectie / opstellen maatregeladvies</strong></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Veld</strong></td>
<td><strong>Heen</strong></td>
<td><strong>Terug</strong></td>
<td><strong>Naam</strong></td>
<td><strong>Toelichting (geen = conform EN 13508-2)</strong></td>
<td><strong>Betreft</strong></td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie werkgever</td>
<td>Opdrachtcode van opdrachtgever (bestaand veld in RibX)</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Naam adviseur</td>
<td>Naam beoordelaar en bedrijf</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Functiereferentie adviseur</td>
<td>Opdrachtcode van het bedrijf van de beoordelaar</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Datum</td>
<td>Datum van oplevering van de beoordeling</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Oorsprong maatregel</td>
<td><p>1. Geautomatiseerd toegekend (codes vergelijken)</p>
<p>2. Nader inhoudelijk toegekend (bekijken beeldmateriaal)</p></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Inventarisatiegegevens (RibX header A, C en E-codes)</td>
<td>Betreft de headergegevens van de objecten</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td><p>Inspectiegegevens (RibX B, D en F-codes)</p>
<p><em>Bestaat uit identificatiecodes van put of leiding en waarnemingen</em></p></td>
<td><p>Betreft de volledige inspectie van objecten die voor beoordeling in aanmerking komen.</p>
<p><em>Bij maatregelen op toestandsaspecten dienen de riool- en waarneming records hiervan in het terug-bestand te worden geleverd.</em></p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Beoordelingscriteria</td>
<td>Minimale Ingrijp- en waarschuwingsmaatstaven</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie beoordelingscriteria</td>
<td></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Randvoorwaarden beoordeling</td>
<td><p>Bijvoorbeeld voorgenomen reconstructies / clustervorming</p>
<p>De waarde “geen” gebruiken indien er geen aanvullende randvoorwaarden gelden.</p>
<p>1 = Geen</p>
<p>2 = Klachten</p>
<p>3 = Wegbeheer</p>
<p>4 = Hydraulische knelpunten</p>
<p>5 = Nieuwbouwlocatie</p>
<p>6 = Beleid o.a. materialen-duurzaamheid-circulariteit</p></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie randvoorwaarden beoordeling</td>
<td></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Maatregel (op (deel)object)</td>
<td><p>De maatregel (Activiteit) registreren in de headergegevens.</p>
<p><em>Bij een maatregel op een deelobject altijd het deel van het object benoemen waar het om gaat. Bijvoorbeeld aanbrengen van een stroomprofiel, vervangen putafdekking, etc.</em></p>
<p><em>(let wel: deze hebben veel subtypes in het concept GWSW-Maatregelen wat nu geprogrammeerd is)</em></p>
<p>0 = Geen</p>
<p><del>1 = Aanleggen (NIET GEBRUIKEN)</del></p>
<p>2 = Buiten gebruik stellen</p>
<p>3 = Conserveren</p>
<p><del>4 = Onderhoud (N.V.T.)</del></p>
<p>5 = Onderzoeken</p>
<p>6 = Renoveren</p>
<p><del>7 = Repareren (N.V.T.)</del></p>
<p>8 = Verbeteren</p>
<p>9 = Vervangen</p>
<p>10 = Verwijderen</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Maatregel (op toestandsaspect)</td>
<td><p>De maatregel (activiteit) registreren in de waarnemingen in RibX?.</p>
<p>Er zijn meerdere maatregelen op 1 toestandsaspect mogelijk.</p>
<p><em>Bij een toestandsaspect binnen een ingrijpmaatstaf welke niet tot een maatregel leidt, de waarde “geen” vermelden.</em></p>
<p><em>(let wel: deze hebben veel subtypes in het concept GWSW-Maatregelen wat nu geprogrammeerd is)</em></p>
<p>0 = Geen</p>
<p><del>1 = Aanleggen (N.V.T.)</del></p>
<p><del>2 = Buiten gebruik stellen (N.V.T.)</del></p>
<p><del>3 = Conserveren (N.V.T.)</del></p>
<p>4 = Onderhouden</p>
<p>4.1. Vrijmaken leidingprofiel</p>
<p>4.2. Vrijmaken putprofiel</p>
<p><del>5 = Onderzoeken (N.V.T.)</del></p>
<p><del>6 = Renoveren (N.V.T.)</del></p>
<p>7 = Repareren</p>
<p>7.1. Beton repareren</p>
<p>7.2. Injecteren</p>
<p>7.3. Deelliner plaatsen</p>
<p>7.4. Manchet plaatsen</p>
<p>7.5. Metselwerkvoegen herstellen</p>
<p>7.6. Omstorten, met beton</p>
<p><del>8 = Verbeteren (N.V.T.)</del></p>
<p><del>9 = Vervangen (N.V.T.)</del></p>
<p><del>10 = Verwijderen (N.V.T.)</del></p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>O</td>
<td>Opmerking maatregel (op -onderdeel van het- object)</td>
<td>Betreft de opmerking van de beoordelaar, clustering altijd vermelden</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>O</td>
<td>Opmerking maatregel (op toestandsaspect)</td>
<td>Betreft de opmerking van de beoordelaar, bijvoorbeeld foutieve toestandsaspecten</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>A</td>
<td>Uitvoeringsperiode maatregel op -onderdeel van het- object)</td>
<td>Betreft de beoogde uitvoeringsperiode naar aanleiding van de beoordeling</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>A</td>
<td>Uitvoeringsperiode maatregel (op toestandsaspect)</td>
<td>Betreft de beoogde uitvoeringsperiode naar aanleiding van de beoordeling</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Toekomstig materiaal</td>
<td>Terug: Alleen bij vervangen van een (deel)object of aanleg van deelobjecten. Aanleg van een volledig object valt hier buiten</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>O</td>
<td>A</td>
<td>Toekomstige vorm</td>
<td>Terug: Alleen bij vervangen van volledig object (leiding of put)</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Toekomstige breedte</td>
<td>Terug: Alleen bij vervangen van volledig object (leiding of put)</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>O</td>
<td>A</td>
<td>Toekomstige hoogte</td>
<td>Terug: Alleen bij vervangen van volledig object (leiding of put)</td>
<td>H</td>
</tr>
</tbody>
</table>

.

Stap 4: Vaststellen maatregelplan
---------------------------------

De controleur stelt aan de hand van het maatregeladvies uit stap 3 de definitieve maatregel vast. Voor zover uit de controle van het maatregeladvies een afwijking ten opzichte van het maatregeladvies volgt, dient dit altijd met een opmerking te worden toegelicht. Op die manier is terug te vinden waarom van een advies is afgeweken. Is de definitieve maatregel gelijk aan de geadviseerde maatregel, dan kan dit veld leeg blijven. Het resultaat van stap 4 is een maatregelplan waarin de definitieve maatregelen staan opgenomen.

Tabel : Informatie-uitwisseling stap 4

<table>
<thead>
<tr class="header">
<th><strong>Stap 4: Vaststellen definitieve maatregel (toegevoegde velden tov stap 3)</strong></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Veld</strong></td>
<td><strong>Heen</strong></td>
<td><strong>Terug</strong></td>
<td><strong>Naam</strong></td>
<td><strong>Toelichting (geen = conform EN 13508-2)</strong></td>
<td><strong>Betreft</strong></td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie werkgever</td>
<td>Opdrachtcode van opdrachtgever (bestaand veld in RibX)</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum</td>
<td><p>Heen: Datum van oplevering van de beoordeling</p>
<p>Terug: Datum van vaststellen definitieve maatregel</p></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Oorsprong maatregel</td>
<td><p>1. Geautomatiseerd toegekend (codes vergelijken)</p>
<p>2. Nader inhoudelijk toegekend (bekijken beeldmateriaal)</p></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Inventarisatiegegevens (RibX header A, C en E-codes)</td>
<td>Betreft de headergegevens van de objecten</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td><p>Inspectiegegevens (RibX B, D en F-codes)</p>
<p><em>Bestaat uit identificatiecodes van put of leiding en waarnemingen</em></p></td>
<td><p>Betreft de volledige inspectie van objecten die voor beoordeling in aanmerking komen.</p>
<p><em>Bij maatregelen op toestandsaspecten dienen de riool- en waarneming records hiervan in het terug-bestand te worden geleverd.</em></p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Beoordelingscriteria</td>
<td><p>Minimale Ingrijp- en waarschuwingsmaatstaven</p>
<p>Afwijkingen tov stap 3 verplicht vermelden; anders “heen” ook mee “terug” leveren</p></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie beoordelingscriteria</td>
<td>Afwijkingen tov stap 3 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Randvoorwaarden beoordeling</td>
<td>Afwijkingen tov stap 3 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie randvoorwaarden beoordeling</td>
<td>Afwijkingen tov stap 3 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op (deel)object)</td>
<td><p>Heen: Het maatregeladvies uit stap 3</p>
<p>Terug: Betreft in stap 4 de definitieve maatregel (op -onderdeel van het- object) na controle door de controleur.</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op toestandsaspect)</td>
<td><p>Heen: Het maatregeladvies uit stap 3</p>
<p>Terug: Betreft in stap 4 de definitieve maatregel (op toestandsaspect) na controle door de controleur</p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op (deel)object)</td>
<td>Verplicht veld in stap 4 indien de definitieve maatregel af wijkt van het maatregeladvies uit stap 3.</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op toestandsaspect)</td>
<td>Verplicht veld in stap 4 indien de definitieve maatregel af wijkt van het maatregeladvies uit stap 3.</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Uitvoeringsjaar maatregel (op (deel)object)</td>
<td><p>Betreft het beoogd uitvoeringsjaar van de definitieve maatregel</p>
<p>Deze kan afwijken van het maatregeladvies</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Uitvoeringsjaar maatregel (op toestandsaspect)</td>
<td><p>Betreft het beoogd uitvoeringsjaar van de definitieve maatregel</p>
<p>Deze kan afwijken van het maatregeladvies</p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Toekomstig materiaal</td>
<td>Alleen bij vervangen van een (deel)object of aanleg van deelobjecten. Aanleg van een volledig object valt hier buiten. Afwijkingen ten opzichte van stap 3 verplicht vermelden</td>
<td>H</td>
</tr>
<tr class="even">
<td> </td>
<td>O</td>
<td>A</td>
<td>Toekomstige vorm</td>
<td>Alleen bij vervangen van volledig object (leiding of put)<br />
Afwijkingen ten opzichte van stap 3 verplicht vermelden</td>
<td>H</td>
</tr>
<tr class="odd">
<td> </td>
<td>O</td>
<td>A</td>
<td>Toekomstige breedte</td>
<td>Alleen bij vervangen van volledig object (leiding of put)<br />
Afwijkingen ten opzichte van stap 3 verplicht vermelden</td>
<td>H</td>
</tr>
<tr class="even">
<td> </td>
<td>O</td>
<td>A</td>
<td>Toekomstige hoogte</td>
<td>Alleen bij vervangen van volledig object (leiding of put)<br />
Afwijkingen ten opzichte van stap 3 verplicht vermelden</td>
<td>H</td>
</tr>
</tbody>
</table>

Stap 5: Opstellen contract ten behoeve van uitvoering
-----------------------------------------------------

Voor het geval sprake is van losse (kleinere) opdrachten, kan stap 5 achterwege gelaten worden. In dat geval geldt het “Terug” bestand van stap 4 als “Heen” bestand voor stap 6.

In stap 5 is de uitwisseling beschreven ten behoeve van het opstellen van een contract voor de uit te voeren maatregelen. Deze kunnen gebaseerd zijn op meerdere beoordelingen. Is dat het geval dan dient het maatregeladvies van al deze beoordelingen als “Heen” bestand te worden aangeleverd. De opdrachtgever levert aan de opdrachtnemer de selectie van de maatregeladviezen welke in het contract opgenomen dienen te worden.

In de praktijk worden vaak de volledige GWSW-RibX bestanden aangeleverd, waarin ook objecten zijn opgenomen waar geen maatregelen nodig zijn. Het advies is om alleen die objecten aan te leveren waar maatregelen nodig zijn om verwarring te voorkomen.

Bij vervanging van (deel)objecten dienen gegevens van het nieuwe (deel)object te worden bepaald. Dit zijn onder andere toekomstige vorm, breedte, hoogte, materiaal en verharding. In geval van renovatie dienen de parameters ten behoeve van het ontwerp te worden aangeleverd.

Het kan voorkomen dat de definitieve maatregel uit stap 4 niet de uiteindelijke maatregel is welke in het contract opgenomen wordt. In dat geval dient de maatregel te worden aangepast en dient middels een opmerking de motivatie van deze wijziging te worden vermeld. Het resultaat van stap 5 is een contract dat uitgevoerd kan worden.

Tabel : Informatie-uitwisseling stap 5

<table>
<thead>
<tr class="header">
<th><strong>Stap 5: Opstellen contract (toegevoegde velden tov stap 4)</strong></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Veld</strong></td>
<td><strong>Heen</strong></td>
<td><strong>Terug</strong></td>
<td><strong>Naam</strong></td>
<td><strong>Toelichting (geen = conform EN 13508-2)</strong></td>
<td><strong>Betreft</strong></td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie werkgever</td>
<td>Opdrachtcode van opdrachtgever (bestaand veld in RibX)</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Inventarisatiegegevens (RibX header A, C en E-codes)</td>
<td>Betreft de headergegevens van de objecten <em>(of een selectie van objecten) die in het contract worden opgenomen</em></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td><p>Inspectiegegevens (RibX B, D en F-codes)</p>
<p><em>Bestaat uit identificatiecodes van put of leiding en waarnemingen</em></p></td>
<td><p>Betreft de volledige inspectie van objecten die voor beoordeling in aanmerking komen.</p>
<p><em>Bij maatregelen op toestandsaspecten dienen de riool- en waarneming records hiervan in het terug-bestand te worden geleverd.</em></p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Beoordelingscriteria</td>
<td>Afwijkingen ten opzichte van stap 4 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie beoordelingscriteria</td>
<td>Afwijkingen ten opzichte van stap 4 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Randvoorwaarden beoordeling</td>
<td>Afwijkingen ten opzichte van stap 4 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum / versie randvoorwaarden beoordeling</td>
<td>Afwijkingen ten opzichte van stap 4 verplicht vermelden</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op (deel)object)</td>
<td><p>Heen: de definitieve maatregel uit stap 4</p>
<p>Terug: Betreft in stap 5 de maatregel (op (deel)object) welke in het contract wordt opgenomen. De contractmaatregel kan afwijken van de definitieve maatregel uit stap 4.</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op toestandsaspect)</td>
<td><p>Heen: de definitieve maatregel uit stap 4</p>
<p>Terug: Betreft in stap 5 de maatregel (op toestandsaspect) welke in het contract wordt opgenomen. De contractmaatregel kan afwijken van de definitieve maatregel uit stap 4.</p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op (deel)object)</td>
<td>Verplicht veld in stap 5 indien de contractmaatregel af wijkt van de definitieve maatregel uit stap 4.</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op toestandsaspect)</td>
<td>Verplicht veld in stap 5 indien de contractmaatregel af wijkt van de definitieve maatregel uit stap 4.</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>A</td>
<td>Uitvoeringsjaar maatregel op (deel)object)</td>
<td>Betreft het beoogd uitvoeringsjaar volgens (meerjaren)contract</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>A</td>
<td>Uitvoeringsjaar maatregel (op toestandsaspect)</td>
<td>Betreft het beoogd uitvoeringsjaar volgens (meerjaren)contract</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Toekomstig materiaal</td>
<td><p>Alleen bij vervangen van een (deel)object of aanleg van deelobjecten. Aanleg van een volledig object valt hier buiten.</p>
<p>Afwijkingen ten opzichter van stap 4 verplicht vermelden</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Toekomstige vorm</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>Afwijkingen ten opzichte van stap 4 verplicht vermelden</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Toekomstige breedte</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>Afwijkingen ten opzichte van stap 4 verplicht vermelden</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Toekomstige hoogte</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>Afwijkingen ten opzichte van stap 4 verplicht vermelden</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Naam opsteller</td>
<td>Naam van de opsteller van het contract</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Functiereferentie opsteller</td>
<td>Opdrachtcode van het bedrijf van de opsteller</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Datum contract</td>
<td><em> </em></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td><p>Kenmerk contract</p>
<p><em>(Code en omschrijving)</em></p></td>
<td><em> </em></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Contractvorm</td>
<td><p>Keuze op basis van een codelijst definiëren:</p>
<p>1 = RAW-bestek</p>
<p>2 = RAW-raamovereenkomst</p>
<p>3 = Programma van Eisen</p>
<p>4 = ????</p></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>O</td>
<td>A</td>
<td>Parameters t.b.v. ontwerp relinen</td>
<td>Geldt voor relinen van leidingen en ook voor putten</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>O</td>
<td>Bestekspostnummer</td>
<td>Om de link te leggen tussen maatregel en het contract c.q. verrekening van de uitgevoerde maatregel</td>
<td>H/T</td>
</tr>
</tbody>
</table>

Stap 6: Uitvoering maatregelen
------------------------------

De opdrachtnemer vult informatie ten aanzien van de uitgevoerde maatregelen aan. De informatiebehoefte is sterk afhankelijk of het gaat om een maatregel op een (deel)object of een toestandsaspect. Tijdens de uitvoering kan het zijn dat de maatregel die in het contract is opgenomen, in de praktijk niet uitvoerbaar en dus aangepast dient te worden. In dat geval dient dit bij de opmerking te worden gemotiveerd. Dit geldt tevens indien een maatregel binnen de opdracht niet uitvoerbaar blijkt te zijn en er geen maatregel is uitgevoerd.

Door een opleveringsinspectie te verlangen, krijgt de opdrachtgever automatisch via waarnemingen de uitgevoerde maatregelen terug. Dit geldt niet voor maatregelen die van buitenaf uitgevoerd zijn. Daarvoor dienen de gegevens handmatig te worden gevuld.

Tabel : Informatie-uitwisseling stap 6

<table>
<thead>
<tr class="header">
<th><strong>Stap 6: Uitvoering maatregelen (toegevoegde velden tov stap 5)</strong></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Veld</strong></td>
<td><strong>Heen</strong></td>
<td><strong>Terug</strong></td>
<td><strong>Naam</strong></td>
<td><strong>Toelichting (geen = conform EN 13508-2)</strong></td>
<td><strong>Betreft</strong></td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie werkgever</td>
<td>Opdrachtcode van opdrachtgever (bestaand veld in RibX)</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Inventarisatiegegevens (RibX header A, C en E-codes)</td>
<td>Betreft de headergegevens van de objecten<br />
<em>Selectie van objecten die in het contract worden opgenomen</em></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td><p>Inspectiegegevens (RibX B, D en F-codes)</p>
<p><em>Bestaat uit identificatiecodes van put of leiding en waarnemingen</em></p></td>
<td><p>Betreft de volledige inspectie van objecten die voor beoordeling in aanmerking komen.</p>
<p><em>Bij maatregelen op toestandsaspecten dienen de riool- en waarneming records hiervan in het terug-bestand te worden geleverd.</em></p></td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op (deel)object)</td>
<td>Heen: De contractmaatregel uit stap 5<br />
Terug: Betreft in stap 6 de uitgevoerde maatregel (op (deel)object). Deze kan afwijken van de contractmaatregel</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op toestandsaspect)</td>
<td>Heen: De contractmaatregel uit stap 5<br />
Terug: Betreft in stap 6 de uitgevoerde maatregel (op toestandsaspect). Deze kan afwijken van de contractmaatregel</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op (deel)object)</td>
<td>Verplicht veld in stap 6 indien de uitgevoerde maatregel af wijkt van de contractmaatregel uit stap 5.</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Opmerking maatregel (op toestandsaspect)</td>
<td>Verplicht veld in stap 6 indien de uitgevoerde maatregel af wijkt van de contractmaatregel uit stap 5.</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Materiaal / UITGEVOERD</td>
<td><p>Alleen bij vervangen van een (deel)object of aanleg van deelobjecten. Aanleg van een volledig object valt hier buiten.</p>
<p>(In RibX update van veld ACD)</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Vorm / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put). Aanleg van een volledig object valt hier buiten.</p>
<p>(In RibX update van veld ACA)</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Breedte / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put). Aanleg van een volledig object valt hier buiten.</p>
<p>(In RibX update van veld ACC)</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Hoogte / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put). Aanleg van een volledig object valt hier buiten.</p>
<p>(In RibX update van veld ACB)</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Naam opsteller</td>
<td>Naam van de opsteller van het contract</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie opsteller</td>
<td>Opdrachtcode van het bedrijf van de opsteller</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum contract</td>
<td></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Kenmerk contract<br />
<em>Code en omschrijving</em></td>
<td></td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Contractvorm</td>
<td></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Parameters t.b.v. ontwerp relinen</td>
<td>Geldt voor relinen leidingen en ook voor putten</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Ontwerp liner</td>
<td>Betreft de ontwerpberekening met wanddiktes, gedeclareerde waarden en certificering</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>O</td>
<td>O</td>
<td>Bestekspostnummer)</td>
<td>Om de link te leggen tussen maatregel en het contract c.q. verrekening van de uitgevoerde maatregel</td>
<td>H/T</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Soort lining</td>
<td>(In RibX update van veld ACE)</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>O</td>
<td>A</td>
<td>Liningmateriaal</td>
<td>(In RibX update van veld ACF)</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Naam directie voerende partij</td>
<td>Naam bedrijf en naam van de directievoerder</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Contractcode directie voerende partij</td>
<td>Opdrachtcode van het bedrijf van de directievoerder</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td> </td>
<td>A</td>
<td>Naam uitvoerende partij</td>
<td>Naam contractpartner die de maatregelen uit voert</td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td> </td>
<td>A</td>
<td>Verificatiedatum (uitgevoerde maatregel)</td>
<td> </td>
<td>H/T</td>
</tr>
<tr class="odd">
<td></td>
<td>O</td>
<td>A</td>
<td>Datum</td>
<td>Datum van uitvoering van de maatregel</td>
<td>H/T</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>A</td>
<td>Informatiedrager</td>
<td><p>Zie <a href="http://www.data">www.data</a>.gwsw.nl</p>
<p>Inspectierapport RibX (met beelden en/of foto’s)</p>
<p>Revisies</p>
<p>Werktekeningen</p>
<p>Prcoces Verbaal van Opneming</p>
<p>(Bij liners) Rapportage laboratoriumonderzoek</p></td>
<td>H</td>
</tr>
</tbody>
</table>

Stap 7: Verwerken oplevering uitgevoerde maatregelen in beheerpakket.
---------------------------------------------------------------------

In deze stap is beschreven welke gegevens uiteindelijk als eindresultaat in de beheerdata verwerkt dient te worden nadat de benodigde maatregelen zijn uitgevoerd. In de praktijk zal bij elke voorgaande stap telkens ook (een deel van) de beheerdata worden verrijkt met informatie uit deze stappen.

Tabel : Informatie-uitwisseling stap 7

<table>
<thead>
<tr class="header">
<th><strong>Stap 7: Verwerken in beheerdata (toegevoegde velden tov stap 6; de stap van controle op de uitvoering is geborgd door D&amp;T)</strong></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Veld</strong></td>
<td><strong>Heen</strong></td>
<td><strong>Terug</strong></td>
<td><strong>Naam</strong></td>
<td><strong>Toelichting (geen = conform EN 13508-2)</strong></td>
<td><strong>Betreft</strong></td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Functiereferentie werkgever</td>
<td>Opdrachtcode van opdrachtgever (bestaand veld in RibX)</td>
<td>P</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op -onderdeel van het- object)</td>
<td>De uitgevoerde maatregel uit stap 6</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Maatregel (op toestandsaspect)</td>
<td>De uitgevoerde maatregel uit stap 6</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Opmerking maatregel (op -onderdeel van het- object)</td>
<td>Betreft de opmerking uit stap 6 van de uitvoerende partij indien de maatregel af wijkt van de maatregel uit stap 5.</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Opmerking maatregel (op toestandsaspect)</td>
<td>Betreft de opmerking uit stap 6 van de uitvoerende partij indien de maatregel af wijkt van de maatregel uit stap 5.</td>
<td>T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Materiaal / UITGEVOERD</td>
<td><p>Alleen bij vervangen van een (deel)object of aanleg van deelobjecten. Aanleg van een volledig object valt hier buiten.</p>
<p>(In RibX update van veld ACD)</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Vorm / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>(In RibX update van veld ACA)</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Breedte / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>(In RibX update van veld ACC)</p></td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Hoogte / UITGEVOERD</td>
<td><p>Alleen bij vervangen van volledig object (leiding of put)</p>
<p>(In RibX update van veld ACB)</p></td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Kenmerk contract<br />
<em>Code en omschrijving</em></td>
<td><em>LET OP: Dit zijn header gegevens van de activiteit en behoren niet tot het niveau van definitieve maatregel</em></td>
<td>P</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Parameters t.b.v. ontwerp relinen</td>
<td>Geldt voor relinen leidingen en ook bij putten</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Ontwerp liner</td>
<td>Betreft de ontwerpberekening met wanddiktes, gedeclareerde waarden en certificering</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Soort lining</td>
<td>(In RibX update van veld ACE)</td>
<td>H</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Liningmateriaal</td>
<td>(In RibX update van veld ACF)</td>
<td>H</td>
</tr>
<tr class="even">
<td></td>
<td>A</td>
<td>A</td>
<td>Verificatiedatum (uitgevoerde maatregel)</td>
<td> </td>
<td>H/T</td>
</tr>
<tr class="odd">
<td></td>
<td>A</td>
<td>A</td>
<td>Datum</td>
<td>Bij aanleg/vervanging/relining is dit de startdatum van het (deel)object. Bij uitgevoerde onderhoudsmaatregelen volgt een nieuwe inspectie.</td>
<td>H/T</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>A</td>
<td>Informatiedrager</td>
<td><p>Zie <a href="http://www.data">www.data</a>.gwsw.nl</p>
<p>Inspectierapport RibX (met beelden en/of foto’s)</p>
<p>Revisies</p>
<p>Werktekeningen</p>
<p>Prcoces Verbaal van Opneming</p>
<p>(Bij liners) Rapportage laboratoriumonderzoek</p></td>
<td>H</td>
</tr>
</tbody>
</table>

## UML schema's tbv modellering

### Maatregelenproces
![maatregelenproces](media/GWSW%20maatregelen%20-%20Maatregelenproces.png)

### Initieren reinigen en inspectie
![reinigen_inspectie](media/GWSW%20maatregelen%20-%20InitierenReinigingInspectie.png)

### Beoordelen en opstellen maatregelen
![reinigen_inspectie](media/GWSW%20maatregelen%20-%20Beoordelen%20en%20opstellen%20maatregelen.png)
