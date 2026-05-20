# ServerHotel — executive summary k prototypu

## Veřejná ukázka

Veřejně posílám pouze funkční HTML prototyp:

- `serverhotel-landing-pyramida.html`

Interní MD podklady neposílám. Obsahují pracovní detaily, které by bylo potřeba anonymizovat a pro účel Aibility stačí bezpečný přehled níže.

## Co prototyp řeší

ServerHotel je diagnostický prototyp pro IT infrastrukturu. Není to jen formulář ani cenová kalkulačka. Cílem je převést technický chaos do rozhodovacího rámce, kterému rozumí obchod, zákazník i technický člověk.

Prototyp kombinuje:

- diagnostiku podle typu prostředí,
- sadu řízených otázek s adaptivní logikou,
- N/A větvení tam, kde otázka pro daný kontext nedává smysl,
- výstup do pětivrstvé pyramidy,
- obrazovkový report,
- gate pro detailnější výstup,
- konfigurátor služeb a parametrů jako navazující obchodní vrstvu.

## Co je připravené kolem launch vrstvy

Z interních podkladů je připravený bezpečný souhrn:

- doména `serverhotel.cz` a technický plán jejího spuštění,
- DNS plán pro web, ověřovací záznamy a e-mailovou autentizaci,
- měřicí vrstva přes GA4, GTM a GSC,
- konverzní logika pro odeslání diagnostiky,
- návrh e-mailového aliasu a neutralizované komunikace na doméně serverhotel.cz,
- transakční e-mailová vrstva pro potvrzení a notifikace,
- CRM návaznost pro práci s leady,
- SEO technická vrstva: metadata, sitemap, robots, strukturovaná data a obsahové landing pages,
- PPC architektura na úrovni kampaní, skupin, klíčových slov, negativních slov a textací,
- importní podklady pro testovací spuštění kampaní,
- základní compliance a provozní checklist: consent, privacy, HTTPS, zálohy, auditní stopa a role v provozu.

Záměrně tu nejsou rozpočty kampaní, účty, telefonní čísla, interní poznámky ani pracovní dokumenty pro klienta.

## Stav

Aktuálně jde o proof-of-concept. Finální produkční verze bude později kódovaná jinak, takže HTML prototyp je ukázka myšlení, struktury a funkční logiky, ne hotový produkční web.
