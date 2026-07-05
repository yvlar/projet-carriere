# Portfolio détaillé — référence pour la recherche d'emploi

> **À quoi sert ce fichier**
> C'est la **source de vérité factuelle** sur le profil et les projets d'Yves Larivière, destinée à un assistant IA (Claude) qui l'aide à postuler : rédiger une lettre, remplir un champ de CV, préparer une entrevue, choisir quel projet mettre en avant.
>
> **Règle d'or** : ne jamais affirmer au-delà de ce qui est écrit ici. Tous les chiffres proviennent de mesures réelles sur les dépôts (commandes de comptage, juillet 2026). Les garde-fous en fin de document listent ce qu'il ne faut **pas** prétendre. En cas de doute sur un fait absent d'ici : le reformuler en « à vérifier », jamais l'inventer.

---

## 1. Profil candidat

| | |
|---|---|
| **Nom** | Yves Larivière |
| **Lieu** | Drummondville (Québec) · permis de conduire + voiture |
| **Contact** | ivess49@gmail.com · github.com/yvlar |
| **Objectif** | Premier emploi de développeur logiciel junior **ou** programmeur en automatisation, région Drummondville / Trois-Rivières (Sherbrooke acceptable), ~30 $/h, dès maintenant |

**Titre de profil canonique** (à utiliser partout — Indeed, LinkedIn, lettres) :
> Développeur logiciel junior — C++ / Python / SQL · Certificat en informatique (génie logiciel), Université Laval · 10 ans d'expérience manufacturière

**Pitch 30 secondes** :
> 10 ans chez ContiTech (responsable de secteur puis formateur) — coordination d'équipes, qualité, formation, liaison plancher-ingénierie, utilisateur quotidien de SAP. En parallèle : certificat en informatique (génie logiciel) de l'Université Laval **complété**, et 3 projets logiciels complets livrés et publics (70 000+ lignes, 3 500+ tests automatisés). Objectif : **automatiser, outiller et fiabiliser la production avec du logiciel**.

**Positionnement** : « le développeur qui connaît le plancher d'usine » — rare des deux côtés (les juniors sortis d'école n'ont jamais vu une ligne de production ; les gens de plancher n'ont ni diplôme info ni portfolio).

**Trois voies** :
1. **Développement logiciel junior** — valorise le certificat + le portfolio (SwingBot en C++ est l'argument massue).
2. **Programmeur en automatisation** — valorise les 10 ans d'usine ; automates (Allen-Bradley/Siemens/Omron) à apprendre, procédés/terrain déjà acquis.
3. **ERP / SAP (moyen terme, 3-5 ans)** — utilisateur SAP quotidien + compétences de programmation → analyste fonctionnel ; pas de marché junior, ne pas payer de certification maintenant.

**Formation** :
- Certificat en informatique (génie logiciel), **Université Laval — obtenu**.
- DEC, Cégep de Drummondville.
- (En cours : certificat en finance quantitative — à confirmer l'établissement et la date avant de l'inscrire au CV comme fait.)

---

## 2. Matrice de compétences

**Langages** : C++ (C++17), Python, TypeScript, Java, SQL, C#, PHP, HTML5
**Frontend** : React 18 / React 19, Next.js 15 (App Router), Tailwind CSS, shadcn/ui, recharts, TanStack Query *(TradingClaude uniquement — voir garde-fous)*
**Backend** : FastAPI, Celery, asyncpg, Pydantic v2, Boost.Beast (C++)
**Données** : PostgreSQL, SQLite, Redis, Qdrant (vectoriel), Supabase (Postgres + RLS)
**Infra / outils** : Docker, Docker Compose, Git, GitHub Actions (CI), Linux, CMake, vcpkg, Ninja, Alembic, Vitest, GoogleTest, pytest, Playwright, Biome, Ruff, mypy
**Transférables (usine)** : SAP (utilisateur quotidien, contexte manufacturier), formation d'employés / vulgarisation, coordination d'équipes en horaire rotatif, contrôle qualité, résolution de problèmes, liaison plancher-ingénierie

---

## 3. Les projets

### 3.1 SwingBot — bot de trading algorithmique C++17
**Dépôt** : github.com/yvlar/swingtradebot · local : `/home/user/swingtradebot`
**Une ligne** : bot de swing-trading pour QQQ (stratégie EMA/RSI), avec backtester, validation quantitative, intégrations broker et dashboard temps réel.

**Faits mesurés** :
- ~14 000 lignes de C++17 (76 fichiers source/headers, hors build)
- **460 tests GoogleTest** (397 unitaires + 63 d'intégration), ~1 300 assertions
- Architecture quasi entièrement **header-only** (un seul `.cpp` compilé)
- 25 commits (mars → juillet 2026)

**Stack** : C++17, GoogleTest, Boost.Beast/Asio, nlohmann-json, SQLite3, libcurl, CMake + vcpkg (fallback paquets système), Ninja, Docker (3 Dockerfiles + compose), GitHub Actions.

**Notions / concepts démontrés** :
- **Architecture par interfaces + injection de dépendances** : 7 interfaces virtuelles pures (`IBroker`, `IDataFeed`, `IStrategy`, `IRiskManager`, `ILogger`, `IIndicator<T>`, `IStateStore`) — orchestrateur qui ne dépend que des abstractions, implémentations injectées.
- **Testabilité par conception** : mocks écrits à la main (aucun gmock), un processus par test, timeouts stricts, isolation totale.
- **Type `Result<T>` maison** pour la gestion d'erreurs sans exceptions.
- **Backtester** avec rapport complet : Max Drawdown, **Sharpe, Sortino, Calmar, CAGR**, Win Rate, Profit Factor, Expectancy, vs Buy & Hold.
- **Validation quantitative** : walk-forward, optimisation par grille (`GridOptimizer`), simulations Monte-Carlo.
- **Multithreading thread-safe** (`std::thread`/`std::atomic`/`mutex`/`condition_variable`) sur 11 modules.
- **Intégrations REST** : 3 brokers (Interactive Brokers, Alpaca, Paper) derrière une interface commune ; data feeds IBKR/Alpaca/CSV.
- **Persistance SQLite** (prepared statements), **dashboard WebSocket** (Boost.Beast asynchrone), **watchdog** de détection de freeze avec alertes email SMTP + webhook Discord/Slack.
- **CI GitHub Actions** : build Ninja + ctest sur chaque push/PR.

**Phrases CV prêtes** :
- « Bot de trading C++17 (~14 000 lignes), architecture header-only autour de 7 interfaces abstraites (injection de dépendances). »
- « 460 tests GoogleTest (unitaires + intégration, ~1 300 assertions), mocks manuels, chaque test isolé dans son processus. »
- « Backtester : Sharpe, Sortino, Calmar, drawdown, win rate ; validation walk-forward + Monte-Carlo. »

**Le plus fort pour** : postes **C/C++** (Infinition), embarqué/systèmes, fintech/trading (moyen terme).

---

### 3.2 TradingClaude — plateforme d'analyse financière IA
**Dépôt** : github.com/yvlar/TRADINGCLAUDE · local : `/home/user/TRADINGCLAUDE`
**Une ligne** : plateforme SaaS multi-tenant d'analyse fondamentale d'actions, 16 cadres d'analyse orchestrés par workflows, backend FastAPI + frontend React.

**Faits mesurés** :
- ~44 500 lignes (~23 000 Python backend + ~21 000 TypeScript frontend)
- **~2 250 tests pytest** backend + **531 tests Vitest** frontend + tests **e2e Playwright** (59) + evals LLM (38)
- 74 endpoints REST (26 routers), 16 skills tier2 + 1 tier1, 12 migrations Alembic

**Stack** : Python 3.11, FastAPI, Pydantic v2, asyncpg, Celery, PostgreSQL 16, Redis, Qdrant (RAG vectoriel), Anthropic SDK, Langfuse ; React 18 + TypeScript strict, Vite, Tailwind + shadcn/ui, recharts, TanStack Query, react-router ; Docker Compose (5 services), GitHub Actions (6 jobs), Ruff, mypy.

**Notions / concepts démontrés** :
- **Architecture orientée services** : orchestrateur multi-workflows, contrat commun `SkillBase`, 16 modules d'analyse composables.
- **API REST** : 74 endpoints, versionnés, documentés.
- **Sécurité applicative** : 4 middlewares — auth JWT (cookie), CSRF (double-submit), rate-limiting Redis, isolation multi-tenant.
- **Traitement asynchrone** : Celery/Redis (11 tâches worker), tout l'I/O en async/await.
- **RAG vectoriel** : Qdrant + embeddings pour recherche sémantique.
- **Observabilité** : Langfuse sur les appels LLM.
- **Base de données** : PostgreSQL avec migrations Alembic versionnées, RLS multi-tenant.
- **Pyramide de tests complète** : unitaires → services → API → e2e Playwright → evals LLM (pratique rare pour un junior).
- **CI multi-jobs** : test backend, test frontend, lint, typage, sécurité, migrations.
- **Frontend typé strict** : 15 pages, react-query, recharts, command palette.

**Phrases CV prêtes** :
- « Plateforme full-stack multi-tenant (~44 500 lignes) : FastAPI (74 endpoints), PostgreSQL, Redis/Celery, RAG Qdrant, React 18/TypeScript strict. »
- « ~2 250 tests pytest + 531 Vitest + e2e Playwright ; CI GitHub Actions à 6 jobs. »
- « Sécurité : JWT, CSRF, rate-limiting Redis, isolation multi-tenant. »

**Le plus fort pour** : postes **full-stack**, Python, backend, **avec composante IA** (Sogesco mentionne l'intérêt IA), fintech.

---

### 3.3 GRANDFORD — PWA d'horaires pour travailleurs d'usine
**Dépôt** : github.com/yvlar/GRANDFORD · local : `/home/user/GRANDFORD`
**Une ligne** : application web progressive (Next.js/Supabase) pour travailleurs d'usine en rotation 12 h (cycle Pitman 2-2-3), avec moteur d'horaire déterministe et confidentialité multi-tenant.

**Faits mesurés** :
- ~15 900 lignes de TypeScript strict (128 fichiers, zéro `any`)
- **~340 tests Vitest** (28 fichiers) dont **~130 tests d'isolation RLS** exécutés contre un vrai Postgres
- 19 tables, **RLS activée sur les 19** (46 policies), 19 migrations SQL, 3 Edge Functions Deno
- Version 0.30.0, 30 sprints, 80 commits

**Stack** : Next.js 15 (App Router), React 19, TypeScript strict, Supabase (Postgres + Auth + RLS + Edge Functions + Realtime), Serwist (PWA), Web Push (VAPID), Zod, Tailwind + shadcn/ui, Sentry, Vitest, Biome, pnpm.

**Notions / concepts démontrés** :
- **Moteur déterministe pur** : fonctions sans I/O, la date est un paramètre, calcul à la volée par modulo mathématique — tourne identiquement client et serveur, testable en isolation.
- **Golden tests + tests de propriétés** : faits calendaires réels encodés (7 j ON / 14, complémentarité stricte des équipes, périodicité 14 j) — « intouchables ».
- **Sécurité multi-tenant Postgres RLS** : 19 tables 100 % sous RLS, 46 policies, confidentialité structurelle (le motif d'une absence isolé dans une table séparée, invisible du conjoint).
- **Tests d'isolation comme livrable** : ~130 tests contre un vrai Postgres (non-fuite entre foyers, révocation d'accès immédiate).
- **PWA hors-ligne** (Serwist) : vues clés consultables sans réseau.
- **Notifications** : Web Push VAPID (3 Edge Functions Deno), repli courriel Resend.
- **Validation aux frontières** : Zod (19 fichiers).
- **Typage strict absolu** : zéro `any` sur 15 900 lignes.
- **Workflow Git discipliné** : branche par sprint, PR vers `dev`, migrations versionnées.

**Phrases CV prêtes** :
- « PWA Next.js 15/React 19/Supabase (~15 900 lignes TS strict, zéro any). »
- « Moteur d'horaire déterministe pur validé par golden tests + tests de propriétés. »
- « Sécurité multi-tenant Postgres RLS : 19 tables (100 % RLS), 46 policies ; ~130 tests d'isolation contre un vrai Postgres. »

**Le plus fort pour** : postes **web/full-stack modernes**, TypeScript, applications métier, **et le storytelling « outil pour travailleurs d'usine »** (relie directement le plancher au logiciel).

---

### 3.4 CoRoute — application de covoiturage (Java)
**Dépôt** : github.com/yvlar/coroute-api (le dépôt `coroute-full` local et distant est **vide** — aucun chiffre disponible)
**Une ligne** : application de covoiturage en Java, projet de génie logiciel à l'Université Laval.

**Notions démontrées** (niveau académique, non quantifié) : programmation Java, génie logiciel (conception, projet d'équipe universitaire).

**⚠️ Limite** : aucun code accessible dans cette session → **ne pas inventer de chiffres, de stack détaillée ni de fonctionnalités**. À présenter comme projet académique Java, sans plus, tant que le dépôt n'est pas fourni.

---

## 4. Notions transversales (prouvées à travers les projets)

| Notion / concept | Prouvé par |
|---|---|
| Tests automatisés (unitaires, intégration, e2e) | SwingBot (460 GoogleTest), TradingClaude (~2 250 pytest + Playwright), GRANDFORD (~340 Vitest) |
| CI/CD (GitHub Actions) | SwingBot (build+ctest), TradingClaude (6 jobs), GRANDFORD |
| Conteneurisation (Docker/Compose) | SwingBot, TradingClaude (5 services), GRANDFORD |
| Architecture par interfaces / injection de dépendances | SwingBot (7 interfaces), TradingClaude (SkillBase) |
| Sécurité applicative | TradingClaude (JWT/CSRF/rate-limit), GRANDFORD (RLS multi-tenant) |
| Bases de données SQL + migrations | TradingClaude (PostgreSQL/Alembic), GRANDFORD (Postgres/Supabase, 19 migrations), SwingBot (SQLite) |
| Async / concurrence | SwingBot (multithread C++), TradingClaude (async/await, Celery) |
| API REST | TradingClaude (74 endpoints), SwingBot (clients broker REST) |
| Typage strict | GRANDFORD (TS zéro any), TradingClaude (TS strict + mypy) |
| Programmation quantitative / finance | SwingBot (backtester, métriques risque, Monte-Carlo), TradingClaude (16 cadres d'analyse) |

---

## 5. Quel projet mettre en avant selon le poste

| Poste / employeur | Projet(s) à mettre en avant en 1er | Angle |
|---|---|---|
| **Infinition** (dev logiciel, C/C++) | SwingBot | C++17, POO, tests, CMake/Git/Python — colle aux exigences |
| **Sogesco** (programmeur, full-stack, forme les users) | TradingClaude + GRANDFORD | Full-stack, SQL, tests unitaires, IA ; + le volet « former les utilisateurs » = métier actuel |
| **Sogenix / Canimex** (automatisation) | Ancrage industriel + SAP + rigueur logicielle | 10 ans d'usine répondent à l'exigence ; automates à apprendre ; SAP quotidien (atout Canimex) |
| **Régulvar** (CVC/immotique, Sherbrooke) | Ancrage industriel + programmation | Terrain + code ; protocoles/immotique à apprendre |
| **Fintech / trading** (moyen terme, Montréal) | SwingBot + TradingClaude | Backtester + analyse financière = profil différenciant rare |

---

## 6. Garde-fous — à NE PAS affirmer

- **GRANDFORD** : `CLAUDE.md` liste TanStack Query et React Hook Form dans la stack *cible*, mais ils **ne sont PAS installés** (absents de `package.json`). Ne pas les revendiquer sur ce projet. Les données y passent par `@supabase/ssr` + supabase-js. *(TanStack Query est bien réel dans TradingClaude, en revanche.)*
- **CoRoute** : dépôt vide dans cette session — **aucun chiffre, aucune stack détaillée, aucune fonctionnalité inventée**. Projet académique Java, point.
- **« Développeur junior »** : ce serait le **premier emploi professionnel salarié en développement**. Le portfolio compense, mais ne jamais prétendre à de l'expérience de dev rémunérée. Les 10 ans sont manufacturiers (formateur, responsable de secteur).
- **SAP** : Yves est **utilisateur quotidien** de SAP en usine (transactions de production). Il n'est **PAS** programmeur ABAP, consultant ni analyste fonctionnel SAP. Ne pas gonfler.
- **Certificat Laval** : c'est un **certificat** (30 crédits), pas un baccalauréat. Le présenter comme « formation équivalente » adossée au portfolio, jamais comme un bac.
- **Certificat en finance quantitative** : en cours — établissement et date à confirmer par Yves avant de l'écrire comme fait daté.
- **Chiffres** : ceux d'ici sont mesurés (juillet 2026) et peuvent bouger si les dépôts évoluent. Arrondir prudemment (« 460 tests », « ~340 tests », « plus de 3 500 tests au total ») ; ne jamais gonfler vers le haut.
