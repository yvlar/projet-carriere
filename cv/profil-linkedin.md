# Profil LinkedIn — contenu section par section

> À copier-coller dans LinkedIn, section par section.
> ⚠️ Régler la visibilité AVANT de modifier le contenu (voir la dernière section) : par défaut, LinkedIn notifie le réseau des changements de profil — donc potentiellement des collègues ContiTech.

---

## 0. Réglages à faire EN PREMIER (avant toute modification)

1. **Désactiver les notifications de modification de profil** : Paramètres → Visibilité → « Partager les modifications de profil » → **Non**.
2. **Open to work — recruteurs seulement** : Profil → « Open to » → « Finding a new job » → visibilité « **Recruteurs uniquement** » (jamais le cadre vert public « #OpenToWork »). LinkedIn ne garantit pas à 100 % que les recruteurs de l'employeur actuel ne le voient pas, mais il tente de les exclure — c'est le bon compromis.
   - Intitulés recherchés : `Développeur logiciel junior` · `Programmeur en automatisation` · `Développeur C++` · `Développeur Python`
   - Lieux : `Drummondville, Québec` · `Trois-Rivières, Québec`
   - Type : Temps plein, permanent · Date de début : dès maintenant

## 1. Titre (headline)

```
Développeur logiciel junior — C++ / Python / SQL · Certificat en informatique (génie logiciel), Université Laval · 10 ans d'expérience manufacturière
```

## 2. Section « Infos » (About)

```
Le développeur qui connaît le plancher d'usine.

Après 10 ans chez ContiTech — d'abord responsable de secteur, aujourd'hui formateur — je fais le saut vers le développement logiciel, avec en main un certificat en informatique (génie logiciel) de l'Université Laval et un portfolio de projets complets et publics.

Ce que l'usine m'a appris : coordonner des équipes en horaire rotatif, tenir les standards de qualité, résoudre des problèmes sous pression, former et vulgariser, faire le pont entre le plancher et l'ingénierie — et travailler quotidiennement dans SAP (transactions de production). Ce que le logiciel m'a permis de livrer :

▸ SwingBot — bot de trading algorithmique C++17, ~14 000 lignes : architecture par interfaces (injection de dépendances), 460 tests GoogleTest, backtester complet (Sharpe, drawdown, win rate) avec validation walk-forward et Monte-Carlo, intégrations Interactive Brokers/Alpaca, dashboard WebSocket, CI GitHub Actions
▸ TradingClaude — plateforme d'analyse financière IA, ~44 500 lignes : FastAPI (74 endpoints), PostgreSQL, Redis/Celery, RAG Qdrant, React 18/TypeScript strict — ~2 250 tests pytest, 531 tests Vitest, e2e Playwright, CI à 6 jobs, Docker Compose (5 services)
▸ GRANDFORD — PWA Next.js/Supabase, ~15 900 lignes de TypeScript strict : moteur d'horaire pur validé par golden tests, sécurité Postgres RLS (19 tables, 46 policies), ~340 tests Vitest dont ~130 d'isolation contre un vrai Postgres, Web Push, mode hors-ligne

Au total : plus de 70 000 lignes de code et plus de 3 500 tests automatisés, publics et vérifiables.

Mon objectif : automatiser, outiller et fiabiliser la production avec du logiciel, dans la région de Drummondville / Trois-Rivières.

Portfolio complet : github.com/yvlar
Contact : ivess49@gmail.com
```

## 3. Section « Expérience »

### Formateur — ContiTech
*Juin 2023 – aujourd'hui · Drummondville, Québec*

```
Formation des employés de production dans une usine en horaire rotatif.

- Conçois et anime des formations techniques : vulgarisation de procédés complexes pour des publics variés
- Documente les contenus de formation et assure le suivi des acquis
- Fais le lien entre les nouvelles recrues, les exigences de production et les standards de qualité
- Utilise SAP (ERP) quotidiennement : transactions de production en contexte manufacturier

Compétences transférables vers le logiciel : communication, vulgarisation technique, documentation, pédagogie.
```

### Responsable de secteur — ContiTech
*Janvier 2016 – juin 2023 · Drummondville, Québec*

```
Coordination d'un secteur de production en horaire rotatif.

- Coordonnais les équipes de production : priorités, affectations, suivi de la cadence
- Gérais la qualité au quotidien : suivi des non-conformités, application des standards, résolution de problèmes sur le terrain
- Assurais la liaison entre le plancher de production et l'ingénierie : remontée des problèmes techniques et participation à leur résolution

Compétences transférables vers le logiciel : coordination, rigueur qualité, résolution de problèmes, compréhension fine des contraintes de production.
```

## 4. Section « Formation »

| Champ | Valeur |
|---|---|
| École | Université Laval |
| Diplôme | Certificat en informatique (génie logiciel) — obtenu |

| Champ | Valeur |
|---|---|
| École | Cégep de Drummondville |
| Diplôme | Diplôme d'études collégiales (DEC) |

## 5. Section « Projets »

### SwingBot — bot de trading algorithmique
*Lien : github.com/yvlar/swingtradebot*
```
Bot de trading algorithmique C++17 (~14 000 lignes, 460 tests GoogleTest) : stratégie EMA/RSI avec filtre SMA200, architecture par interfaces avec injection de dépendances, backtester complet (Sharpe, Sortino, max drawdown, win rate), validation walk-forward et Monte-Carlo, intégrations Interactive Brokers/Alpaca, persistance SQLite, dashboard temps réel WebSocket (Boost.Beast), code multithread, build CMake/vcpkg, Docker, CI GitHub Actions.
```

### TradingClaude — plateforme d'analyse financière IA
*Lien : github.com/yvlar/TRADINGCLAUDE*
```
Plateforme d'analyse financière IA (~44 500 lignes) : FastAPI (74 endpoints REST), 16 modules d'analyse orchestrés en workflows, PostgreSQL (12 migrations Alembic), Redis, Celery, RAG vectoriel Qdrant, authentification JWT + protection CSRF + rate-limiting, React 18/TypeScript strict (15 pages), ~2 250 tests pytest, 531 tests Vitest, tests e2e Playwright, Docker Compose (5 services), CI GitHub Actions (6 jobs).
```

### GRANDFORD — PWA d'horaires pour travailleurs d'usine
*Lien : github.com/yvlar/GRANDFORD*
```
PWA Next.js 15/React 19/Supabase (~15 900 lignes de TypeScript strict) pour travailleurs d'usine en rotation 12 h : moteur d'horaire TypeScript pur (cycle Pitman 2-2-3) validé par golden tests et tests de propriétés, sécurité multi-tenant Postgres RLS (19 tables, 46 policies), ~340 tests Vitest dont ~130 d'isolation RLS exécutés contre un vrai Postgres, 3 Edge Functions, notifications Web Push (VAPID), mode hors-ligne (Serwist).
```

### CoRoute — application de covoiturage
*Lien : github.com/yvlar/coroute-api*
```
Application de covoiturage en Java — projet de génie logiciel, Université Laval.
```

## 6. Section « Compétences » (épingler les 3 premières)

Ordre suggéré :

1. **C++**
2. **Python**
3. **SQL**
4. TypeScript
5. Java
6. React
7. FastAPI
8. Git
9. Docker
10. Linux
11. HTML5
12. C#
13. PHP
14. SAP (utilisateur)
15. Formation d'employés
16. Coordination d'équipes
17. Contrôle qualité

## 7. Divers

- **Localisation du profil** : Drummondville, Québec, Canada
- **Secteur** : Développement de logiciels
- **URL personnalisée** : linkedin.com/in/… (choisir un slug propre, p. ex. `yves-lariviere-dev`)
- Ajouter le lien `github.com/yvlar` dans la section « Coordonnées » du profil
