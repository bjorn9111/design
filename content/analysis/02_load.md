---
Title: Load
Description: This is my load page.
Template: analysis
---

Laddningstid
=======================

I denna analys skall tre webbplatser jämföras. Fokus ligger på laddningstid, användbarhet och förbättringspotential.

Urval
-----------------------
Urvalet är detsamma som i andra analyser. Jag kollar på intressanta, framgångsrika och förhoppningsvis väldesignade personliga bloggar i mina analyser. För utförligare svar se urval i artikeln som behandlar färgteori.

De tre webbplatserna är följande:

1. [James Clear] [2], författaren bakom bästsäljaren 'Atomic Habits'.
2. [Dana Shultz] [3], minimalist baker. Skapar vegetariska recept med få ingredienser som går snabbt att laga.
3. [Gala Darling] [4], en självhjälp blogg med tapping inriktad mot kvinnor.

Metod
-----------------------

I denna analys används devtools samt '[PageSpeed Insights] [1]' för att beräkna betyg och laddningstider.

Resultat
-----------------------

### Rådata

<div class="embed-container">
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQ_yF8WpA-WAJI4pu4Ynz5A0x3uG7Qv5lfmyOOJCSKrmY-hRBu6vxfp4YvhQv61sjjYkn5tkE0DNZTU/pubhtml?widget=true&amp;headers=false" frameborder="0" allowfullscreen></iframe>
</div>

### James Clear blog

![Screenshot of James Clear homepage](%assets_url%/img/James_Clear.png "Screenshot of James Clear homepage") {.center}

Bra betyg med dator, 95 av 100 i snitt, medan mobil enhet ser något större förbättringspotential då betyget blir 84 av 100 i snitt. 

### Dana Shultz mat blog

![Screenshot of Dana Shultz homepage](%assets_url%/img/minimalist_baker.png "Screenshot of Dana Shultz homepage") {.center}

Låga betyg i framförallt prestanda (betyg 31/64) och bästa metoder (betyg 57/56) för både mobila och desktop enheter. 

### Gala Darling självhjälp blog för kvinnor

![Screenshot of Gala Darling homepage](%assets_url%/img/Gala_Darling.png "Screenshot of Gala Darling homepage") {.center}

SEO('search engine optimization') har stora förbättringsmöjligheter på alla enheter (betyg 69), samt prestanda på mobila enheter (betyg 39).

Analys
-----------------------

### PageSpeed analys

Dana Shultz tycks prioritera SEO med ett betyg på 100 trots lägst snittbetyg överlag bland de tre jämförda webbplatserna (betyg 68.5/76.75). Det är framför allt dålig prestanda och bästa metoder som drar ner genomsnittsbetyget. Hög körningstid att tolka och kompilera JS-kod, tredjepartscookies samt användandet av ett gammalt API (vars stöd gick ut dec 2018) är några av de större bovarna.

Gala Darling knep andraplats sett till genomsnittsbetyg (72.25/83). Layoutförskjutningar, resurser som blockerar rendering och långsam tid att rita upp element med störst innehåll (LCP) ledde till lågt betyg inom prestanda för mobila enheter. Ingen metabeskrivning i dokumentet, bristande beskrivande texter för länkar och för få alt-attribut på bildelement leder till dålig SOP på alla enheter.

Första plats går till James Clear vars blog når snittbetygen 84 och 95. Prestanda på mobila enheter hade störst förbättringspotential. Mer moderna bildformat (WebP och AVIF), långsam LCP och JS körningstid är de viktigaste faktorerna till det lägre betyget här.

### Devtools analys

James Clear har lägst DOM laddningstid, 0.34 sekunder medan de andra webbplatserna ligger runt eller strax över 1 sekund. På grund av blockerande resurser på James Clear blir 'Devtool Load' klart högre, 5.54 sekunder i snitt. Detta händer endast på startsidan, inte övriga flikar, och diverse JS filer samt fetch API är ansvariga för detta. Gala Darling var bäst med 1.45 sekunder laddningstid. medan Dana Shultz hamnar i mitten, 3.27 sekunder. Total tid för då HTML + blockerande (CSS, JS) + icke blockerande (async JS) resurser har laddats ner blev oändlig i webbplatsen Dana Shultz eftersom den har en loop som letar efter uppdateringar. Övriga webbplatser hade runt 6 sekunder total laddningstid. James Clear skickar information till google analytics med beacon API vilket tycks vara den begränsande faktorn till detta. 

Godkänd laddningstid kan ses som 3 sekunder, då mer än detta kan leda till att användare lämnar, se [Sematext] [5]. Här klarar sig endast Gala Darling. Viktigt att notera är dock att laddningstiden är runt 1.5 sekunder på testade flikar i James Deans blogg. Dana Shultz har hög variation på laddningstiderna. Vissa recept tar över 15 sekunder, medan andra flikar kan ladda på under 2 sekunder. Dana Shultz känns långsam ibland, särskilt då bilderna är många. Både James Clear och Gala Darling känns snabba. Detta stämmer väl med den prestanda som mäts i PageSpeed analysen. Notera att jag besökt webbplaserna via desktop.

Referenser
-----------------------

1. [James Clear (2024)] [2]. *An Easy & Proven Way to Build Good Habits & Break Bad Ones*. [https://bloggerspassion.com/popular-personal-blogs/] [2] [2024-05-15]
2. [Dana Shultz (2024)] [3]. *Minimalist Baker*. [https://minimalistbaker.com/] [3] [2024-05-15]
3. [Gala Darling (2024)] [4]. *Gala Darling.* [https://galadarling.com/] [4] [2024-05-15]

Övrigt
-----------------------

Skriven av Björn Horndahl.

[1]: https://pagespeed.web.dev/ "PageSpeed Insights"
[2]: https://jamesclear.com/ "Build Good Habits & Break Bad Ones"
[3]: https://minimalistbaker.com/ "Minimalist Baker"
[4]: https://galadarling.com/ "Self proclaimed professional optimist"
[5]: https://sematext.com/glossary/page-load-time/ "Sematext"
