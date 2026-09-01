---
name: humanizer-svenska
version: 3.0.0
description: |
  Rewrite AI-sounding Swedish professional text so it reads naturally without
  changing what it says. Use when editing or reviewing Swedish prose (business
  writing, reports, articles, LinkedIn posts) for significance inflation, sales
  language, passive voice as false formality, nominalization, anglicisms, vague
  sources, stock AI words, filler, hedging, chatbot artifacts, fake-candid
  openers, formulaic sayings, or dash and quote typography. Patterns follow
  blader/humanizer 2.11.2, adapted to Swedish.
allowed-tools:
  - Read
  - Write
  - Edit
  - AskUserQuestion
---

# Humanizer Svenska: Ta bort AI-mönster ur professionell text

Skriv om AI-klingande svensk text så att den låter som skribenten, inte som en chattbot. 
Ändra inte vad texten säger och hitta inte på detaljer. Guiden bygger på observerade 
mönster i AI-genererad svenska, med fokus på professionellt skrivande. Mönsterlistan 
följer [blader/humanizer](https://github.com/blader/humanizer) 2.11.2 (Wikipedias 
"Signs of AI writing"), anpassad till hur AI skriver svenska.

## Din uppgift

När du får en text att humanisera:

1. **Fråga om texttyp om det är oklart** – Affärstext, rapport, artikel eller sociala medier 
   har olika register. Om det inte framgår av texten eller instruktionen, fråga innan du börjar.
2. **Identifiera AI-mönster** – Scanna efter mönstren nedan
3. **Behåll varje påstående** – Du får korta ner det tråkiga, bygga ut det användbara och 
   slå ihop eller dela stycken. Informationen ska finnas kvar även när strukturen ändras.
4. **Hitta inte på fakta** – Lägg inte till en uppgift, ett namn, en siffra, ett datum, ett 
   citat eller en källa som inte finns i underlaget eller kommer från användaren. Saknas en 
   detalj som meningen behöver: fråga, eller skriv en enklare mening. En åsikt eller reaktion 
   får du tillföra när rösten kräver det, men aldrig ett faktapåstående.
5. **Matcha rätt register** – Applicera rätt ton utifrån texttypen, och skribentens egen röst 
   om det finns ett textprov (se nedan)
6. **Tillför röst när det passar** – Krönikor, inlägg, mejl och debattartiklar ska ha en 
   människa bakom sig. Rapporter, avtalstext och myndighetstext ska vara sakliga; tillför inte 
   åsikter eller jag-form där de inte hör hemma.
7. **Gör ett avslutande AI-test** – Fråga: "Vad avslöjar att det här fortfarande är AI-genererat?" 
   Svara kortfattat. Fråga sedan: "Vad saknar texten för att låta skriven av en verklig person 
   med en verklig åsikt?" Revidiera baserat på båda svaren.

Vad du lämnar tillbaka styrs av hur texten kom in. Se [Så returnerar du resultatet](#så-returnerar-du-resultatet).

---

## MATCHA SKRIBENTENS RÖST

Om användaren skickar med ett textprov (egen tidigare text), analysera det innan du skriver om:

1. Läs provet först. Notera meningslängd, ordval, hur stycken öppnar, interpunktion, 
   återkommande fraser och övergångar.
2. Matcha vanorna. Byt inte ut vardagliga ord mot formella och ta inte bort medvetna egenheter.
3. Finns inget prov: följ riktlinjerna nedan.

Ett textprov går före stilreglerna i den här guiden. Använder provet tankstreck som inskott, 
behåll dem i ungefär samma takt (se §21).

---

## PERSONLIGHET OCH RÖST

Att undvika AI-mönster är bara halva jobbet. Steril, röstlös text avslöjar sig lika 
mycket som slarvigt AI-innehåll. Bra svensk professionell text har en människa bakom sig.

Det gäller texter med en avsändare: artiklar, inlägg, mejl, förslag. En rapport eller ett 
beslutsunderlag ska vara sakligt; där tillför du tydlighet, inte åsikter. Och hitta aldrig 
på fakta för att texten ska kännas personlig.

### Tecken på röstlös text (även om den är tekniskt "ren"):
- Varje mening har samma längd och struktur
- Inga egna åsikter, bara neutral rapportering
- Ingen erkänsla av komplexitet eller motstridiga tankar
- Inget "jag" eller "vi" när det vore naturligt
- Läses som en pressrelease eller myndighetstext

### Vad nordisk professionell röst innebär:
- **Direkthet utan brasklappar.** Skriv vad du menar. Inte "det kan konstateras att 
  resultaten möjligen indikerar" utan "resultaten visar."
- **Understatement som trovärdighet.** Svenska läsare misstror superlativ. "Det här 
  fungerade bra" är mer övertygande än "det här var banbrytande."
- **Aktiv röst och första person.** "Vi ändrade strategin" snarare än "en strategiändring 
  genomfördes." Jag-form är inte oprofessionellt, det är ärligt.
- **Specifika detaljer framför generella påståenden.** Inte "starka resultat" utan 
  "30% ökning på tre månader."
- **Erkänn komplexitet.** "Det här är inte enkelt" är mer trovärdigt än en text som 
  låtsas att allt är löst.

### Röst i praktiken: Innan och efter

**Tekniskt ren men röstlös:**
> Analysen visar att retail media är ett växande segment. Det finns både möjligheter 
> och utmaningar för aktörerna på marknaden. Framåt kommer positionering och 
> mätbarhet att vara viktiga faktorer.

**Med röst:**
> Retail media växer snabbt, men mätbarheten haltar. De flesta retailers kan redovisa 
> klick, inte inkrementalitet. Det är ett problem som annonsörerna börjar ställa krav 
> på, och de retailers som inte har ett svar förlorar budgetar till de som har det.

Skillnaden är inte tonen. Det är att den andra texten faktiskt har en ståndpunkt.

---

## MÖNSTER ATT IDENTIFIERA OCH ÅTGÄRDA

### 1. Signifikansuppblåsning

**Ord att se upp med:**
avgörande, banbrytande, epokgörande, revolutionerande, transformativt, 
spelar en central/viktig/avgörande roll, vittnar om, utgör ett tydligt bevis på, 
det råder ingen tvekan om att, i det stora perspektivet, ett genombrott

**Problem:** AI-text blåser upp vikten av vanliga saker genom att beskriva dem som 
historiska vändpunkter eller avgörande skifte.

**Innan:**
> Vår lösning utgör ett banbrytande verktyg som möjliggör en mer effektiv och hållbar 
> affärsprocess och representerar en unik möjlighet att ta ägarskap över er digitala 
> transformation.

**Efter:**
> Verktyget automatiserar delar av affärsprocessen. (Skriv hur mycket tid eller hur många 
> moment det sparar bara om siffran finns i underlaget. Hitta inte på en.)

---

### 2. Landskap- och trenduppramning

**Fraser att se upp med:**
i en alltmer digitaliserad värld, i en allt mer föränderlig omvärld, i takt med den 
snabba teknologiska utvecklingen, i ett allt mer komplext landskap, digitaliseringen 
(som fristående förklaring utan specificering), spelplanen förändras, paradigmskifte

**Problem:** AI öppnar texter med en bred kontextuell fras som inte tillför något. 
Det är ett sätt att låta relevant utan att säga något specifikt.

**Innan:**
> I en värld där digitaliseringen omformar spelplanen i grunden spelar retail media 
> en alltmer central roll för hur varumärken kommunicerar med sina kunder.

**Efter:**
> Retail media är nu det snabbast växande annonsformatet i Sverige. Annonsörerna följer 
> köpintentionen, och köpintentionen finns på handelns egna plattformar.

---

### 3. Participfraser som falsk analys

**Fraser att se upp med:**
belyser vikten av, understryker behovet av, bidrar till en ökad förståelse för, 
möjliggör en mer..., lyfter fram, synliggör, tydliggör vikten av, 
understryker att, påvisar behovet av

**Problem:** AI lägger till nuvarande particip i slutet av meningar för att simulera 
analytiskt djup som inte finns där.

**Innan:**
> Implementeringen av denna strategi bidrar till en ökad förståelse för kundernas 
> behov, vilket i sin tur lyfter fram värdet av ett datadrivet arbetssätt.

**Efter:**
> Strategin bygger på kunddata. När vi förstår köpmönstren kan vi anpassa erbjudandet 
> i realtid, och det är det datadrivna arbetssättet i praktiken.

---

### 4. Vaga attributioner och vagbeskrivningar

**Fraser att se upp med:**
experter menar, forskning visar (utan källhänvisning), branschkällor pekar på, 
allt fler ser, många anser, det har konstaterats att, studier tyder på, 
ledande aktörer, tongivande röster

**Problem:** AI tillskriver åsikter till luddiga auktoriteter utan konkreta källor.

**Innan:**
> Experter menar att företag som inte anpassar sig riskerar att förlora marknadsandelar. 
> Branschkällor pekar på att investeringarna förväntas fördubblas inom de närmaste åren.

**Efter:**
> Vår bedömning är att företag som inte anpassar sig tappar marknadsandelar. (Namnge 
> källan om underlaget har en. Har det ingen: skriv påståendet som skribentens egen 
> bedömning, som här, eller stryk det. Gör det inte till ett faktum. Prognosen om 
> fördubbling saknar stöd i underlaget och stryks.)

Namnge en verklig källa när underlaget ger en. Annars: ta bort det ostödda påståendet. 
Hitta aldrig på en källa.

**Namedropping:** "Vårt arbete har uppmärksammats av DI, SvD, Breakit och Resumé" utan att 
säga vad som sades. Behåll den omnämning som faktiskt säger något, stryk resten. Hitta inte 
på ett sammanhang för att motivera en kortare lista.

---

### 5. Passiv röst som falsk formalitet

**Fraser att se upp med:**
det kan konstateras att, det bör påpekas att, det är viktigt att notera att, 
det är tydligt att, det råder ingen tvekan om att, det har visat sig att, 
det kan fastslås att, hänsyn bör tas till

**Problem:** AI använder passiva konstruktioner för att låta formell och neutral. 
I svensk professionell text, särskilt i affärsskrivande och artiklar, är aktiv röst 
tydligare och mer trovärdig.

**Innan:**
> Det kan konstateras att branschen befinner sig i en fas av betydande förändring. 
> Det bör påpekas att ett holistiskt förhållningssätt krävs.

**Efter:**
> Branschen förändras snabbt. Regulatoriska krav och konsumenternas förväntningar 
> drar åt olika håll, och det kräver att man faktiskt väljer prioritetsordning.

---

### 6. Nominaliseringsöverdrift

**Problem:** AI omvandlar verb till abstrakta substantiv för att låta formell. 
Resultatet är tung, opersonlig text som distanserar läsaren från budskapet. 
Detta är ett specifikt mönster i svensk AI-text som inte är lika vanligt på engelska.

**Att byta ut:**
- "implementeringen av" → "när vi implementerar" / "att implementera"
- "möjliggörandet av" → "att möjliggöra"
- "etableringen av" → "att etablera"
- "genomförandet av" → "när vi genomför"
- "säkerställandet av" → "för att säkerställa"
- "hanteringen av" → "hur vi hanterar"

**Innan:**
> Genomförandet av strategin och säkerställandet av intern förankring är 
> förutsättningar för etableringen av en hållbar process.

**Efter:**
> Strategin fungerar bara om den är internt förankrad innan vi börjar genomföra den.

---

### 7. Anglifieringsimporter

**Problem:** AI översätter engelska idiom direkt till svenska på ett sätt som 
infödda skribenter inte skriver. Texten låter som en maskinöversättning av en 
engelsk AI-text.

**Fraser att ersätta:**
- "ta ägarskap över" → "ansvara för", "driva", "äga frågan"
- "göra en skillnad" → "förändra något", "ha effekt"
- "ha en positiv impact" → "ge resultat", "påverka positivt"
- "navigera förändringen" → "hantera förändringen", "hitta vägen framåt"
- "på ett holistiskt sätt" → "i sin helhet", "sammantaget", eller stryk det helt
- "i linje med" → "enligt", "i enlighet med", "som stämmer med"
- "proaktivt" → "i förväg", "tidigt", eller stryk det
- "skala upp" → "växa", "öka volymen"
- "leverera värde" → specificera exakt vilket värde, t.ex. "minska kostnaden"
- "agera proaktivt" → "agera tidigt", "ta initiativ"

---

### 8. Strukturella AI-mönster

**Treregel på svenska:**
"snabbt, enkelt och effektivt" / "transparent, mätbar och skalbar" / 
"smart, hållbar och lönsam"

**Ersätt med:** Välj det viktigaste och motivera det. Tre egenskaper utan förklaring 
är inte ett argument.

**Falsk balansstruktur:**
"Å ena sidan... å andra sidan..." / "Dels... dels..." (utan att ta ställning efteråt)

**Ersätt med:** Ta faktiskt ställning. Presentera spänningen och lös den.

**Formulärsektion: Utmaningar och möjligheter:**
> "Trots utmaningarna finns det stora möjligheter för de aktörer som väljer att 
> agera proaktivt."

Stryk alltid. Skriv om vad utmaningarna faktiskt är och vad som krävs för att lösa dem.

**Jämna styckeblock:**
AI skapar visuellt symmetriska stycken. Bryt mönstret. Korta meningar. 
Sedan en längre som tar sin tid att landa.

**Generisk positiv avslutning:**
"Sammantaget representerar detta en unik möjlighet" / 
"Avslutningsvis kan vi konstatera att möjligheterna är stora" /
"Framåt ser det lovande ut för de aktörer som..."

Stryk alltid. Avsluta med det konkreta: nästa steg, en öppen fråga, eller en 
specifik slutsats.

---

### 9. Negativ parallellism (svensk variant)

**Mönster:** "Det är inte längre en fråga om om, utan när."
/ "Det handlar inte om teknik, det handlar om förtroende."
/ "Det är inte ett kostnadsställe, det är en investering."

**Problem:** Låter smart men säger ingenting. AI använder detta för att skapa känsla 
av insikt utan att leverera innehåll.

**Ersätt med:** Förklara exakt vad du menar i ett direkt påstående.

---

### 10. Sociala medier: Specifika mönster

Förutom ovanstående, se särskilt upp med dessa i inlägg:

- **Frågehak utan poäng:** "Vad tänker du? Hur navigerar du förändringen?" 
  som avslutning på ett inlägg som inte etablerat en verklig ståndpunkt
- **Hashtag-upprepning:** #DigitalTransformation #Innovation #Framtid 
  som fristående fraser utan koppling till faktiskt innehåll
- **"Jag delar en reflektion":** som inledning – stryk, börja med reflektionen
- **Konsensusöppning:** "Vi lever i en tid av förändring" – alla vet det, 
  säg något specifikt istället

---

### 11. Sycofantiska öppningar och avslutningar

**Mönster:**
- "Vilken bra fråga!" / "Det är en utmärkt observation."
- "Självklart, jag hjälper dig gärna med det!"
- "Tack för att du delar det här, det är verkligen intressant."
- "Hoppas det här hjälper! Hör av dig om du har fler frågor."
- "Stort lycka till med projektet!"
- "Vill du att jag utvecklar någon punkt?" / "Ska jag fortsätta?" / "Här är en sammanställning av..."

**Problem:** AI-text försöker behaga läsaren med onödig positiv förstärkning. 
Det signalerar omedelbart ett icke-mänskligt ursprung, och det underminerar trovärdigheten. 
Samma sak med chattbotens hälsning, erbjudande eller avslut som blivit kvar i en text som 
ska stå för sig själv.

**Innan:**
> Vilken intressant fråga! Det är verkligen ett komplext område. Jag hoppas att den 
> här genomgången ger dig en bra bild. Hör av dig om du vill veta mer!

**Efter:**
> Här är vad som faktiskt avgör priset.

---

### 12. Utfyllnadsfraser

**Problem:** AI fyller ut meningar med fraser som inte tillför innehåll. 
Resultatet är längre men inte bättre text.

**Att stryka eller ersätta:**
- "i syfte att uppnå detta mål" → "för att uppnå det"
- "på grund av det faktum att" → "eftersom"
- "i nuläget" / "i dagsläget" → "nu"
- "i händelse av att" → "om"
- "systemet har förmågan att" → "systemet kan"
- "det är viktigt att notera att" → skriv påståendet direkt
- "som ett resultat av detta" → "därför"
- "med tanke på ovanstående" → stryk, gå direkt till slutsatsen
- "inte minst" → stryk om det inte faktiskt finns en rangordning

**Innan:**
> I syfte att säkerställa en effektiv process är det viktigt att notera att systemet 
> har förmågan att hantera upp till 10 000 transaktioner per sekund.

**Efter:**
> Systemet hanterar upp till 10 000 transaktioner per sekund.

---

### 13. Överdriven osäkerhetssignalering

**Problem:** AI överkvalificerar påståenden, ofta för att undvika att ha fel. 
Resultatet är text som låter som den undviker att säga något.

**Mönster:**
- "det kan möjligen argumenteras att detta eventuellt skulle kunna..."
- "det är inte otänkbart att..."
- "det finns indikationer på att det möjligen..."
- "i viss mån", "till viss del", "i någon mening" (staplade på varandra)

**Innan:**
> Det kan möjligen argumenteras att denna strategi eventuellt skulle kunna ha en 
> viss positiv effekt på resultatet under rätt förutsättningar.

**Efter:**
> Strategin fungerar bäst när den kombineras med tydliga mätpunkter från start.

**Notera:** Verklig osäkerhet ska kommuniceras. "Vi vet inte ännu" är mer trovärdigt 
än en stapel av hedgingfraser. Skriv ut osäkerheten konkret istället för att dölja 
den i grammatik.

---

### 14. Kunskapsavgränsningsklausuler

**Mönster:**
- "Baserat på tillgänglig information..."
- "Inom ramen för mina kunskaper..."
- "Utan tillgång till fullständig data kan jag inte..."
- "Det bör nämnas att mina uppgifter kan vara föråldrade."

**Problem:** AI lägger in påminnelser om sina egna begränsningar i löpande text. 
En mänsklig skribent skriver inte så. Om informationen är osäker, säg varför 
informationen är osäker – inte att skribenten har begränsade kunskaper.

**Innan:**
> Baserat på tillgänglig information och inom ramen för vad som är känt om branschen 
> kan det konstateras att marknaden troligen kommer att växa.

**Efter:**
> Marknaden förväntas växa. (Ange vems prognos, om underlaget säger det. Annars stryk 
> meningen; hitta inte på en källa.)

**Innan (spekulativ lucktäppning):**
> Uppgifter om grundarens bakgrund är inte offentliga, vilket tyder på att hon håller en 
> låg profil. Hon växte troligen upp i en företagarfamilj, vilket formade hennes intresse 
> för entreprenörskap.

**Efter:**
> Grundarens bakgrund framgår inte av underlaget. (Eller stryk meningen. En gissning 
> med "troligen", "det är rimligt att anta" eller "vilket tyder på" är inte fakta.)

---

### 15. Kopulaundvikande (utgör/representerar/utgör)

**Problem:** AI undviker "är" och ersätter det med omskrivningar som låter tyngre 
och mer formella. Det är ett av de tydligaste AI-tecknen i svensk text.

**Att ersätta:**
- "utgör" → "är"
- "representerar" → "är" / "innebär"
- "fungerar som" → "är" (om det faktiskt är en synonym)
- "verkar som" → "är" (i formell mening)
- "syftar till att vara" → "ska vara"
- "kan beskrivas som" → "är"
- "står för" → "är" / "betyder" (om det är en direkt definition)

**Innan:**
> Rapporten utgör ett viktigt underlag och representerar ett genombrott i hur vi 
> förstår kundbeteende. Plattformen fungerar som en brygga mellan data och beslut.

**Efter:**
> Rapporten ger underlag för tre konkreta beslut om sortimentsbredden. 
> Plattformen kopplar ihop kunddata med inköpssystemet.

---

### 16. Bullet-punkts- och emoji-formatting som AI-signal

**Problem:** AI strukturerar spontant text med bullet-listor, feta rubriker och 
emojis även när innehållet inte kräver det. I professionell löptext och sociala 
medier-inlägg signalerar det omedelbart ett AI-ursprung.

**Vanliga mönster:**
- Listor med tre till fem punkter som sammanfattar något som ryms i en mening
- Rubriker som "Fördelar:", "Utmaningar:", "Nästa steg:" i ett kort inlägg
- Emojis som dekorativa avdelare: ✅ 🚀 💡 📊 👉
- Varje punkt börjar med ett fetstilt nyckelord följt av förklaring

**Innan:**
> Här är de viktigaste fördelarna:
> 
> 💡 **Effektivitet:** Processen går snabbare.  
> 🚀 **Skalbarhet:** Lösningen växer med er verksamhet.  
> ✅ **Kvalitet:** Resultaten förbättras över tid.

**Efter:**
> Processen går snabbare, lösningen skalbar och kvaliteten förbättras när volymerna ökar.

**Undantag:** Bullet-listor är legitima när innehållet faktiskt är en lista – 
tekniska specifikationer, åtgärdslistor, jämförelsetabeller. Problemet är när 
löpande resonemang styckas upp i listor utan att det tillför struktur.

---

### 17. Säljspråk

**Ord att se upp med:**
ledande, marknadsledande, innovativ, unik, skräddarsydd, i framkant, i världsklass, 
förstklassig, kraftfull, sömlös, passionerad, vi brinner för, ett nav för, hjärtat i, 
ett måste

**Problem:** AI-text låter som en annons, särskilt när den beskriver företag, produkter, 
platser eller organisationer. Svenska läsare misstror superlativ. Beskriv sakligt.

**Innan:**
> Vi är en ledande, innovativ aktör inom ekonomisystem för grossister, i framkant av 
> digitaliseringen, och erbjuder skräddarsydda lösningar i världsklass.

**Efter:**
> Vi gör ekonomisystem för grossister.

---

### 18. Överanvända AI-ord

**Högfrekventa AI-ord på svenska:**
dessutom, vidare, därtill, ytterligare (staplade som styckeöppnare), avgörande, central, 
nyckel- (nyckelfaktor, nyckelinsikt), landskap (abstrakt), belysa, understryka, betona, 
fördjupa oss i, dyka ner i, utforska, främja, möjliggöra, robust, sömlös, holistisk, 
dynamisk, innovativ, optimera, skalbar, värdefull, levande, i grunden, samspel, väv

**Problem:** AI använder de här orden mycket oftare än de flesta människor, och gärna 
flera i samma stycke. Ett enskilt "dessutom" är inget tecken. Fem i en text är det.

**Innan:**
> Dessutom är det avgörande att belysa samspelet mellan robusta processer och en dynamisk 
> kultur, vilket i grunden möjliggör en sömlös och skalbar tillväxt i ett föränderligt landskap.

**Efter:**
> Processerna och kulturen måste fungera ihop för att företaget ska kunna växa. (Säg hur, 
> om underlaget berättar det.)

---

### 19. Synonymväxling och upprepade meningsstarter

**Problem:** AI hanterar upprepning efter regel, inte efter öra. Den byter namn på samma 
sak ("företaget", "bolaget", "organisationen", "aktören") för att slippa upprepa ett ord, 
eller börjar flera meningar i rad med samma subjekt.

Använd ett tydligt namn för samma sak. Upprepade meningsstarter: slå ihop meningar, byt 
subjekt där det hjälper, eller börja med handlingen.

**Innan (synonymväxling):**
> Företaget växte snabbt under 2023. Bolaget rekryterade 40 personer. Organisationen 
> öppnade kontor i Malmö. Aktören ses nu som etablerad.

**Efter:**
> Företaget växte snabbt 2023, rekryterade 40 personer och öppnade kontor i Malmö.

**Innan (upprepade starter):**
> Vi såg problemet. Vi analyserade orsakerna. Vi tog fram en åtgärdsplan.

**Efter:**
> När vi hade sett problemet och analyserat orsakerna tog vi fram en åtgärdsplan.

Förbjud inte det upprepade ordet. Åtgärda det upprepade meningsmönstret. Den kvarvarande 
meningen får fortfarande börja med "Vi".

---

### 20. Falska spann ("från X till Y")

**Problem:** AI skriver "från X till Y" när X och Y inte är ändpunkter på en verklig 
skala. Det låter heltäckande men listar bara två saker.

**Innan:**
> Vi hjälper er hela vägen från strategi till genomförande, från insikt till handling, 
> från data till beslut.

**Efter:**
> Vi hjälper till med strategi, genomförande och analys. (Lista det underlaget faktiskt 
> nämner.)

---

### 21. Tankstreck, citattecken och versaler (svensk typografi)

Här skiljer sig svenskan från den engelska guiden. Tankstreck och typografiska citattecken 
är korrekt svenska, så de är inte AI-tecken i sig. Det är fel tecken och överanvändning 
som avslöjar.

**Långt tankstreck (—):** Används inte i svensk typografi. Ersätt alltid: med kort 
tankstreck (–), komma, punkt, kolon eller parentes, eller skriv om meningen.

**Kort tankstreck (–) som inskott:** Korrekt, men AI lägger ett inskott – som det här – i 
varannan mening. Finns ett textprov, behåll dess takt. Annars: högst något enstaka inskott 
per text; skriv om resten med komma eller punkt. Rör aldrig tankstreck i intervall och 
relationer ("2020–2024", "Stockholm–Göteborg", "3–4 veckor") eller replikstreck i dialog.

**Citattecken:** Svensk text använder ”…” (samma tecken före och efter) eller raka "…". 
Engelska “…” (66–99) i svensk text är ett tecken, liksom blandade stilar i samma dokument. 
Följ dokumentets konvention. Blanda inte.

**Versaler i rubriker:** Svenska rubriker har stor bokstav bara i första ordet och 
egennamn. "Varför Kultur Slår Teknik" är engelsk versalisering, och nästan alltid AI.

**Innan:**
> Strategin — som togs fram under våren — bygger på tre delar. Vd:n kallar den “vår 
> viktigaste satsning” — och det är ingen överdrift.

**Efter:**
> Strategin, som togs fram under våren, bygger på tre delar. Vd:n kallar den ”vår 
> viktigaste satsning”, och det är ingen överdrift.

Sök efter — i slutversionen och ta bort varje förekomst. Räkna – som inskott. Ligger 
antalet över textprovets takt, eller över ett par per text utan prov, skriv om.

---

### 22. Låtsad djupare sanning

**Fraser att se upp med:**
den egentliga frågan är, i grund och botten, i slutändan handlar det om, kärnan i det 
hela, det som verkligen spelar roll, vad det egentligen handlar om, i själva verket, 
det djupare problemet

**Problem:** AI använder fraserna för att få en vanlig poäng att låta som en dold sanning.

**Innan:**
> Den egentliga frågan är om teamen kan ställa om. I grund och botten handlar det om 
> organisationens mognad.

**Efter:**
> Frågan är om teamen kan ställa om. Det beror mest på om organisationen är beredd att 
> ändra sina vanor.

---

### 23. Annonsering av nästa poäng

**Fraser att se upp med:**
låt oss dyka ner i, låt oss titta närmare på, låt oss bryta ner det, här är vad du 
behöver veta, nu till det viktiga, utan vidare omsvep, en sak att ha koll på:, kort 
notering:, innan jag glömmer

**Problem:** AI annonserar nästa poäng i stället för att göra den. En vardaglig variant 
("en sak som bet mig ordentligt, så läs noga:") har samma problem. Ta bort annonseringen, 
inte bara dess formella ton.

**Innan:**
> Låt oss dyka ner i hur upphandlingen fungerar. Här är vad du behöver veta.

**Efter:**
> Upphandlingen sker i tre steg: annonsering, anbud och tilldelning.

---

### 24. Rubrik som upprepas i första meningen

**Problem:** AI följer ofta en rubrik med en mening som bara säger om rubriken innan det 
riktiga innehållet börjar. Stryk den meningen.

**Innan:**
> ## Leveranstider
>
> Leveranstiden är viktig.
>
> När kunder väntar mer än tre dagar avbryter var fjärde köpet.

**Efter:**
> ## Leveranstider
>
> När kunder väntar mer än tre dagar avbryter var fjärde köpet.

---

### 25. Forcerade punchlines och dramatiska fragment

**Problem:** AI gör varje mening till en slagkraftig slutrad. En kort mening kan ge 
eftertryck. En rad korta fragment känns konstruerad.

**Innan:**
> Sedan kom AI. Inga möten. Inga beslutsunderlag. Ingen väntan. Spelreglerna var borta.

**Efter:**
> När vi införde AI-verktyget försvann flera möten och beslutsunderlag, och väntetiderna 
> kortades. Det ändrade hur vi arbetar.

---

### 26. Formelartade talesätt

**Mönster att se upp med:**
X är det nya Y, data är den nya oljan, förtroende är den nya valutan, X är inte ett 
verktyg utan ett förhållningssätt, X är språket för Y, X blir en fälla, arkitekturen 
bakom X

**Problem:** AI gör om ett vanligt påstående till ett talesätt som låter djupt men inte 
tillför någon detalj. Ersätt talesättet med det konkreta påstående underlaget stödjer.

**Innan:**
> Data är den nya oljan. Effektivitet blir en fälla när teamen glömmer det mänskliga lagret.

**Efter:**
> Företag som samlar in köpdata kan prissätta bättre än de som inte gör det. Team som 
> optimerar processen för hårt missar ofta hur folk faktiskt använder den.

---

### 27. Låtsad uppriktighet

**Fraser att se upp med:**
Ärligt talat?, Låt oss vara ärliga:, Sanningen är att, Här är grejen:, Det är så här:, 
Rent krasst:, Om jag ska vara helt ärlig, när de används som fristående krokar eller 
konstpaus före en vanlig poäng.

**Problem:** AI inleder med en iscensatt paus eller ett anspråk på ärlighet före en 
rutinpoäng. Säg poängen direkt.

**Innan:**
> Är det värt pengarna? Ärligt talat? Det beror på hur ofta ni använder det.

**Efter:**
> Om det är värt pengarna beror på hur ofta ni använder det.

---

### 28. Svar på invändningar ingen gjort

**Fraser att se upp med:**
det här handlar inte (främst) om, jag säger inte att, jag menar inte att, för att vara 
tydlig, missförstå mig rätt, det betyder inte att, man kan förstås invända att... men, 
vissa skulle säga... men

**Problem:** AI bemöter en invändning som inte finns i texten. Var uppmärksam på ett 
påstående om vad skribenten *inte* menar, särskilt när ämnet inte nämns någon annanstans. 
Ett direkt påstående som "systemet är inte trådsäkert" är inte det här mönstret.

**Innan:**
> Det här handlar inte främst om budget, och jag säger inte att verktygen är oviktiga. 
> Man kan förstås se problemet på andra sätt, men frågan är om teamet kan använda 
> instruktionen när det gäller.

**Efter:**
> Frågan är om teamet kan använda instruktionen när det gäller.

Ta bara bort det ostödda försvaret. Innehåller det ett verkligt påstående, skriv ut det 
direkt. Behåll en invändning när texten namnger dess källa eller besvarar den fullt ut.

---

### 29. Avfärdande av påhittade alternativ

**Fraser att se upp med:**
ett frestande alternativ vore, man skulle kunna tänka sig att, det enkla vore att, en 
uppenbar lösning vore, du kanske tänker att... men, vissa skulle föreslå

**Problem:** AI lanserar ett alternativ ingen läsare skulle överväga, avfärdar det i en 
bisats och nämner det aldrig igen. Ofta är det en rest från ett tidigare utkast. Ta bort 
det påhittade alternativet och skriv den verkliga begränsningen direkt.

**Innan:**
> Vi fakturerar månadsvis. Ett frestande alternativ vore att fakturera per projekt, men 
> det skulle ge oförutsägbara intäkter. Faktureringen sker i stället löpande, och kunderna 
> får en samlad faktura.

**Efter:**
> Vi fakturerar månadsvis, och kunderna får en samlad faktura.

Ett enstaka avfärdat alternativ kan vara berättigat. Flera korta, orelaterade avfärdanden 
är ett starkare tecken. Fråga vad varje mening tillför. Registrerar den bara en tidigare 
redigering, skriv om stycket kring dess huvudpoäng.

---

## KONTROLLERA FALSKA POSITIVA

### Vad du inte ska flagga

En människa kan använda flera av mönstren ovan. Ta inte något av det här som bevis i sig:

- **Felfri grammatik och konsekvent stil.** Många skribenter är proffs eller har blivit 
  redigerade. Polish är inte AI.
- **Formella eller akademiska ord.** §18 listar specifika ord som AI överanvänder. 
  Förenkla inte varje formellt ord.
- **Ett enskilt "dessutom", "vidare" eller "därtill".** Övergångsord är AI-kodade först 
  när de staplas. Ett "dock" är inget tecken.
- **Tankstreck i sig.** Kort tankstreck är korrekt svenska och används flitigt av 
  journalister och redaktörer. Det är takten och det långa strecket (—) som räknas (§21).
- **Typografiska citattecken i sig.** Word, Google Docs och de flesta CMS gör om raka 
  citattecken automatiskt. Räknas bara ihop med andra tecken, eller när stilen är engelsk.
- **Passiv röst i myndighetstext och avtal.** "Beslutet överklagas till förvaltningsrätten" 
  är genrekorrekt. §5 gäller passiv som *falsk* formalitet, inte passiv som genrekrav.
- **En kort mening för eftertryck.** Flagga dramatiska fragment först när flera kommer i rad.
- **Avsiktligt upprepade starter.** "Vi kom. Vi såg. Vi levererade." kan vara rytm. Ändra 
  bara när upprepningen inte tillför något.
- **"Ärligt talat" eller "alltså" mitt i en mening.** Vanligt i vardaglig svenska. Tecknet 
  är den fristående teatrala öppningen, inte ordet.
- **Nödvändiga förbehåll.** Behåll avgränsningar, juridiska och säkerhetsrelaterade 
  upplysningar, verkliga rättelser, namngivna invändningar, svar och FAQ-svar.
- **Verkliga alternativ.** Behåll alternativ en läsare kan överväga i ett beslutsunderlag, 
  en guide eller ett resonemang. Ta bara bort ett osannolikt alternativ som texten avfärdar 
  och aldrig använder igen.
- **Källösa påståenden.** Det mesta på nätet saknar källhänvisning. Avsaknad av källor 
  bevisar ingenting.
- **Andrahandstext.** Skriv inte om bevakade fraser inuti citat, titlar, egennamn eller 
  exempel där frasen diskuteras snarare än används.
- **Sammansatta ord.** "Datadriven" och "kundfokuserad" är korrekt svenska. Särskrivning 
  ("data driven") är ett språkfel, inte ett AI-tecken.

När du är osäker: leta efter flera mönster tillsammans. Ett tankstreck bevisar ingenting. 
Flera standardmönster i samma stycke är starkare bevis.

### Mänskliga detaljer att behålla

De här detaljerna bär ofta skribentens röst. Behåll dem om de inte skadar betydelsen:

- **Specifika, udda detaljer.** En riktig adress, ett konstigt citat, "revisorn som satt 
  en trappa upp från min tandläkare".
- **Blandade känslor och olösta spänningar.** "Jag tycker att det här mest är bra, men 
  något skaver, och jag kan inte riktigt förklara vad."
- **Tidsbundna referenser.** Slang, memes eller interna skämt som hör till ett visst år 
  och en viss krets. Modeller ligger ett år eller mer efter.
- **Medvetna förstapersonsval.** Behåll ett ordval eller en strykning skribenten kan 
  motivera.
- **Variation i meningslängd.** Riktig text växlar kort och lång. AI-text tenderar mot en 
  jämn, medellång takt.
- **Genuina utvikningar, parenteser och självrättelser.** "(Jag vill hela tiden skriva 
  'nästan' här, men det var faktiskt säkert.)" Modeller avbryter sällan sig själva så.
- **Text skriven före 30 november 2022.** ChatGPT:s lansering. Äldre text är, med mycket 
  få undantag, inte AI-skriven.

---

## REGISTER PER TEXTTYP

### Affärsskrivande (mejl, offerter, presentationer, intern kommunikation)
- Aktiv röst, första person naturligt
- Konkreta siffror och åtgärder
- Inga brasklappar om det inte finns en verklig osäkerhet att kommunicera
- Struktur som gör det lätt att fatta beslut

### Rapportskrivande (analyser, sammanfattningar, strategidokument)
- Faktapåståenden med källa eller tydlig härledning
- Analytisk röst som faktiskt drar slutsatser, inte bara listar observationer
- Aktivt subjekt: "vi rekommenderar", inte "det rekommenderas"
- Exekutiv sammanfattning som faktiskt sammanfattar, inte introducerar ämnet

### Artiklar och redaktionellt (branschkommentar, thought leadership)
- Öppna med ett konkret påstående, inte en kontextbeskrivning
- Egna åsikter med tydlig grund
- Erkänn vad du inte vet
- Avsluta med ett omdöme, inte en öppen fråga

### Sociala medier
- Öppna med det specifika, inte det generella
- Bygg på en verklig erfarenhet eller ett konkret exempel
- CTA som är kopplad till en faktisk fråga, inte ett generellt "vad tänker du?"
- Max 3 hashtags, välj dem utifrån relevans inte ambition

---

## PROCESS

1. Om texttypen är oklar: fråga innan du börjar
2. Läs texten noggrant
3. Identifiera alla AI-mönster ovan
4. Identifiera texttypen och applicera rätt register från sektionen ovan
5. Skriv om varje problematiskt avsnitt
6. Kontrollera att den reviderade texten:
   - Låter naturlig när man läser den högt på svenska
   - Varierar meningslängd och struktur
   - Använder specifika detaljer framför vaga påståenden
   - Har en röst som äger en ståndpunkt
7. Ställ frågan: **"Vad avslöjar att det här fortfarande är AI-genererat?"**
8. Svara kort med kvarvarande tecken
9. Ställ frågan: **"Vad saknar texten för att låta skriven av en verklig person med 
   en verklig åsikt?"** (hoppa över för rapporter och annan saklig text)
10. Ställ frågan: **"Har omskrivningen lagt till eller tagit bort någon uppgift, ett namn, 
    en siffra, ett datum, ett citat, en källa eller en rangordning?"** Varje tillägg utan 
    stöd i underlaget och varje tappat påstående är ett fel. Rätta det.
11. Sök efter — och räkna – som inskott (§21)
12. Revidiera och presentera slutversionen. Formulera varje poäng naturligt i stället för 
    att lappa en flaggad fras i taget. Är en mening fortfarande stel, skriv om stycket 
    kring dess huvudpoäng.

## Så returnerar du resultatet

**Inklistrad text (standard).** Returnera:
1. Utkast till omskrivning
2. "Vad avslöjar att det här är AI-genererat?" (korta punkter)
3. Slutlig version
4. Kort sammanfattning av ändringar (valfritt, om det tillför värde)

**Filläge.** När användaren pekar på en fil: kör hela processen men skriv bara slutversionen 
till filen. Ändra bara löptext. Rör inte kodblock, YAML-metadata, tabelldata eller länkmål. 
Ge sedan användaren en kort sammanfattning.

**Inbäddat läge.** När en annan uppgift använder den här färdigheten för ett mejl, en 
PR-beskrivning, ett commit-meddelande eller ett dokument: returnera bara slutversionen.

---

## FULLSTÄNDIGA EXEMPEL

Siffror, källor och kundcase i exemplen nedan är illustrativa: de visar vilken *typ* av 
konkretion som ersätter AI-mönstren. I ett verkligt uppdrag får sådana uppgifter bara komma 
från underlaget eller användaren (Din uppgift, punkt 4). Saknas de: fråga, eller skriv enklare.

---

### Exempel 1: Affärsskrivande

**Innan (AI-text):**
> I dagens alltmer digitaliserade affärsklimat är det avgörande att företag proaktivt 
> navigerar de möjligheter och utmaningar som den teknologiska utvecklingen medför. 
> Vår lösning utgör ett banbrytande verktyg som möjliggör en mer effektiv och hållbar 
> affärsprocess. Det är viktigt att notera att implementeringen av denna strategi 
> bidrar till en ökad förståelse för kundernas behov, vilket i sin tur lyfter fram 
> värdet av ett datadrivet arbetssätt. Sammantaget representerar detta en unik möjlighet 
> att ta ägarskap över er digitala transformation och säkerställa långsiktig tillväxt.

**Utkast till omskrivning:**
> Verktyget är byggt för att lösa ett konkret problem: för lång tid mellan kunddata 
> och affärsbeslut. I dag tar det i genomsnitt tre veckor från att ett köpmönster 
> förändras tills att sortimentet speglar det. Med vår plattform är det nere på 48 timmar. 
> Det är inte en digital transformation, det är en kortare loop.

**Vad avslöjar att det här fortfarande är AI-genererat?**
- "I dag" och "48 timmar" är bra men vi gör ett antagande om tidsramarna som borde 
  antingen bekräftas med ett riktigt kundcase eller mjukas upp
- "Det är inte en digital transformation, det är en kortare loop" riskerar att låta 
  som en konstruerad one-liner

**Slutlig version:**
> Det tar ofta tre veckor från att ett köpmönster ändras tills sortimentet hinner med. 
> Vi har sett det hos de flesta av de grossister vi arbetar med. Plattformen kortar 
> den loopen till 48 timmar, baserat på samma data ni redan har men med en annan 
> uppdateringsfrekvens. Inget du behöver bygga om, bara koppla in.

---

### Exempel 2: Rapportskrivande

**Innan (AI-text):**
> Denna rapport belyser vikten av ett strukturerat förhållningssätt till 
> hållbarhetsarbete inom den svenska detaljhandeln. Det kan konstateras att branschen 
> befinner sig i en fas av betydande förändring, driven av såväl regulatoriska krav 
> som förändrade konsumentbeteenden. Experter menar att företag som inte anpassar sig 
> riskerar att förlora marknadsandelar. Rapporten understryker behovet av en holistisk 
> strategi som tar hänsyn till samtliga intressenter. Avslutningsvis kan vi konstatera 
> att möjligheterna är stora för de aktörer som väljer att agera proaktivt.

**Utkast till omskrivning:**
> Den svenska detaljhandeln möter två motstridiga krav på hållbarhet: EU:s 
> rapporteringsdirektiv CSRD kräver mer granulär data, medan konsumenternas 
> faktiska köpbeteende fortfarande prioriterar pris. Rapporten undersöker hur 
> 40 svenska detaljhandelsbolag hanterar den spänningen i praktiken.

**Vad avslöjar att det här fortfarande är AI-genererat?**
- Inget egentligt, men "i praktiken" i slutmeningen riskerar att bli en tom utfyllnad 
  om rapporten sedan inte levererar praktiska exempel

**Slutlig version:**
> Den svenska detaljhandeln möter två motstridiga krav: EU:s CSRD-direktiv kräver 
> detaljerad hållbarhetsrapportering från och med 2025, medan konsumentdata visar 
> att pris fortfarande är det primära köpkriteriet för 68% av svenska konsumenter 
> (HUI Research, 2024). Den här rapporten undersöker hur 40 svenska detaljhandelsbolag 
> navigerar spänningen, vad som faktiskt förändrats i verksamheten och vad som 
> stannat vid presentationslagret.

---

### Exempel 3: Artikel

**Innan (AI-text):**
> I en värld där digitaliseringen omformar spelplanen i grunden spelar retail media 
> en alltmer central roll för hur varumärken kommunicerar med sina kunder. Det råder 
> ingen tvekan om att detta skifte representerar en av de mest betydelsefulla 
> förändringarna inom marknadsföring på decennier. Branschkällor pekar på att 
> investeringarna förväntas fördubblas inom de närmaste åren. Å ena sidan erbjuder 
> detta nya möjligheter för annonsörer, å andra sidan ställer det höga krav på 
> transparens och mätbarhet.

**Utkast till omskrivning:**
> Retail media är inte ett nytt annonsformat. Det är ett maktskifte. Handlarna 
> sitter nu på den data som varumärkena har velat ha i tio år: vem som faktiskt 
> köper, hur ofta och i vilka kombinationer. Frågan är vad de gör med det.

**Vad avslöjar att det här fortfarande är AI-genererat?**
- "Maktskifte" är bättre än "banbrytande" men fortfarande ett lite töjt påstående 
  utan faktaunderlag direkt efteråt
- Tredje meningen stannar vid en fråga utan att ens antyda ett svar

**Slutlig version:**
> Retail media är inte ett nytt annonsformat. Det är ett maktskifte.
>
> I tio år har varumärken betalat Google och Meta för att gissa sig till köpintentionen. 
> Nu sitter ICA, Coop och Zalando på den faktiska köphistoriken och säljer tillgången 
> till den. Enligt eMarketer uppgick de globala retail media-investeringarna till 
> 140 miljarder dollar 2024. Omfördelningen av annonsbudgeten pågår redan.
>
> Problemet är att transparensen haltar. Många retailers kan inte redovisa 
> inkrementalitet, bara klick. Det är inte tillräckligt för annonsörer som vill 
> veta om exponeringen faktiskt drev en ny försäljning eller bara mätte en som 
> ändå hade skett.

---

### Exempel 4: Sociala medier

**Innan (AI-text):**
> I takt med att AI förändrar spelreglerna inom marknadsföring är det avgörande 
> att vi som yrkesverksamma håller oss uppdaterade och proaktivt anpassar våra 
> strategier. Det är inte längre en fråga om om, utan när. Företag som lyckas 
> integrera AI på ett genomtänkt och holistiskt sätt kommer att ha en tydlig 
> konkurrensfördel framåt. Vad tänker du – hur navigerar du förändringen?
>
> #AI #Marknadsföring #DigitalTransformation #Framtid #Innovation

**Utkast till omskrivning:**
> Vi bytte ut vår brief-process med ett AI-verktyg i höstas. Resultatet: brieferna 
> är längre men sämre strukturerade. Inte för att verktyget är dåligt, utan för att 
> vi inte hade en tydlig briefstandard att börja med. AI synliggjorde ett hål vi 
> inte visste att vi hade.
>
> Vad har du lärt dig av att implementera AI i ett befintligt arbetssätt?
>
> #Marknadsföring #AI #Processutveckling

**Vad avslöjar att det här fortfarande är AI-genererat?**
- "Synliggjorde ett hål" är lite klyschigt
- Frågan i slutet är bättre eftersom den är specifik, men den kan bli ännu vassare

**Slutlig version:**
> Vi bytte ut vår brief-process med ett AI-verktyg i höstas.
>
> Brieferna blev längre. Men inte bättre.
>
> Problemet var inte verktyget, det var att vi inte hade en tydlig standard att 
> börja med. AI:n förstärkte det vi matade in, och det vi matade in var halvfärdiga 
> tankar som vi tidigare hade löst muntligt i rummet.
>
> Nu har vi en briefstandard. Verktyget fyller ut den, inte ersätter den.
>
> Har du upplevt att AI avslöjat ett processproblem du inte visste att du hade?
>
> #Marknadsföring #AI #Processutveckling

---

## Snabbreferens: Vanliga byten

| AI-svenska | Mänsklig svenska |
|---|---|
| "det kan konstateras att" | skriv påståendet direkt |
| "belyser vikten av" | stryk eller skriv vad som är viktigt och varför |
| "i en alltmer digitaliserad värld" | stryk, börja med din faktiska poäng |
| "sammantaget representerar detta" | stryk, avsluta med det konkreta |
| "navigera förändringen" | "hantera det", "hitta rätt", eller specificera vad |
| "proaktivt" | "tidigt", "i förväg", eller stryk |
| "holistiskt" | "i sin helhet", eller specificera vad du menar |
| "ta ägarskap över" | "ansvara för", "driva" |
| "implementeringen av" | "att implementera", "när vi inför" |
| "å ena sidan... å andra sidan" | ta ställning |
| "möjligheterna är stora" | vilka möjligheter? för vem? |
| "avgörande" | varför? bevis? |
| "banbrytande" | stryk |
| "vittnar om" | "visar", "tyder på" |
| "utgör" | "är" |
| "representerar" | "är" |
| "fungerar som" | "är" (om det är en synonym) |
| "möjliggör" | "gör det möjligt", "låter oss" |
| "det är viktigt att notera" | skriv vad som är viktigt direkt |
| "avslutningsvis" | stryk, avsluta med substansen |
| "Vilken bra fråga!" | stryk |
| "Hoppas det hjälper!" | stryk |
| "i syfte att uppnå" | "för att" |
| "på grund av det faktum att" | "eftersom" |
| "i nuläget" / "i dagsläget" | "nu" |
| "baserat på tillgänglig information" | stryk, skriv vad du vet och varifrån |
| "det kan möjligen argumenteras att" | ta ställning eller skriv ut osäkerheten konkret |
| "kan beskrivas som" | "är" |
| 💡 🚀 ✅ 📊 som dekorativa avdelare | stryk |
| fetstilta rubriker i löptext | stryk om det inte är en faktisk rubrik |
| "ledande", "unik", "i världsklass", "sömlös" | stryk, beskriv vad det är |
| "dessutom / vidare / därtill" som styckeöppnare | stryk, eller behåll ett |
| "företaget / bolaget / organisationen / aktören" om samma sak | välj ett ord |
| "från strategi till genomförande, från insikt till handling" | lista det som faktiskt ingår |
| — (långt tankstreck) | – , komma eller punkt |
| – som inskott i varannan mening | komma eller punkt; matcha textprovets takt |
| “engelska citattecken” | ”svenska” eller raka " |
| "Varför Kultur Slår Teknik" | "Varför kultur slår teknik" |
| "den egentliga frågan är", "i grund och botten" | säg poängen |
| "låt oss dyka ner i", "här är vad du behöver veta" | stryk, börja med innehållet |
| Färre möten. Bättre beslut. Punkt. | skriv ihop till en mening |
| "X är det nya Y", "data är den nya oljan" | det konkreta påståendet |
| "Ärligt talat?", "Här är grejen:" | stryk, säg poängen |
| "jag säger inte att", "missförstå mig rätt" | stryk om ingen har invänt |
| "ett frestande alternativ vore" | stryk alternativet, skriv begränsningen |
| "troligen", "det är rimligt att anta" som fakta | skriv vad underlaget visar, eller stryk |
| en siffra eller källa som inte finns i underlaget | fråga, eller skriv utan |
