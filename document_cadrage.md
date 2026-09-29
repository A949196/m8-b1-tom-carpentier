# Document de cadrage — Cabinet Maître Devalle (Bordeaux)

> Version de travail : §2 à §6 rédigés, §1 provisoire (à réécrire en dernier, après l'imprévu de 14h30). Plafond : 3 pages, à vérifier au rendu..

## 1. Synthèse exécutive (5-6 lignes — rédigée EN DERNIER)
Le cabinet perd du temps à retrouver ses propres décisions (environ 10 recherches par jour, estimées à 30 minutes) et à réécrire ses courriers types (environ 15 par jour). Nous proposons **une recherche dans le texte des décisions du cabinet, avec les filtres du registre, hébergée en France, et une bibliothèque de courriers types à jour**. Aucun outil ne rédige de texte tout seul (IA générative) à ce stade : chaque résultat renvoie à un document réel que l'avocat vérifie.
Indicateurs clés : recherche de 30 minutes à moins de 5 minutes (objectif : moins d'une minute) ; **0 décision inventée** ; environ 25 minutes gagnées par avocat et par jour grâce à la recherche (l'objectif d'une heure n'est pas démontré). Budget visé : 15 000 €, estimation détaillée en phase de conception.
 
> **Imprévu client (14h30) — ce que ça change** : _à compléter après le message du client._

## 2. Besoin métier et contexte (1 paragraphe)
**Demande exprimée** : « un assistant pour aller plus vite, et retrouver les bonnes jurisprudences en 30 secondes au lieu de 30 minutes ».
 
**Besoin réel** : le cabinet perd du temps parce que son savoir est difficile à retrouver et à réutiliser. Deux besoins distincts :
1. **Retrouver vite, avec la preuve, les décisions que le cabinet a lui-même obtenues** (environ 2 000 en quinze ans, cherchées aujourd'hui par nom de fichier ou en demandant à un collègue). La jurisprudence publique est déjà couverte par votre abonnement à une base juridique en ligne. Environ 10 recherches par jour, estimées à 30 minutes chacune : environ 5 heures par jour pour tout le cabinet (estimation à mesurer).
2. **Ne plus réécrire les courriers types à partir de vieux courriers** : environ 15 par jour, copiés-collés depuis les postes de chacun, le dossier « modèles » partagé datant de 2019.
Priorité : Maître Devalle dit que « c'est surtout la recherche qui prend du temps ». Nous proposons de commencer par la recherche, à valider.
 
**Contraintes révélées en entretien** : aucune erreur tolérée (décision inventée ou fuite = responsabilité personnelle devant le Barreau) ; tout résultat doit être vérifiable ; pas de « cloud américain », hébergeur français envisageable ; budget de 15 000 € au démarrage puis quelques centaines d'euros par mois ; délai : « du fiable dans six mois plutôt que du risqué dans un mois » ; explications sans jargon.

## 3. Données — mini-cours `02`
| Donnée | Existante / à acquérir | Volume, qualité estimée | Personnelle ? |
|---|---|---|---|
| Décisions obtenues par le cabinet | Existante (serveur du cabinet) | Environ 2 000 sur 15 ans, PDF ou Word ; **anciennes décisions en scans papier peu lisibles, part inconnue**. Aucune décision reçue : qualité non vérifiée | Oui : clients, parties adverses, salariés, enfants ; non anonymisées |
| Registre des décisions (tenu par une assistante) | Existante | Colonnes : numéro, date, matière, juridiction, issue, fichier. Extrait de 19 lignes reçu ; couverture et mise à jour inconnues | Aucun nom vu sur l'extrait |
| Courriers archivés (dossiers clients, postes des avocats) | Existante | « Des milliers » ; aucun exemple reçu, qualité inconnue | Probable (non confirmé) |
| Dossier « modèles » partagé | Existante | Daté de 2019, non mis à jour : peu fiable | À vérifier |
| Base juridique en ligne (jurisprudence publique) | Existante (abonnement) | Anonymisée ; déjà couverte, **hors périmètre proposé** | Non |
| Texte lisible des anciens scans | **À acquérir** | Nécessite une reconnaissance automatique de texte (OCR) ; coût et délai dépendent de la part de scans | Oui (mêmes documents) |
| Contenu de chaque décision (point de droit, mots-clés) | **À acquérir** | Absent du registre : à extraire ou à saisir | Oui |
| Courriers types à jour | **À acquérir** | À sélectionner et valider par le cabinet | À vérifier |
| Temps de recherche mesuré | **À acquérir** | Les « 30 minutes » sont une estimation | Non |
 
**Étiquettes existantes** : le registre donne déjà la matière, la juridiction et l'issue de chaque décision. Cela permet de filtrer, mais pas de retrouver une décision par son contenu.
 
**Constats sur l'extrait du registre (19 lignes, comptées à la main)** :
- Matières : recouvrement 8, bail commercial 4, famille 4, prud'hommes 2, sociétés 1 ; issues : favorable 9, défavorable 7, transaction 3.
- **Extrait non représentatif** : identifiants consécutifs (DEC-1000 à DEC-1018) et dates de 2020 à 2025, alors que le cabinet parle de quinze ans.
- **Juridiction douteuse** : « TJ Bordeaux » sur les 19 lignes, y compris deux affaires prud'homales (erreur de saisie ou valeur par défaut, à vérifier).
- **Noms de fichiers non parlants** (`decision_1004.pdf`) : le registre existe pourtant et la recherche reste longue, à comprendre (§6).

## 4. Risques et conformité — mini-cours `04` et `07`

**Usage réel** : les avocats et assistantes interrogent l'outil pour retrouver une décision du cabinet, ou préparent avec lui un brouillon de courrier. Le résultat est une liste de documents du cabinet ou un brouillon. Il ne déclenche aucune action : l'avocat relit, corrige et signe, et peut l'écarter. Qui vérifie une décision retrouvée n'a pas été précisé (§6).
 
**Qualification AI Act** (le règlement européen sur l'IA) :
- **Pratique interdite** : aucune.
- **Haut risque** : probablement non. L'outil n'est pas un produit réglementé (Annexe I). Le cas « justice » de l'Annexe III vise l'usage par ou pour une autorité judiciaire, ce qu'un cabinet d'avocats n'est pas. Le cas « emploi » ne s'applique pas tant que l'outil n'évalue pas les salariés. À reconfirmer sur le texte (EUR-Lex).
- **Transparence** : si l'outil dialogue avec l'utilisateur, celui-ci doit savoir qu'il s'adresse à une IA. Simple à respecter. Former les utilisateurs à l'IA (art. 4).
- **Condition de bascule vers haut risque** : (a) l'outil serait utilisé par ou pour un tribunal ou une instance de règlement de litiges ; (b) il servirait à évaluer ou surveiller le travail des avocats ou des assistantes (par exemple mesurer leur rapidité).
**RGPD** (protection des données personnelles) :
- **Base légale proposée : intérêt légitime**. Le cabinet retrouve, dans ses propres archives, des documents qu'il détient déjà pour exercer son métier. Les autres bases conviennent mal : le consentement est impossible à recueillir auprès des parties adverses, et le contrat lie chaque client à son seul dossier, pas à un moteur de recherche couvrant tous les dossiers. **Conditions** : peser l'intérêt du cabinet face aux droits des personnes (dont les enfants), informer les clients, prévoir un droit d'opposition, ne traiter que le nécessaire, fixer une durée de conservation. Réutiliser un dossier pour un autre usage est une finalité nouvelle : compatibilité à vérifier.
- **Données sensibles** : les affaires familiales peuvent en contenir (non précisé par le cabinet). Une exception existe pour l'exercice ou la défense d'un droit en justice ; **à valider avec le DPO ou le conseil du cabinet**.
- **Profilage** : aucun prévu. À surveiller si l'outil produisait des statistiques sur des personnes.
- **Décision automatisée** : ne s'applique pas, car les deux conditions ne sont pas réunies : la décision n'est pas exclusivement automatisée (l'avocat signe) et n'a pas d'effet juridique. **Vigilance** : une relecture faite « pour la forme » changerait l'analyse.
| Risque | 🔴/🟠/🟡 | Obligation ou raison | Traitement dans l'archi (hypothèse, à confirmer §5) |
|---|---|---|---|
| Décision ou jurisprudence inventée | 🔴 | Responsabilité professionnelle ; « tout doit être vérifiable » | L'outil ne renvoie que des documents réels du cabinet, avec lien vers l'original ; aucune citation sans source ; relecture par l'avocat |
| Fuite de données couvertes par le secret professionnel | 🔴 | Obligation déontologique, responsabilité devant le Barreau | Hébergement en France, aucun transfert hors de France, accès authentifié, journal des consultations |
| Données de tiers et de mineurs (affaires familiales) | 🔴 | RGPD : minimisation, art. 9 | Accès restreint, pas de copie vers un service externe, matière « famille » traitée à part si le DPO l'exige |
| Accès élargi aux dossiers : un avocat peut ouvrir ceux d'un autre | 🟠 | Secret professionnel ; l'outil rend l'accès plus facile | Journal des accès ; droits par dossier à trancher (§6) |
| Anciens scans mal lus : décision existante non retrouvée | 🟠 | Fiabilité ; risque de fausse assurance | Message « aucun résultat trouvé » ≠ « aucune décision » ; contrôle de la lisibilité |
| Courrier contenant des informations d'un autre client (copier-coller) | 🟠 | Secret professionnel | Modèles neutres à jour, relecture obligatoire par l'avocat |
| Dérive vers l'évaluation des salariés | 🟡 | Bascule en haut risque (AI Act) | Aucune donnée sur l'usage individuel exploitée pour évaluer ; à inscrire dans la charte d'usage |
 
Point de vigilance : Microsoft 365 est déjà utilisé pour les mails et Word. Il faut vérifier si cela relève du refus du « cloud américain » (§6).
 
**Sécurité du modèle** — exposition : outil interne, utilisateurs identifiés (12 avocats et assistantes), documents non publics, aucune interface ouverte à des tiers. Hypothèse de travail (à confirmer en §5, avec la grille de décision) : l'outil retrouve et cite des documents réels.
 
| Menace | Plausibilité sur CE cas | Mitigation proposée | Risque résiduel |
|---|---|---|---|
| Fuite de documents confidentiels vers l'extérieur ou vers un utilisateur non autorisé | 🟠 Documents très sensibles, accès ouvert entre avocats | Hébergement français, authentification, limitation des requêtes, journal des consultations | Une personne autorisée copie volontairement un document |
| Consigne cachée dans un document (injection indirecte) | 🟡 seulement si un modèle de langage lit des documents venant de tiers (pièces adverses, courriers reçus) | Contenu traité comme donnée, jamais comme consigne ; sortie limitée à citer et lier ; vérification humaine | Consigne subtile non détectée. **Sans objet si aucun modèle de langage n'est retenu** |
| Ajout d'un faux document dans la base de recherche | 🟡 | Ajout réservé au personnel habilité, ajouts journalisés | Erreur ou malveillance interne |
| Entrée trompeuse (adversarial), vol du modèle | ⚪ Écartées : aucun tiers ne soumet d'entrée et aucun modèle propre n'est exposé | — | — |

## 5. Architecture cible et sobriété — mini-cours `05`
Schéma : `schema_archi_cible.md`. Six briques, toutes hébergées en France avec accès par identifiant : le serveur du cabinet, la préparation des scans (reconnaissance de texte), un index de recherche, une interface pour les avocats et assistantes, la bibliothèque de courriers types et un journal des consultations. Le nœud « résultat trouvé et texte lisible ? » évite qu'un silence soit pris pour une absence.
 
**Modèle de langage (IA qui rédige des textes) : refusé à ce stade.** Le besoin est de retrouver des documents réels, pas d'en générer, et une décision inventée est le risque que vous excluez. Une recherche dans le texte suffit pour environ 2 000 décisions et tient dans votre budget.
**Condition de bascule** : si un essai sur un échantillon montre que la recherche par mots ne retrouve pas la bonne décision assez souvent (seuil à fixer, §6), on envisagera une aide à la recherche par un modèle hébergé en France, sans qu'il produise de citation. Comparaison à faire avec la grille de décision C4.
**Écarté** : assistant qui répond en langage naturel (RAG), agents qui agissent seuls, modèle entraîné sur vos décisions, tout service hébergé hors de France.

## 6. Indicateurs, seuils, questions ouvertes
| Indicateur | Cible | Seuil d'acceptabilité | Comment on le mesure |
|---|---|---|---|
| Temps pour retrouver une décision | 30 min (estimation, à mesurer) → moins d'1 min (votre objectif) | 5 min en moyenne (proposé) | Chronométrage de 2 semaines avant, puis journal des consultations |
| Bonne décision dans les 5 premiers résultats | ≥ 90 % (proposé) | ≥ 80 % (proposé) : un échec se rattrape par le registre ou un collègue | Test sur 30 recherches réelles du cabinet |
| Décisions inventées ou sans document source | 0 | 0, non négociable : responsabilité personnelle de l'avocat | Vérification sur les 30 recherches de test, puis contrôle régulier |
| Temps gagné par avocat et par jour | 25 min via la recherche (10 × 25 min ÷ 12) ; 1 h si les courriers y contribuent, non démontré | 20 min | Temps de recherche × nombre de recherches, temps de rédaction mesuré avant/après |
| Coût | Mise en place ≤ 15 000 € ; abonnement mensuel « quelques centaines d'euros » | Plafond mensuel à chiffrer avec vous | Devis de l'hébergeur et des prestataires |
 
Les cibles et seuils marqués « proposé » sont des propositions à valider avec le cabinet : ils ne viennent pas d'un chiffre donné en entretien. Le seuil sur les erreurs est justifié par leur coût : une décision non retrouvée se rattrape, une décision inventée engage la responsabilité personnelle.
 
**Prochaines étapes** : (1) mesurer pendant 2 semaines le temps de recherche et de rédaction d'un courrier ; (2) transmettre le registre complet et quelques décisions anonymisées, dont des scans, pour tester la lisibilité et la recherche ; (3) valider avec le DPO ou le conseil du cabinet la base légale, les données sensibles et l'hébergeur.
 
**Questions ouvertes**
- Le registre contient-il toutes les décisions et est-il à jour ? Pourquoi la recherche prend-elle encore 30 min, alors qu'un registre existe ?
- Quelle part des 2 000 décisions est en scan papier, et pourquoi les décisions n'ont-elles pas pu être transmises ?
- Combien de minutes prend un courrier type aujourd'hui ? Les 30 min de recherche sont-elles mesurées ?
- Les assistantes peuvent-elles ouvrir les dossiers ? Faut-il des droits par dossier ou par matière (famille) ? Existe-t-il un journal des accès ?
- Quel est le logiciel de gestion du cabinet et peut-il s'intégrer ? Microsoft 365 est-il compatible avec le refus du « cloud américain » ? Quelles garanties attendez-vous d'un hébergeur « sérieux » ?
- Que couvrent les 15 000 € (hébergement, numérisation, formation) ? Le budget est-il ferme ?
- Recherche ou courriers d'abord ? Quel taux de bonnes décisions retrouvées jugez-vous suffisant ?
- Quelles données sensibles contiennent les affaires familiales ? Un outil a-t-il déjà été essayé, et pourquoi a-t-il été abandonné ?
