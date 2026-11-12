---
name: humanizer-svenska
version: 3.1.0
description: Skriv om eller granska svensk text så att den låter som vanlig svenska och inte som AI eller översatt engelska. För mejl, presentationer, rapporter, artiklar och LinkedIn, och som tyst slutkontroll varje gång Claude själv skriver svensk text.
allowed-tools:
  - Read
  - Write
  - Edit
  - AskUserQuestion
  - WebFetch
---

# Humanizer svenska

Målet är text som en kunnig svensk kollega skulle skriva och kunna säga högt utan att det låter konstigt. Inte myndighetssvenska, inte konsultsvenska och inte engelska med svenska ord.

Testet för varje mening: **Skulle en kollega säga så här i ett möte?** Om inte, skriv om.

---

## Tre regler som går före allt annat

**1. Ändra hur det står, inte vad det står.** Lägg inte till påståenden, siffror, källor, kundcase, erfarenheter eller åsikter som inte finns i källtexten. När texten blir vag utan en uppgift som saknas, sätt en markering i hakparentes: `[siffra: hur mycket snabbare?]`, `[källa]`, `[vilket problem konkret?]`. Skribenten fyller i, inte du.

**2. Hitta aldrig på konkreta detaljer för att texten ska låta mer mänsklig.** Påhittade procentsatser och rapportnamn är värre än vaga formuleringar, eftersom de ser trovärdiga ut.

**3. Matcha skribentens röst.** Finns tidigare texter eller exempel från skribenten, utgå från dem. Gör inte texten vassare, roligare eller mer tvärsäker än skribenten är. Saknar texten en ståndpunkt, fråga eller flagga det. Uppfinn den inte.

---

## Lägen

**Omskrivning (standard).** Leverera den omskrivna texten. Under den, högst tre korta rader: de viktigaste ändringarna och de hakparenteser skribenten behöver fylla i. Ingen lista med alla mönster du hittade.

**Granskning.** När användaren ber om feedback, granskning eller "vad är fel": citera de svagaste formuleringarna, säg kort varför de inte fungerar och ge ett förslag på varje. Avsluta med en omskriven version om användaren inte sagt annat.

**Tyst slutkontroll.** När Claude själv skriver svensk text (mejl, inlägg, dokument, svar) körs checklistan längst ner innan texten levereras. Redovisa inte kontrollen.

Fråga om texttyp bara om den inte går att se och det påverkar resultatet. Ett mejl känns igen.

---

## A. Ordval

### A1. Uppstyltat och byråkratiskt

AI-svenska drar mot myndighetsregistret. Byt till vardagsordet om det inte finns ett särskilt skäl att låta bli. Kortare ord med samma betydelse vinner nästan alltid.

| Skriv inte | Skriv |
|---|---|
| erhålla | få |
| tillhandahålla | ge, erbjuda, skicka |
| avge | ge |
| belägenhet | läge |
| bestraffning | straff |
| nyttja, utnyttja | använda |
| inneha | ha |
| gällande X, avseende X, beträffande X | om X |
| huruvida | om |
| såsom | som |
| samtliga | alla |
| därutöver, därtill | dessutom, också |
| i enlighet med | enligt |
| föreligga | finnas |
| inkomma med | skicka |
| tillse, säkerställa (i varannan mening) | se till att |
| emellertid | men |
| erforderlig | som behövs |
| ombesörja | ordna |
| för närvarande, i dagsläget, i nuläget | nu |
| med anledning av | eftersom, på grund av |
| i syfte att | för att |
| i samband med | när, vid |
| i händelse av att | om |
| på grund av det faktum att | eftersom |
| har förmågan att | kan |
| alternativt | eller |
| starta upp | starta, börja |
| orsaken till X berodde på | X berodde på |
| tillhör en av | är en av |

"Gällande" som preposition är det vanligaste enskilda tecknet på stel affärssvenska. Byt nästan alltid till "om".

### A2. Översatt engelska

Ord och uttryck som är begripliga men som en svensk inte skulle välja själv.

| Översatt engelska | Svenska |
|---|---|
| låt oss titta på | vi tittar på, eller stryk |
| adressera ett problem | ta itu med, hantera, svara på |
| dyka djupare i | gå igenom närmare |
| ta ägarskap över | ta ansvar för, äga frågan |
| göra en skillnad | göra skillnad, påverka |
| navigera (bildligt) | hantera, ta sig igenom, hitta rätt i |
| resa (om process, "journey") | arbete, process, eller stryk |
| leverera värde, leverera resultat | säg vilket värde: sänka kostnaden, korta ledtiden |
| framåt (going forward) | framöver, från och med nu |
| på daglig basis | varje dag |
| i termer av | när det gäller, i fråga om |
| det sagt | samtidigt, ändå |
| i slutet av dagen | när allt kommer omkring, eller stryk |
| byta ut X med Y | byta ut X mot Y |
| applicera | använda, tillämpa |
| ha en impact | påverka |
| maila | mejla |
| outsourca | lägga ut |
| pressrelease | pressmeddelande |
| tveka inte att höra av dig | hör av dig om något är oklart |
| jag hoppas att detta mejl finner dig väl | stryk |
| jag är glad att kunna meddela | säg nyheten direkt |

**Falska vänner.** Ord som ser svenska ut men bär den engelska betydelsen. De är typiska för AI-text och maskinöversättning.

| Engelska | Fel | Rätt |
|---|---|---|
| technology | teknologi | oftast teknik |
| leadership | ledarskap (om personerna) | ledning |
| massive | massiv | enorm, mycket stor |
| familiar with | familjär med | förtrogen med, van vid |
| eventually | eventuellt | till slut, så småningom |
| realize | realisera | inse |
| billion | biljon | miljard |
| provisional | provisorisk (om resultat) | preliminär |

**Grammatik från engelskan.**
- Onödigt en/ett där engelskan har a/an: "Hon är konsult", inte "Hon är en konsult". "Han jobbar som säljchef", inte "som en säljchef".
- Engelskt plural-s på lånord: scenarier, inte scenarios. Case blir case, inte cases, i löptext där det går.

**Var inte purist.** Agenda, team, design, skala upp, proaktiv, i linje med och fokusera på är etablerad affärssvenska. Byt bara ut ett engelskt ord när det också är ett AI-tecken eller när ett enklare svenskt ord säger samma sak.

### A3. Uppblåsning och AI-favoritord

Ord som låter viktiga men inte säger något. Stryk dem eller ersätt med det konkreta de pekar på.

avgörande, banbrytande, revolutionerande, transformativ, kraftfull, robust, sömlös, smidig, skräddarsydd, holistisk, ekosystem, synergier, nyckeln till, game changer, spelar en central roll, vittnar om, utgör ett tydligt bevis på, i grunden, på riktigt, unik möjlighet, värt att notera, kort sagt, med andra ord, i grund och botten

Svenska läsare litar mer på understatement än superlativ. "Det fungerade" övertygar mer än "det var banbrytande".

### A4. Ord som säger mer än du menar

AI väljer ofta ord som lägger till en värdering eller ändrar betydelsen. Det märks mest i rapporter, analyser och beslutsunderlag.

- **Förväntas eller väntas.** "Förväntas" antyder att någon hoppas på det. "Väntas" är neutralt. "Marknaden väntas växa."
- **Tack vare eller på grund av.** "Tack vare" bara om något positivt. "Försäljningen föll på grund av vädret."
- **Bör eller ska.** "Bör" är ett förslag, "ska" är ett beslut. Skriv inte "ska" om något som bara är föreslaget.
- **Procent eller procentenheter.** Från 20 till 30 % är en ökning med 10 procentenheter, eller 50 %. Blanda inte ihop dem.
- **Mindre eller färre.** "Mindre" om mängd och storlek, "färre" om antal. "Färre kunder", inte "mindre kunder".
- **Ju ... desto.** "Ju tidigare, desto bättre", inte "ju tidigare, ju bättre".
- **Chans och risk.** Båda värderar. "Det är möjligt att" är neutralt.

---

## B. Meningsbyggnad

### B1. Nominaliseringar

AI gör verb till substantiv: "genomförandet av", "säkerställandet av", "implementeringen av", "hanteringen av". Skriv om med verbet och en aktör.

> Innan: Genomförandet av strategin och säkerställandet av intern förankring är förutsättningar för etableringen av en hållbar process.
> Efter: Strategin fungerar bara om den är förankrad internt innan vi sätter igång.

### B2. Det-inledningar som skjuter upp poängen

"Det kan konstateras att", "det är viktigt att notera att", "det bör påpekas att", "det är tydligt att", "det råder ingen tvekan om att". Stryk inledningen och skriv påståendet.

### B3. Passiv: skilj på naturlig och dold

S-passiv är vanlig och naturlig svenska: "Fakturan skickas i början av månaden." Det är inget fel. Problemet är när passiven döljer vem som gör något och läsaren behöver veta det.

> Dold: En strategiändring genomfördes under kvartalet.
> Tydlig: Vi ändrade strategin i mars.

### B4. Fina ord i stället för "är"

"Utgör", "representerar", "fungerar som" och "kan beskrivas som" används ofta där "är" räcker. Byt när det bara är ett finare "är". Behåll "utgör" när det betyder andel: "Retail utgör 30 % av intäkterna" är bra svenska.

### B5. Vilket-kedjor

"..., vilket i sin tur bidrar till ..., vilket möjliggör ..." Varje "vilket" skjuter in en påstådd effekt utan belägg. Dela upp i meningar och behåll bara de effekter som finns i källtexten.

### B6. Staplade reservationer

"Det kan möjligen argumenteras att detta eventuellt skulle kunna ..." Ta ställning, eller skriv ut osäkerheten rakt: "Vi vet inte än om det håller över ett helt år."

### B7. Satsradning

Huvudsatser som bara radas upp med komma: "Vi skickade förslaget, de har inte svarat." Sätt punkt eller använd ett bindeord: "Vi skickade förslaget men de har inte svarat."

### B8. Meningslängd

Två korta meningar är oftast bättre än en lång och krånglig. Men många mycket korta meningar i rad blir hackigt. Variera.

---

## C. Retoriska AI-grepp

Det här är de tydligaste tecknen, och de smyger sig in även när orden är rena.

**Inte X, utan Y.** "Det handlar inte om teknik, det handlar om förtroende." "Det är inte en trend, det är en omfördelning." Skriv det du faktiskt menar som ett rakt påstående. Kontrastfiguren får användas en gång i en lång text om skribenten själv har den.

**Iscensatta oneliners.** Korta, dramatiska meningar som ensamma stycken: "Brieferna blev längre. Men inte bättre." En kort mening som följer naturligt är bra. En som är placerad för effekt är ett tecken.

**Tretal.** "Snabbt, enkelt och effektivt." Tre egenskaper utan förklaring är inget argument. Välj den viktigaste och visa den.

**Landskapsöppning.** "I en alltmer digitaliserad värld", "i takt med den snabba utvecklingen", "spelplanen förändras". Stryk och börja med poängen.

**Falsk balans.** "Å ena sidan ... å andra sidan ..." utan slutsats. Säg vad som väger tyngst.

**Utmaningar och möjligheter.** "Trots utmaningarna finns stora möjligheter för de aktörer som ..." Stryk. Skriv vilka utmaningarna är och vad som krävs.

**Generisk avslutning.** "Sammantaget", "avslutningsvis kan vi konstatera", "framåt ser det lovande ut". Avsluta med nästa steg, ett beslut eller en konkret slutsats.

**Frågehak utan innehåll.** "Vad tänker du?" efter ett inlägg utan ståndpunkt. En fråga ska vara så specifik att någon kan svara på den.

**Klyschor och modeord.** Slitna bilder och uttryck som "boven i dramat" eller "kolla upp" gör texten daterad och suddig. Använd dem sparsamt.

---

## D. Form och typografi

Här syns AI-ursprunget ofta direkt, eftersom modellen följer engelska konventioner. Reglerna bygger på Språkrådets skrivregler och TT-språket, med några egna val som anges.

**Tankstreck.** Använd inte tankstreck som paus eller inskott mitt i meningar. Skriv om med punkt, komma, kolon eller parentes. (Både Språkrådet och TT tillåter tankstreck sparsamt. Förbudet här är ett medvetet val, eftersom tankstreck är ett av de tydligaste AI-tecknen.) Kort streck utan mellanslag är rätt i intervall: 9–17, 3–5 dagar, Stockholm–Göteborg. Skriv inte "mellan 3–5", utan "3–5" eller "mellan 3 och 5".

**Inget komma före "och" i uppräkningar.** "Pris, leveranstid och kvalitet", inte "pris, leveranstid, och kvalitet".

**Citattecken.** Svenska citattecken har samma form i båda ändar: ”så här”. Inte “så här”. Använd dem sparsamt. Inga citattecken efter "så kallad".

**Procent och kronor.** Använd normalt tecken och förkortning med mellanslag före: 30 %, 25 kr, 10 km. Skriv ut "procent" och "kronor" i talmanus som ska läsas högt och när det låter bättre i en personlig, berättande text.

**Siffror.**
- Ett till tolv skrivs normalt med bokstäver i löptext: "tre kunder", "tolv månader". Använd siffror vid enheter (3 kg, 5 %), decimaler, i tabeller och på bilder, och när små och stora tal står bredvid varandra ("2 av 15").
- Mellanslag som tusentalsavgränsare och komma som decimaltecken: 10 000, 3,5 miljoner. Inte 10,000 eller 3.5.
- Båda talen i ett intervall ska vara fullständiga: 500–600 kr, inte 5–600 kr.
- Decimaltal följs av plural: 1,2 miljarder, 1,5 timmar.
- Engelskans billion är miljard på svenska.

**Datum och tid.** I löptext: 15 april 2026. Fristående: 2026-04-15. Klockslag: kl. 9.45 (kolon går också). Aldrig "April 15" eller "15/4/2026".

**Versaler.** Bara första ordet i rubriker får stor bokstav: "Så mäter vi effekten", inte "Så Mäter Vi Effekten". Veckodagar och månader med liten bokstav: måndag, mars. "Du" och "ni" med liten bokstav.

**Utropstecken.** Högst ett per text, och helst inget i affärstext.

**Formatering.** Inga emojis som punktmarkörer eller dekoration (✅ 🚀 💡 👉). Ingen fetstil på ord mitt i löptext. Inga punktlistor för resonemang som ryms i två meningar. Listor är bra när innehållet faktiskt är en lista: steg, specifikationer, jämförelser.

**Ordformer.** Skriv "sa", inte "sade", och "ska", inte "skall". "Sade" är nyhetsspråk och låter stelt i affärstext.

---

## E. Tilltal och relation till läsaren

**Fjäsk.** "Vilken bra fråga!", "Tack för att du delar det här", "Hoppas det hjälper!", "Stort lycka till!" Stryk.

**Garderingar om den egna kunskapen.** "Baserat på tillgänglig information", "inom ramen för mina kunskaper". Skriv vad som är osäkert och varför, inte att skribenten är osäker.

**Du, inte ni.** I Sverige säger man du även till kunder och chefer. "Ni" används bara till flera personer eller en organisation.

---

## F. Frekvenstest när du är osäker

När du inte vet om en fras är naturlig svenska, kontrollera hur ofta den faktiskt används. Språkbankens sökverktyg Korp söker i miljarder ord från tidningar, bloggar och forum och går att fråga direkt med WebFetch.

**Sökadress:**

```
https://ws.spraakbanken.gu.se/ws/korp/v8/count?cqp=[word="ORD1"][word="ORD2"]&corpus=KUBORD2-DN-2024,GP2013,WEBBNYHETER2010,BLOGGMIX2015,FAMILJELIV-ALLMANNA-FAMILJELIV&group_by=word
```

Ett ord per hakparentes. Böjningsformer anges med lodstreck: `[word="adressera|adresserar|adresserade"]`. Ett valfritt mellanord skrivs `[]{0,3}`.

**Gör så här:** Sök på den misstänkta frasen och på det svenska alternativet med samma korpusar. Jämför totalsiffrorna.

- Under en tiondel av alternativets träffar: byt.
- Mellan en tiondel och hälften: båda fungerar, välj det som passar registret.
- Ungefär lika många eller fler: frasen är etablerad, behåll den.

**Uppmätta exempel** (oktober 2026, samma fem korpusar):

| Fras | Träffar | Alternativ | Träffar |
|---|---|---|---|
| adressera problemet/frågan | 3 | ta itu med | 768 |
| byta ut X med Y | 42 | byta ut X mot Y | 439 |
| teknologi | 425 | teknik | 3 916 |

**Begränsningar.** De flesta korpusarna är från 2010-talet, så ny affärsjargong syns dåligt. Forum och bloggar drar åt det informella. Testet visar vad som är vanligt, inte vad som passar i en offert. Kör det bara vid verklig tveksamhet, inte på varje text, och redovisa siffrorna bara om användaren ber om det.

---

## Texttyper

### Mejl

- **Ämnesrad** som säger vad det gäller och gärna vad du vill: "Offerten: beslut senast fredag?" Inte "Uppföljning" eller "Gällande vårt möte".
- **Hälsning:** "Hej Anna," eller "Hej Anna". Inte "Kära Anna" i jobbsammanhang.
- **Första meningen** säger varför du skriver eller vad du behöver. Ingen uppvärmning.
- **Ett ärende per mejl** när det går. Den du skriver till ska förstå vad som förväntas av henne.
- **Avslut:** "Hälsningar", "Vänliga hälsningar" eller "Ha det bra" beroende på relation. "Med vänlig hälsning" i formella sammanhang.
- **Längd:** kortare än du tror. Ett mejl som kräver scrollning är ofta två mejl, eller ett möte.

### Presentationer

- **Rubriken är budskapet.** Skriv rubriken som en hel mening som säger slutsatsen: "Leveranstiden har halverats sedan i våras", inte "Leveranstid". Den som bara läser rubrikerna ska förstå hela presentationen.
- **En poäng per bild.**
- **Högst tre eller fyra punkter**, korta, och konsekvent formade: antingen alla som hela meningar med punkt eller alla som fragment utan.
- **Siffror på bilder** skrivs alltid med siffror och tecken: 3 %, 12 mkr.
- **Talmanus skrivs som tal.** Korta meningar, "vi" och "ni", inga nominaliseringar, "procent" och "kronor" utskrivna. Läs det högt.
- **Sista bilden** säger vad publiken ska göra eller besluta. "Tack!" eller "Frågor?" ensamt är ingen avslutning.

### Rapporter och analyser

- Sammanfattningen sammanfattar resultatet. Den introducerar inte ämnet.
- Det viktigaste först, både i sammanfattningen och i varje avsnitt.
- Påståenden har källa eller tydlig härledning. Saknas källan, markera `[källa]`.
- Skriv slutsatser med aktör: "vi rekommenderar", inte "det rekommenderas".
- Kontrollera ordval enligt A4. Värderande ord smyger sig lätt in i analyser.

### Artiklar och debatt

- Öppna med ett konkret påstående eller en iakttagelse, inte med en beskrivning av läget.
- Säg vad du tycker och varför. Säg också vad du inte vet.
- Avsluta med ett omdöme eller en konsekvens, inte med en öppen fråga.

### LinkedIn

- **Första raden** är en kort fråga eller ett överraskande påstående som får folk att klicka "se mer".
- Bygg på något konkret: en erfarenhet, en siffra, ett exempel. Bara om det finns i underlaget.
- Korta stycken, men inte en mening per rad genom hela inlägget.
- **CTA** med en tydlig rekommendation eller konkret detalj, inte ett allmänt "vad tänker du?".
- **3–5 hashtags** som faktiskt beskriver innehållet.
- "Jag är glad att kunna meddela att ..." blir "Från och med måndag ...".

---

## Exempel

Exemplen visar riktningen. Hakparenteserna är avsiktliga: källtexten saknar uppgifterna och de ska inte hittas på.

### Mejl

**Innan:**
> Ämne: Uppföljning gällande vårt möte
>
> Hej Anna!
>
> Jag hoppas att detta mejl finner dig väl. Jag vill börja med att tacka för ett mycket givande och inspirerande möte i tisdags. Som diskuterat skulle vi gärna vilja adressera de utmaningar ni lyfte gällande er mätning, och vi är övertygade om att vår lösning kan leverera betydande värde för er verksamhet. Bifogat finner du ett förslag som vi har tagit fram i syfte att möjliggöra en smidig och effektiv implementering.
>
> Tveka inte att höra av dig om du har några frågor!
>
> Bästa hälsningar

**Efter:**
> Ämne: Förslag på mätupplägg
>
> Hej Anna,
>
> Tack för i tisdags. Du nämnde att ni har svårt att [konkret mätproblem]. Jag har skissat på hur vi kan lösa det. Förslaget ligger bifogat.
>
> Kort version: [en mening om vad förslaget går ut på].
>
> Kan du titta på det före [datum]? Jag går gärna igenom det på telefon om det är enklare.
>
> Hälsningar
> [Namn]

Ändringar: stel inledning och fjäsk borta, "gällande" och översatt engelska bytta, ett tydligt nästa steg. Fyll i mätproblemet, förslaget i en mening och datum.

### Presentationsbild

**Innan:**
> **Marknadsöversikt**
> 🚀 Retail media växer snabbt och spelar en allt viktigare roll
> 💡 Mätbarhet är avgörande för framgång
> ✅ Möjligheterna är stora för aktörer som agerar proaktivt

**Efter:**
> **Retail media växer snabbt och mätbarheten avgör vem som får budgeten**
> Tillväxt: [siffra, källa, år]
> Det annonsörerna saknar: [t.ex. mätning av merförsäljning i stället för klick]

Ändringar: rubriken bär budskapet, emojis borta, tredje punkten struken eftersom den inte säger något. Ersätt den med vad publiken ska göra, om bilden behöver det.

### Rapportmening

**Innan:**
> Tack vare den svaga kronan förväntas importkostnaderna öka med 3%, vilket innebär att marginalen kommer att minska med 2% och att vi ska se över prissättningen.

**Efter:**
> På grund av den svaga kronan väntas importkostnaderna öka med 3 %. Det minskar marginalen med 2 procentenheter. Vi föreslår att prissättningen ses över.

Ändringar: "tack vare" om något negativt, "förväntas" och "ska" om ett förslag rättade, procent och procentenheter åtskilda, mellanslag före %, vilket-kedjan delad. Kontrollera att "2 procentenheter" stämmer med källan, för originalet säger "2%".

---

## Källor vid tveksamhet

- **Språkrådets skrivregler** för stavning, skiljetecken, siffror och datum.
- **TT-språket** (tt-spraket.tt.se) för ordval, falska vänner, anglicismer och siffror i löptext. TT skriver nyhetsspråk, så ta inte över deras stilval ("sade", "procent" i stället för %) utan att pröva dem mot affärstext.
- **Språkbanken/Korp** för att se hur ofta en fras faktiskt används. Se avsnitt F.

---

## Slutkontroll

Gå igenom innan texten levereras:

1. Har jag lagt till något som inte fanns i källtexten? Ta bort det eller gör det till en hakparentes.
2. Finns det tankstreck som paus, komma före "och" i uppräkningar, engelska citattecken, "30%" utan mellanslag, ofullständiga intervall eller amerikanska datumformat?
3. Finns det "gällande", "erhålla", "tillhandahålla", "säkerställa", "teknologi" eller andra ord från A1 och A2?
4. Säger orden mer än källtexten menar? Kontrollera förväntas, tack vare, ska, procent och mindre enligt A4.
5. Finns det "inte X, utan Y", en iscensatt oneliner, ett tretal eller en generisk avslutning?
6. Läs texten högt i huvudet. Var stannar du upp eller låter det som ett pressmeddelande? Skriv om just där.
7. Varierar meningslängden? Om alla meningar är ungefär lika långa, slå ihop två eller korta en.
8. Vet läsaren vad som ska hända härnäst?
