# Code Squad delivery model — anonymizovaný podklad

> Tento dokument je anonymizovaná verze interního delivery modelu. Neobsahuje osobní jména, názvy firem, klientský kontext ani odkaz na konkrétní repozitář. Cílem je ukázat metodiku práce, ne zveřejnit klientské nebo interní informace.

## 1. Executive Summary

Code Squad je lehký, ale auditovatelný delivery model pro AI-assisted dodávku webového nebo digitálního projektu.

Vychází z jednoduchého principu: AI může výrazně zrychlit přípravu zadání, dokumentaci, implementaci, review i testování, ale nesmí nahradit odpovědnost, klasifikaci rizik, security gate, sign-off ani auditní stopu.

Proces proto nestaví na modelu „nejdřív něco vygeneruj a potom zjisti, jestli to bylo bezpečné“. Nejprve se ověří scope, data, integrace, rizika a schvalovací brány. Teprve potom začíná implementace.

Základní tok:

`zadání -> intake -> klasifikace -> AI/data/security kontrola -> implementace -> lint -> build -> review -> vypořádání -> sign-off -> release evidence`

## 2. K čemu je model určený

Model je vhodný pro situace, kdy se AI používá jako pracovní multiplikátor při dodávce digitálního výstupu, ale projekt musí zůstat:

- kontrolovatelný,
- auditovatelný,
- bezpečný,
- vysvětlitelný vůči klientovi nebo internímu stakeholderovi,
- připravený na technické a compliance review.

Ty*****ký use case:

- interní informační web,
- portál nebo microsite,
- klientský web s formuláři,
- obsahově-technický web s více stakeholdery,
- projekt, kde AI pomáhá s dodávkou, ale cílový produkt sám nemusí mít AI funkcionalitu.

## 3. Z čeho metodika vychází

Code Squad není jedna těžká enterprise metodika. Je to praktický průnik několika principů:

| Oblast | Jak se používá |
|---|---|
| Secure SDLC | bezpečnost, review a evidence jsou součást procesu, ne dodatečná kontrola na konci |
| DevSecOps | technická kontrola a bezpečnostní pravidla běží v delivery toku |
| Change Enablement | změna má vlastníka, scope, rozhodnutí a release evidence |
| Pull request workflow | změna je auditovatelná jednotka práce |
| Required checks | merge až po splnění povinných kontrol |
| Product gate | funkční výstup nestačí; kontroluje se UX, důvěra, srozumitelnost a hlavní workflow |
| AI/data governance | odděluje se AI-assisted delivery od AI funkcionality v produktu |

Záměr je jednoduchý: rychlost ano, zkratky přes bezpečnost a odpovědnost ne.

## 4. Připravenost před buildem

Před implementací musí být připravené minimálně:

- project brief,
- feature brief,
- change intake,
- AI/data classification,
- risk classification,
- PR checklist,
- self-review šablona,
- findings report,
- release evidence šablona,
- rollback note,
- open findings tracker,
- seznam required checks,
- popis review režimu,
- procesní mapa delivery toku.

Bez těchto podkladů se implementace nemá rozbíhat, protože by AI pracovala bez hranic.

## 5. Role a odpovědnosti

| Role | Odpovědnost |
|---|---|
| Sponsor | mandát, eskalace, zásadní scope, reputační a obchodní dopad |
| Product Owner | business cíl, priorita, hodnota, product go/no-go, koordinace vstupů |
| Obsahový vlastník | upřesnění obsahu, validace věcné správnosti a pilotní oblasti |
| Code Squad | delivery proces, dokumentace, evidence, implementace, review orchestrace |
| AI Primary Builder | implementace, testy, self-review, zapracování nálezů |
| Fresh AI Review | oddělený druhý pohled bez implementačního tunelu |
| Independent Reviewer | nezávislé technické review proti stejnému review package |
| Expert Panel | security, data/AI, backend/integrace, frontend/UX, release, code quality |
| AI Compliance / Technology Advisor | sanity check AI, data, compliance a technické logiky modelu |
| Formal Governance Gate | validační nebo eskalační cesta pro AI-relevantní změny s vyšším rizikem |

## 6. Procesní mapa

```text
01 PROJECT INTENT
   business cíl, kontext, proč to děláme
   |
   v
02 WORK PACKAGE
   proveditelná část práce, jasný scope, mimo rozsah
   |
   v
03 FEATURE BRIEF
   acceptance kritéria, závislosti, rizika, testy
   |
   v
04 CHANGE INTAKE + AI / DATA CLASSIFICATION
   co smí do AI, co smí do repozitáře, co je citlivé, co vyžaduje gate
   |
   v
05 AI / DATA / SECURITY CONTROL
   kontrola před implementací, zakázaná data, governance/security review podle rizika
   |
   v
06 RISK CLASSIFICATION
   low / medium / high / critical
   |
   +----------------------+
   |                      |
   v                      v
LOW / MEDIUM           HIGH / CRITICAL
self-review            povinný expert panel
independent review     security/data/UX/devops/code quality
   |                      |
   +----------+-----------+
              |
              v
07 BRANCH + PR
   samostatná větev, žádný direct commit do main
              |
              v
08 IMPLEMENTATION
   AI Primary Builder
              |
              v
09 LINT + STATIC CHECKS
   lint, typecheck, secret scan, dependency/security check
              |
              v
10 BUILD + PREVIEW CHECK
   build až po lintu, preview, smoke check
              |
              v
11 SELF-REVIEW
   builder popíše co změnil, proč, jak ověřil, co je rizikové
              |
              v
12 FRESH AI REVIEW
   oddělený AI review pohled
              |
              v
13 INDEPENDENT REVIEW
   nezávislý reviewer proti review package
              |
              v
14 FINDINGS REPORT
   blocker / high / medium / low / note
              |
              v
15 CHANGE INTAKE
   každý nález má stav, vlastníka, rozhodnutí a rationale
              |
              v
16 REMEDIATION
   schválené nálezy se zapracují
              |
              v
17 RE-CHECK
   kontroly a cílené review vypořádání
              |
              v
18 SIGN-OFF
   product / technical / security / sponsor podle dopadu
              |
              v
19 MERGE / DEPLOY
   jen po zelených kontrolách a explicitním go
              |
              v
20 RELEASE EVIDENCE
   co se změnilo, proč, kdo reviewoval, nálezy, rollback, open findings
```

Stop pravidlo je jednoduché: pokud chybí brief, klasifikace, kontrola, review, vypořádání blockeru nebo sign-off, změna nejde dál.

## 7. Kde se proces zastaví

| Situace | Reakce |
|---|---|
| Nejasný business cíl | vrátit k Product Ownerovi |
| Nejasný scope | nevytvářet implementaci |
| Chybí acceptance kritéria | zastavit před buildem |
| Chybí AI/data/security klasifikace | stop před implementací |
| Chybí kontrola před implementací | stop před implementací |
| Citlivá data bez schválení | stop |
| Direct commit do main | zakázáno |
| Lint neprošel nebo neběžel | build se nespouští |
| Failing required check | stop |
| Chybí self-review | stop |
| Blocker/high nález | vypořádat před merge/deploy |
| Security/data nález | stop; další postup přes určený gate nebo expert panel |
| Chybí sign-off | žádný merge/deploy |
| Chybí release evidence | release není dokončený |
| Dočasné env proměnné jako cílový provozní režim | nepřijmout; pouze dočasná nebo nouzová review varianta |

## 8. Expert Panel

Expert panel se nespouští až na lidskou otázku „prohnali jste to panelem?“. Aktivuje ho risk classification.

Povinný je při:

- auth / role / oprávnění,
- formulářích nebo ukládání dat,
- AI / model disclosure,
- AI funkcionalitě přímo v produktu,
- AI-assisted nebo AI-generated obsahu, pokud může ovlivnit uživatele nebo rozhodování,
- potřebě formální AI governance validace,
- CRM, analytics nebo integracích,
- produkčním deploymentu,
- secrets nebo env konfiguraci,
- zásadním UX workflow,
- high/critical security nálezu,
- provozně kritické logice.

Panel vrací pouze:

- PASS,
- PASS WITH REQUIRED CHANGES,
- FAIL,
- DEFER WITH OWNER AND DEADLINE.

FAIL není komentář. FAIL znamená, že změna nesmí pokračovat do merge/deploy, dokud není přepracovaná a znovu předložená ke kontrole.

## 9. AI-assisted Delivery vs. AI Funkcionalita

Code Squad rozlišuje dvě různé věci:

1. **AI-assisted delivery** — použití AI nástrojů při přípravě zadání, dokumentace, implementace, review a testování.
2. **AI funkcionalita v produktu** — jakákoliv funkce, která by AI používala přímo v provozu pro koncového uživatele.

Tento model řeší primárně AI-assisted delivery. Pokud se později objeví požadavek na AI funkcionalitu přímo v produktu, musí projít samostatným intake, AI/data/security klasifikací, posouzením pravidel a podle rizika formálním governance gate.

## 10. AI/Data Pravidla

AI/data režim se neřídí tím, zda data patří jedné nebo druhé firmě. Primární je datová klasifikace, schválený způsob zpracování a kontext použití.

Bez samostatného schválení nesmí do AI workflow vstupovat:

- osobní údaje,
- mzdy,
- finanční plány,
- citlivé bezpečnostní informace,
- secrets, přístupové údaje, tokeny a konfigurační hodnoty,
- interní technické detaily, které nejsou určené pro sdílení mimo schválený režim,
- další data podle existujících směrnic nebo dohody.

AI-assisted nebo AI-generated obsah se označuje tam, kde je to relevantní pro transparentnost, review nebo uživatelskou důvěru. AI review nenahrazuje lidský dohled u kritických, citlivých nebo provozně dopadových změn.

## 11. Repo, Preview, Review Data

| Nástrojová oblast | Role v procesu | Stav v anonymizované verzi |
|---|---|---|
| Version control | primární repozitář, PR, issues/change intake, auditní stopa | konkrétní odkaz odstraněn |
| Preview hosting | volitelná preview/review vrstva pro online komentování | neidentifikováno |
| Review data store | strukturované komentáře nebo review data u složitějšího review | neidentifikováno |

Každý projekt má vlastní repozitář nebo samostatný workspace. Nemíchá se s jinými projekty.

Auth, formuláře, CRM, analytics, interní AI/search integrace a další napojení nejsou v tomto modelu „automaticky schválené“. Každá taková oblast jde do samostatného intake, protože mění datový, bezpečnostní nebo provozní profil projektu.

## 12. Ochrana Budoucího Online Review Linku

Pokud bude použit online review link, minimální ochranný režim je:

```text
review link
   |
   v
simple passcode gate
   |
   v
review content
```

Prakticky:

- review portal před zobrazením obsahu zobrazí krátkou vstupní obrazovku,
- reviewer zadá předem domluvený passcode nebo odpověď na kontrolní otázku,
- passcode se neukládá do repozitáře,
- hodnota může být dočasně v env proměnné, pokud je takový review režim schválený,
- po správné odpovědi se nastaví session/cookie a obsah se zobrazí.

Toto není enterprise access management a není to určené pro citlivá data. Je to rychlá bariéra proti náhodnému otevření linku někým, kdo se k němu dostane omylem. Pro review bez secrets, osobních údajů a citlivých technických detailů je to přiměřená první úroveň ochrany.

## 13. Otázky Pro Review

1. Je tento Code Squad delivery model akceptovatelný pro projekt tohoto typu?
2. Chybí v něm povinný gate z pohledu compliance, security nebo provozu?
3. Jsou role a odpovědnosti nastavené realisticky?
4. Je oddělení implementace, fresh review a independent review dostatečné?
5. Je expert panel spouštěný správně podle rizika?
6. Jsou AI/data pravidla dostatečná pro práci před buildem?
7. Existují interní pravidla pro AI nástroje, modely, providery, data handling nebo disclosure, která se musí zohlednit?
8. Mají auth, formuláře, CRM, analytics a další integrace projít samostatným intake?
9. Je formální AI governance gate správně nastavený jako defaultní eskalační možnost pro AI-relevantní změny s vyšším rizikem?
10. Kdo má být finální technický sign-off vlastník u high-risk změn?
11. Co by před buildem bylo červenou vlajkou?

## 14. Zapracované Principy Z Review

Tato verze zapracovává poznámky z předchozího technického a compliance review:

| Vstup | Zapracování |
|---|---|
| Oddělit AI-assisted delivery od AI funkcionality v produktu | doplněno v modelu i gate logice |
| AI/data režim řídit podle datové klasifikace | doplněno do procesu před implementací |
| Zakázaná data bez schválení | doplněno v AI/data pravidlech |
| AI review nenahrazuje lidský dohled | doplněno v AI/data pravidlech |
| Formální governance gate pro vyšší AI riziko | doplněno v rolích, expert panelu a otázkách k potvrzení |
| Integrace řešit samostatným intake | doplněno v části repo/preview/review data |
| Klasifikace a kontrola před implementací | přepsaná procesní mapa |
| Lint před buildem | doplněno do procesní mapy a stop pravidel |
| Security nález = stop | doplněno do stop pravidel |
| Expert panel může vrátit FAIL | doplněno do expert panelu |
| Env proměnné nejsou cílový provozní režim | doplněno do stop pravidel a ochrany review linku |

## 15. Pointa

Code Squad je způsob, jak stavět rychle s AI, ale bez iluze, že rychlost sama o sobě stačí.

Nejdůležitější přínos není v tom, že AI „umí napsat kód“. Přínos je v tom, že AI pomůže rychle připravit zadání, varianty, dokumentaci, review package a implementaci, zatímco člověk drží scope, odpovědnost, risk gate a rozhodnutí.

Tohle je praktická metodika pro situace, kde se nechce čekat měsíce na perfektní plán, ale zároveň není přijatelné pálit změny do produkce bez kontroly.
