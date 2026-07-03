# Plan emploi — stratégie de recherche

> Objectif : premier emploi de développeur logiciel junior OU programmeur en automatisation, région de Drummondville (Trois-Rivières acceptable), dès maintenant, ~30 $/h.

---

## 1. Lecture du marché local

Le corridor **Drummondville – Victoriaville – Trois-Rivières – Sorel** est un tissu de PME manufacturières (agroalimentaire, transformation, mécanique, portes/quincaillerie, défense) qui ont deux besoins logiciels distincts — et j'ai un pied dans chacun :

| Voie | Type de poste | Ce qu'on y demande | Mon atout |
|---|---|---|---|
| **A. Développement logiciel** | Développeur junior (C++, Python, C#) | POO, Windows/Linux, Git, capacité à livrer | Certificat U. Laval + portfolio livré (SwingBot en C++ colle exactement aux exigences d'Infinition) |
| **B. Automatisation industrielle** | Programmeur automatisation (PLC) | Automates Allen-Bradley/Siemens/Omron + **expérience de projets en usine** | 10 ans ContiTech — l'exigence « 3 à 10 ans d'expérience pertinente de projets en usine » de Sogenix décrit mon parcours mot pour mot |

Les deux voies sont menées **en parallèle** : la voie A valorise d'abord le diplôme et le portfolio ; la voie B valorise d'abord les 10 ans d'usine. Aucune des deux n'exige de compétence que je n'ai pas déjà ou que je ne peux pas acquérir en poste.

## 2. Positionnement — « le développeur qui connaît le plancher d'usine »

C'est un profil rare des deux côtés :

- Les développeurs juniors sortis d'école n'ont jamais vu une ligne de production, un horaire rotatif, un arrêt machine à 3 h du matin, ni la pression d'une non-conformité qualité.
- Les gens de plancher n'ont généralement ni diplôme universitaire en informatique, ni portfolio logiciel public.

Moi, j'ai les deux : **10 ans ContiTech** (formateur, responsable de secteur — coordination d'équipes, qualité, formation, liaison plancher-ingénierie) **+ certificat en informatique (génie logiciel) de l'Université Laval, obtenu, + 3 projets livrés et publics** (SwingBot, TradingClaude, GRANDFORD — voir github.com/yvlar).

Phrase d'ancrage à réutiliser partout : *« automatiser, outiller et fiabiliser la production avec du logiciel »*.

Arguments par objection anticipée :

| Objection | Réponse |
|---|---|
| « Pas d'expérience professionnelle en développement » | Portfolio public complet : C++17 testé (GoogleTest), stack full-web (FastAPI/React/PostgreSQL/Docker), PWA TypeScript testée. Le code est visible, pas théorique. |
| « Certificat, pas un bac » | Les offres visées demandent « DEC ou bac » ou « bac ou formation équivalente » — certificat universitaire + DEC + 10 ans d'expérience = formation équivalente, démontrée par les projets. |
| « Pas d'expérience PLC » (voie B) | Exact, et je le dis d'emblée. Mais la moitié difficile du métier — comprendre les procédés, le terrain, les opérateurs — est déjà acquise. La syntaxe Ladder s'apprend vite avec une base C++/Python. |

## 3. Formation — rien de neuf requis pour postuler

- **Le certificat est obtenu.** Aucune formation supplémentaire n'est un prérequis pour les postes visés.
- Ne PAS retarder les candidatures pour « finir de se préparer » — le portfolio et l'expérience suffisent pour postuler aujourd'hui.

### Priorité 1 — cours courts PLC (si la voie automatisation est active)

La seule vraie case manquante du profil, et elle se comble sans retourner aux études (formations continues à la carte, vérifiées) :

| Formation | Établissement | Lien |
|---|---|---|
| Automates programmables Allen-Bradley — **Débutant** | Cégep de Trois-Rivières (formation continue) | https://formation-mauricie.ca/courslacarte/automates-programmables-allen-bradley-debutant/ |
| Automates programmables Allen-Bradley — **Intermédiaire** | Cégep de Trois-Rivières (formation continue) | https://formation-mauricie.ca/courslacarte/automates-programmables-allen-bradley-intermediaire/ |
| Siemens TIA Portal (S7-1200/1500) | Collège de Maisonneuve (alternative : Cégep du Vieux Montréal) | https://fc.cmaisonneuve.qc.ca/formations/automatisation-industrielle/ |

- Allen-Bradley d'abord : première marque citée par Sogenix, dominante en agroalimentaire nord-américain — et le cours se donne dans la zone cible (Trois-Rivières).
- **Effet candidature** : la ligne « automates à apprendre » de la lettre Sogenix devient « formation Allen-Bradley en cours au Cégep de Trois-Rivières » — l'objection principale tombe.
- Vérifier auprès de **Services Québec** si une subvention pour travailleurs en emploi s'applique.

### Priorité 2 — autoformation immédiate et gratuite

Simulateurs et versions d'évaluation en attendant (ou en parallèle) : LogixPro, Studio 5000/RSLogix (Allen-Bradley), TIA Portal (Siemens) — objectif : arriver en entrevue capable de lire un programme Ladder et d'en parler intelligemment. Effort : quelques soirées.

### Plan C — AEC, seulement si la recherche piétine après 90 jours

| Programme | Établissement | Lien |
|---|---|---|
| AEC Automatismes industriels (soir) | Collège Ahuntsic | https://www.collegeahuntsic.qc.ca/formation-continue/aec-et-dec-en-cours-du-soir/automatismes-industriels-soir/grille-de-cours |
| Instrumentation, automatisation et robotique | Cégep de Victoriaville (~40 min de Drummondville) | https://www.cegepvicto.ca/programme/instrumentation-automatisation-et-robotique-iar/ |

1 à 2 ans d'engagement — à considérer uniquement après avoir épuisé les candidatures, jamais avant.

### À éviter

Bootcamp, deuxième certificat ou certifications web côté développement : le portfolio (70 000+ lignes, 3 500+ tests, CI, Docker) démontre déjà plus qu'aucun cours. Ce temps vaut plus en candidatures et en entrevues qu'en classe. Même logique pour les **certifications SAP payantes** — voir l'avenue ERP ci-dessous.

## 3b. Avenue ERP/SAP — moyen terme (3-5 ans)

**Fait acquis** : j'utilise SAP quotidiennement chez ContiTech (transactions de production) — c'est maintenant dans le CV, et c'est plus crédible qu'une certification aux yeux d'un employeur régional.

**Lecture du marché (vérifiée juillet 2026)** :
- **Canimex (Drummondville) roule sur SAP** — offre « Agent du transport, logistique et soutien SAP » observée (https://to.indeed.com/aalsjpjz7z2k). À mentionner dans ma candidature Canimex : usage quotidien de SAP = atout direct.
- Le marché SAP « développeur/consultant » est concentré à Montréal et **entièrement sénior** (Accenture, Infosys, Sopra Steria, analyste principal Agropur…) — aucun poste junior observé. Une certification payante maintenant n'ouvrirait aucune porte.

**Chemin réaliste** : entrer comme développeur/programmeur dans un manufacturier qui roule SAP (Canimex en tête) → devenir naturellement le pont plancher-ERP (ma spécialité) → viser analyste fonctionnel SAP (modules production/matières) à 3-5 ans, où le vécu d'usine vaut de l'or.

**Formation** : rien de payant. En option, les parcours gratuits officiels (learning.sap.com, MOOC openSAP) pour pouvoir écrire « autoformation SAP en cours » — seulement APRÈS le cours Allen-Bradley, qui reste la priorité d'investissement.

## 4. Plan 30-60-90 jours

### Jours 0-30 — tout lancer

- [ ] Mettre à jour le profil Indeed (`cv/cv-indeed.md`) et LinkedIn (`cv/profil-linkedin.md`, open-to-work recruteurs seulement)
- [ ] Postuler chez **Infinition** (offre Indeed, lettre `candidatures/lettres/infinition.md`)
- [ ] Postuler chez **Sogenix** (rh@sogenix.com, lettre `candidatures/lettres/sogenix.md`)
- [ ] Contacter **Canimex** (recrutement@canimex.com · 819-477-1335)
- [ ] Lancer les candidatures spontanées : Soucy (carriere.soucy-group.com), Cascades (jobs.cascades.com), Synovatec, Régulvar, SOPREMA
- [ ] Sonder discrètement la **mutation interne TI chez ContiTech** (plan B sans risque de trou d'emploi)
- [ ] Tenir `candidatures/suivi.md` à jour à chaque action

### Jours 30-60 — relancer et élargir

- [ ] Relancer chaque candidature sans réponse après 10-14 jours (courriel court, poli, avec le lien GitHub)
- [ ] Élargir la zone : alertes Indeed/LinkedIn sur Trois-Rivières, Victoriaville, Sorel-Tracy et **Sherbrooke** (offre Régulvar trouvée — voir suivi) ; alertes de veille C++ sur Québec (Thales, Evident/Wabtec) pour dans 1-2 ans
- [ ] Préparer les entrevues : démo de SwingBot et TradingClaude prête à montrer (5 minutes, code + résultat)
- [ ] Si voie B active : autoformation PLC/Ladder entamée + **inscription au cours Allen-Bradley débutant, Cégep de Trois-Rivières** (voir §3)

### Jours 60-90 — ajuster le tir

- [ ] Bilan du taux de réponse : si faible côté A, renforcer la mise en avant du portfolio (README des dépôts, épingler les bons projets) ; si faible côté B, viser aussi les intégrateurs d'automatisation de la région
- [ ] Considérer sérieusement la mutation interne ContiTech si aucune offre externe ne se dessine
- [ ] Réviser le salaire cible seulement si le marché le force — 30 $/h reste réaliste pour le double profil

## 5. Règles d'hygiène

- **Confidentialité** : ce dépôt reste privé ; open-to-work jamais public ; pas de recherche d'emploi depuis les équipements ou le réseau de ContiTech.
- **Traçabilité** : chaque envoi, relance et réponse est consigné dans `candidatures/suivi.md` le jour même.
- **Honnêteté** : aucune compétence gonflée — le positionnement est assez fort sans rien inventer.
