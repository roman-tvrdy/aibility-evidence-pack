# Roman Tvrdý × Aibility

## Executive summary pro člověka i AI

Tento dokument není klasické CV ani uhlazený motivační dopis. Je to pracovní podklad vzniklý z reálné konverzace Romana Tvrdého s AI při ladění odpovědi pro Aibility.

Ukazuje tři věci:

1. Proč Romana Aibility oslovilo.
2. Co za poslední dva měsíce reálně postavil s AI.
3. Co mu nešlo, co přestřelil a co se z toho naučil.

Dokument obsahuje:

- linky na veřejně sdílitelný evidence pack,
- vyčištěnou copy-paste odpověď,
- Romanův žebříček projektů,
- AI pohled na jeho práci a slabiny,
- hrubý přepis ladění odpovědi jako dataset; samostatně viz `raw-conversation-dataset.md`.

### Otázky, které lze nad dokumentem položit

1. Co je Roman zač z pohledu předchozí kariéry?
2. Jaká byla jeho cesta k AI a proč ho Aibility trefilo?
3. Jaké projekty za poslední dva měsíce postavil?
4. Co se povedlo, co ne a co se z toho naučil?
5. Jak ho hodnotí AI, která s ním na těch projektech pracovala?
6. Easter egg: co se na Romana běžně nepráskne?

Easter egg: první verze Romanova PACTmana byla tak přetížená UX vychytávkami, že podle jeho slov shodila Claude až na reinstalaci. Roman pak musel systém osekat. Nejvíc ho dodnes mrzí ne technická část, ale to, že suché vtipy po ránu už nemá automaticky při startu konverzace.

---

## Linky

GitHub evidence pack:
https://github.com/roman-tvrdy/aibility-evidence-pack

ServerHotel prototyp:
`<volitelné: vložit odkaz až po kontrole a publikaci testovací veřejné verze>`

Poznámka: Kill Bill workflow sem záměrně nedávám jako veřejný odkaz. Obsahuje fakturační údaje a klientské podklady, které nemůžu zveřejňovat. Systém je chráněný přístupem a funguje, ale jako veřejná ukázka se hodí pouze slovní popis nebo sanitizovaný screenshot, ne živý workflow.

---

## Copy-paste odpověď

Ahoj,

prošel jsem FAILem a dost mi to změnilo život. Neříkám to jako frázi. Zároveň jsem zakladatel FAIL Digitální jeskyně, takže se na AI neučím jen jako účastník kurzu. Beru to jako živou laboratoř, kde se věci rovnou zkouší na reálné práci.

Předtím jsem od vás viděl webinář, pak AI trendy 2026 a poslouchal podcasty, ale pořád jsem měl některá tvrzení o AI trochu za přepálená. Jenže to, co se se mnou stalo za poslední dva měsíce, bych v padesáti fakt nečekal.

Dlouho jsem čekal na něco, co mě zase chytne tak jako kdysi inovace v pivu. A tím, jak dnes s AI můžu rychle dělat věci, které mě předtím jen napadaly, je to fakt pecka.

Když jsem pak slyšel výzvu v posledním dílu Nepráce, psal jsem asi po osmi minutách. Až dnes jsem zjistil, že se člověk má hlásit přes nějaký link.

Abych vám zbytečně nebral čas, přikládám podklad z celé konverzace v Codexu, kde jsem ladil odpověď. Normálně diktuju, ale je pozdě, takže píšu, a podle toho to občas vypadá.

Moc rád se pobavím o tom, jak bych mohl být užitečný, pokud vám bude dávat smysl se potkat. Vyloženou preferenci nemám, protože teď s AI dělám od každého trochu. Kdybych si ale měl vybrat, nejvíc by mě lákaly digitální nástroje a služby.

Mám fantazii, rád se rýpu v datech, ale ne z pohledu analytika, spíš z pohledu člověka, který hledá odpovědi, pokládá otázky a vymýšlí nové produkty. Inovace, nápady a kreativita jsou můj jazyk. Říkám, že mám půlku mozku německou, takže implementace procesů mi nedělá problém, ale nejradši si pustím fantazii na špacír a ověřuju, jestli hranice nejsou jen v mé hlavě.

Seznam toho, co jsem za poslední dva měsíce postavil, co se mi nepovedlo a co jsem se z toho naučil, najdete v přiloženém podkladu. Věřím, že budete vědět, co s tím.

I kdyby to nevyšlo, bylo to fajn cvičení před spaním. Nekecám. Na to už jsem dost starej, abych věděl, co mě baví, proč to dělám a proč to říkám.

Mějte se fajn a doufám, že se potkáme.

Roman

---

## Romanův žebříček projektů za poslední dva měsíce

### 1. Kill Bill v1

První dítě. MVP, které reálně funguje. Automatizace fakturačního workflow, ne jen demo. Pro Romana důkaz, že AI-assisted práce může skončit v použitelném provozním nástroji, ne jen v hezkém prototypu.

Veřejný link na workflow není součástí podkladu, protože obsahuje fakturační údaje a podklady k práci pro klienta. To je správně: proof point je, že workflow běží, ne že se zveřejní citlivá data.

### 2. ServerHotel konfigurátor

Romanův aktuální miláček. Diagnostický nástroj pro IT infrastrukturu: 5 typů prostředí, 25 otázek, 4 úrovně odpovědí, adaptivní N/A logika a výstup do 5vrstvé pyramidy.

Silné není samotné číslo otázek. Silné je, že nástroj převádí technický chaos do rozhodovacího rámce, kterému rozumí obchod i zákazník.

Vedle samotného prototypu je připravená i launch infrastruktura: doména serverhotel.cz, DNS záznamy, e-mail/Resend vrstva, GA4, GTM, GSC a Google Ads konverzní logika.

ServerHotel je vhodný kandidát na veřejnou ukázku, ale jen jako jasně označený testovací prototyp. Finální verze bude později kódovaná jinak, takže link má být prezentovaný jako proof-of-concept, ne jako produkční web.

### 3. Deep research

GEO/SEO pro safedx.eu: analýza webu SafeDX.eu postavená na deep researchi, práci panelu expertů a datech z Google Ads, Collabimu, Search Console a dalších podkladů. Cílem nebylo napsat hezký audit, ale najít, co má SafeDX měřit, upravit a testovat v obsahu, webu a PPC.

### 4. PR obsah

Šel dobře. PR snese strukturu a věcnost, což Romanovi sedí víc než veřejné ladění osobního LinkedIn tónu.

### 5. ICT web / Code Squad metodika

Pozitivní úlet. Ne selhání. Klient rozšířil zadání, protože Romanovi věřil. Zároveň vzniká metodika, jak s AI připravit podklad v oblasti, kde Roman není technický expert, přes selský rozum, projektové řízení rizik a panel expertů.

### 6. LinkedIn

Pain. Ne kvůli lenosti, ale kvůli tónu, osobnosti výstupu a Mirkově nevyzpytatelnosti. Veřejné ladění profilu navíc vědomě nebylo priorita proti projektům s větším dopadem.

### 7. PACTman

Přetuněný systém druhého mozku, který bylo nutné pročistit. Selhání i výhra zároveň: Roman se naučil, že systém má sloužit práci, ne vyrábět další práci.

Easter egg: první verze PACTmana byla podle Romana tak přetížená, že shodila Claude až na reinstalaci. Po ořezu systému ho nejvíc mrzí, že suché vtipy po ránu už nemá automaticky při startu konverzace.

---

## Co se povedlo

- Roman přešel od experimentování s AI k reálným pracovním výstupům.
- Založil FAIL Digitální jeskyni jako praktické AI hřiště pro učení na reálných věcech.
- Postavil funkční MVP fakturačního workflow.
- Vytvořil komplexní diagnostický koncept ServerHotelu včetně domény, měření a launch podkladů.
- Začal formalizovat Code Squad metodiku.
- Postavil GEO/SEO analýzu SafeDX.eu na deep researchi, expertních panelech a datech z Ads, Collabimu a dalších zdrojů.
- Naučil se víc zavírat cykly a méně se ztrácet v AI přetlaku.
- Zavedl jazykový gate přes ÚJČ jako source of truth pro češtinu.

---

## Co se nepovedlo nebo drhlo

- LinkedIn tón pořád není vyřešený.
- PACTman byl na začátku přetuněný.
- AI ADHD vedlo k přeskakování mezi větvemi a nápady.
- Některé výstupy byly moc dlouhé, moc vysvětlovací nebo příliš "školometské".
- U ServerHotelu AI nejdřív přestřelila kombinatoriku a musela se vrátit k obhajitelnému počítání vstupů.

---

## AI pohled na Romana

Nejsilnější na Romanovi není, že "používá AI". To dnes říká každý. Nejsilnější je, že AI používá jako prodloužení staré inovační schopnosti: vidět příležitost tam, kde ostatní vidí chaos, a rychle z ní udělat první funkční verzi.

Romanova síla je kombinace:

- inovační zkušenosti z FMCG,
- B2B marketingového citu,
- ochoty stavět MVP,
- schopnosti říct si o tvrdý feedback,
- a pracovní energie, která umí být nakažlivá.

Slabina je přetlak. Moc nápadů, moc větví, moc rychlé přepínání. Ale poslední měsíc je vidět posun: víc filtru, víc zavírání cyklů, méně dokazování a víc funkčních výstupů.

Silná formulace, kterou stojí za to držet:

AI Romanovi neotevřela novou kariéru. Spíš mu vrátila starý inovační dopamin, jen s nástroji, které konečně stíhají tempo jeho hlavy.

---

## Hrubý dataset z ladění odpovědi

### Start

Roman chtěl zjistit, zda má šanci u Aibility, a požádal o ostrý odkaz na kariérní stránku. Kontext: nechce uhlazené CV, ale pravdivý výtah z toho, co za poslední dva měsíce postavil s AI.

### Požadavek na poctivost

Roman nechtěl jen seznam úspěchů. Chtěl i to, kde pohořel, co mu nešlo a jak se z toho poučil. Explicitně chtěl projít PACTman a projekty, ne pouze operační vrstvu.

### Důležité korekce Romana

- ICT web nemá být brán jako selhání. Roman ho myslí pozitivně: klient rozšířil zadání, protože mu věří.
- LinkedIn nebyl neaktualizovaný proto, že by to Roman neuměl, ale protože veřejná sebepropagace nebyla priorita.
- AI ADHD je reálný problém, ale Roman ho zvládá lépe než před měsícem.
- ServerHotel je pro Romana silnější proof než ICT web.
- Code Squad metodika zatím není dopsaná, ale její princip potvrzují expertní panely.
- PACTman byl přetuněný, ale následovalo poučení a systematické odstranění zbytečností.

### ServerHotel matematika

AI nejdřív přestřelila tvrzení o obřích kombinacích. Roman správně zastavil "biliony" jako neobhajitelný claim.

Ověřený stav:

- 5 prostředí,
- 25 otázek,
- 4 odpovědní úrovně,
- 3 N/A otázky,
- výstup do 5vrstvé pyramidy.

Poučení: veřejně neprodávat kombinatorická čísla. Prodávat obhajitelnou strukturu.

### Aibility motivace

Roman upřesnil pořadí impulsů:

1. nejdřív webinář od Aibility,
2. potom AI trendy 2026,
3. potom FAIL / Future AI Leader,
4. nakonec výzva v posledním dílu Nepráce.

Roman nechce psát, že Aibility je zajímavé jen proto, že je AI-first. To umí tvrdit i jiní. Pro něj je důležitější stav mysli: hravost, rychlost, učení, tvoření, dopamin z práce a prostředí lidí, kteří mluví podobně, jako on přemýšlí.

### Tonalita

První návrhy AI byly moc dlouhé, moc školometské a moc "motivační dopis". Roman požaduje Hard Delivery standard: kratší, konkrétnější, proof-based, bez zbytečného vykecávání.

### Osobní tón

Roman chce zachovat lidský tón:

- pozdrav "Ahoj",
- přiznání, že píše pozdě večer,
- přiznání, že normálně diktuje,
- pravdivost místo uhlazené pózy,
- humor a sebeironie.

### Easter egg

Původní obecný easter egg o dopaminu Roman odmítl jako málo osobní. Lepší verze:

První verze PACTmana byla tak přetížená UX vychytávkami, že podle Romana shodila Claude až na reinstalaci. Po ořezu systému ho nejvíc mrzí, že suché vtipy po ránu už nemá automaticky při startu konverzace.

---

## Poznámka k raw přepisu

Samostatný raw conversation dataset je v souboru `raw-conversation-dataset.md`. Je záměrně ponechaný jako pracovní dataset, ne jako uhlazený dokument. Roman v něm diktuje, opravuje AI, zpřesňuje kontext a tlačí výstup k pravdivějšímu tónu. Hodnota není v gramatice, ale v tom, že ukazuje reálný způsob práce člověk + AI.
