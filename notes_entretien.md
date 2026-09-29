# Notes d'entretien — Cas A : Cabinet Maître Devalle (juridique PME)

> Demande exprimée : « un assistant pour aller plus vite sur les courriers types, et retrouver les bonnes jurisprudences en 30 secondes au lieu de 30 minutes ».
> Client : cabinet de 12 avocats, Bordeaux. Interlocutrice : Maître Élise Devalle.

## 1. Avant le rendez-vous — 12 questions + 3 de réserve

Liste préparée avant l'entretien. Elle a été adaptée en cours de route (voir §2) : les questions du bot doivent être simples, courtes et à un seul sujet.

| # | Priorité (1-3) | Catégorie | Question |
|---|---|---|---|
| 1 | 1 | Besoin | Entre les courriers types et la recherche de jurisprudence, lequel est le plus urgent pour vous ? |
| 2 | 1 | Processus actuel | Comment un avocat cherche-t-il une jurisprudence aujourd'hui ? |
| 3 | 1 | Processus actuel | Combien de courriers types rédigez-vous par semaine ? |
| 4 | 1 | Processus actuel / KPI | Combien de recherches de jurisprudence faites-vous par semaine ? |
| 5 | 2 | Données : existence | Où sont stockés vos anciens courriers ? |
| 6 | 1 | Données : extrait | Pouvez-vous nous transmettre trois courriers anonymisés ? |
| 7 | 1 | Données personnelles | Ces courriers contiennent-ils des données de vos clients ? |
| 8 | 1 | Critère de succès | Quel résultat chiffré vous ferait dire que le projet est réussi ? |
| 9 | 1 | Coût d'une erreur | Que se passe-t-il si une jurisprudence citée est fausse ? |
| 10 | 2 | Utilisateurs | Qui utiliserait l'outil au quotidien ? |
| 11 | 2 | SI / hébergement | Où vos données doivent-elles être hébergées ? |
| 12 | 3 | Budget | Quel budget avez-vous prévu ? |
| R1 | réserve | Validation humaine | Qui relit un courrier avant son envoi ? |
| R2 | réserve | SI | Quel logiciel de gestion de cabinet utilisez-vous ? |
| R3 | réserve | Délai | Quel délai visez-vous ? |

**Ajustements décidés pendant l'entretien** (le journal Discord fait foi) :
- La valeur du cabinet étant dans ses propres décisions, « jurisprudence » est devenu « décisions » dans les questions.
- Question imposée par le cours (volumétrie labellisée), absente de ma liste initiale : ajoutée en cours d'entretien, reformulée pour un client métier (« Vos décisions sont-elles classées par type d'affaire ? »).
- Trois questions reformulées après une réponse hors sujet du bot : le volume de décisions (avec choix d'ordres de grandeur), l'accès aux dossiers (deux essais).
- Demande d'extrait posée avec le mot « anonymisées » : elle a obtenu le registre, pas les décisions.

## 2. Pendant le rendez-vous — dit / interprété

| Question posée (telle quelle) | Ce que le client a **dit** (citation) | Ce que j'en **interprète** |
|---|---|---|
| **R1** — Comment un avocat cherche-t-il une jurisprudence aujourd'hui ? *(libellé exact à vérifier dans le journal)* | « Pour la jurisprudence publique, on a un abonnement à une base juridique en ligne. Mais notre vraie richesse, ce sont nos propres dossiers : les décisions qu'on a obtenues ici, à Bordeaux. Elles sont rangées dans des dossiers sur le serveur, et on cherche par nom de fichier… ou on demande au collègue qui s'en souvient. » | La jurisprudence publique est déjà couverte. Le besoin réel semble être de retrouver le savoir interne du cabinet. Ce savoir dépend de la mémoire de certaines personnes (hypothèse). |
| **R2** — Question sur les courriers *(libellé exact à vérifier dans le journal)* | « Chaque avocat a ses vieux courriers sur son poste, et on copie-colle. Il y a bien un dossier "modèles" partagé, mais il date de 2019 et personne ne le met à jour. Les assistantes préparent, l'avocat relit et signe. » | Pas de source unique pour les courriers. Relecture humaine existante, systématique ou non : inconnu. Le copier-coller peut mélanger des informations de clients (hypothèse, non dite). |
| **HS-a** — Combien de décisions sont rangées sur ce serveur ? | Le bot a répété mot pour mot la réponse R1. | Question non comprise. Aucune information obtenue, reformulée juste après. |
| **R3** — Environ combien de décisions avez-vous : des dizaines, des centaines ou des milliers ? | « Environ 2 000 décisions sur les quinze dernières années, en PDF ou en Word, plus des milliers de courriers archivés dans les dossiers clients. Les plus anciennes décisions sont des scans papier, pas toujours très lisibles. » | Volume modeste (environ 130 par an). Qualité hétérogène : une part inconnue de scans à convertir en texte. Deux stocks distincts, décisions et courriers. |
| **R4** — Pouvez-vous nous transmettre trois décisions anonymisées ? | « Bien sûr : nos clients, les parties adverses, parfois des salariés, des enfants dans les affaires familiales. Les décisions publiques sont anonymisées, les nôtres non. » | Le bot a surtout répondu sur les données personnelles : elles sont avérées, dont celles de tiers et de mineurs. Les décisions du cabinet ne sont pas anonymisées, l'anonymisation serait donc à faire avant tout partage. « Bien sûr » ne suffisait pas pour l'extrait : la suite a montré que seul le registre serait transmis. |
| **R5** — Combien de temps prend aujourd'hui la recherche d'une de vos décisions ? | « Si chaque avocat gagne une heure par jour sans prendre le moindre risque déontologique, je signe tout de suite. Et pour la recherche : retrouver la bonne décision en moins d'une minute. » | Objectifs, pas mesure actuelle. Critère de succès : 1 h/jour/avocat et moins d'une minute par recherche. La condition « sans risque déontologique » est très forte. Pas de seuil de fiabilité chiffré. |
| **R6** — Où vos données doivent-elles être hébergées ? | « Je ne veux pas que mes dossiers partent dans un cloud américain. Un hébergeur français avec un contrat sérieux, pourquoi pas, notre logiciel de gestion de cabinet l'est déjà. Mais il faudra me l'expliquer simplement. » | Fournisseurs américains exclus. Hébergeur français envisageable. « Sérieux » et le périmètre exact de l'exclusion ne sont pas définis. La cliente attend des explications sans jargon. |
| **R7** — Que se passe-t-il si une décision citée par l'outil est fausse ? | « Une erreur dans un courrier ou une jurisprudence qui n'existe pas, c'est ma responsabilité professionnelle engagée. J'ai lu cette histoire d'avocats américains qui ont cité des décisions inventées par une IA. Ça, jamais chez nous. Tout doit être vérifiable. » | Coût d'une erreur élevé et personnel. Exigence de vérifiabilité : chaque résultat devrait renvoyer à un document réel (conséquence possible, non dite). |
| **HS-b** — Qui peut lire ces dossiers aujourd'hui ? | Le bot n'a pas compris (pas de réponse exploitable). | Question trop abstraite. Reformulée. |
| **HS-c** — Sur le serveur du cabinet, qui peut ouvrir les décisions : tous les avocats, seulement l'avocat du dossier, ou aussi les assistantes ? | Le bot a répété mot pour mot la réponse R2. | Les trois choix ont pu la faire passer pour une question composée. Reformulée en une seule idée. |
| **R8** — Un avocat peut-il ouvrir les dossiers d'un autre avocat ? | « Absolument. Tout ce qui est dans nos dossiers est couvert par le secret professionnel. C'est une obligation déontologique : si ça fuit, c'est ma responsabilité personnelle devant le Barreau, pas seulement une amende. » | Accès apparemment ouvert entre avocats, sans cloisonnement par dossier (« Absolument » est ambigu). Secret professionnel confirmé sur tous les documents. Le cas des assistantes n'est pas confirmé. |
| **R9** — Entre retrouver vos décisions internes et rédiger les courriers types, lequel est le plus urgent pour vous ? | « Deux choses. D'abord les courriers types, mises en demeure, transmissions de dossier : on les réécrit à partir d'anciens courriers, c'est du temps perdu. Ensuite, et c'est le plus pénible, retrouver une décision qu'on a déjà obtenue ou étudiée : trente minutes pour ce qui devrait en prendre trente secondes. » | Les deux besoins comptent, ordre non tranché. Les « 30 minutes » sont ici donnés comme temps actuel, mais c'est une estimation sans mesure. |
| **R10** — Combien de recherches de décision faites-vous par semaine ? | « Pour tout le cabinet, une quinzaine de courriers types par jour, et une dizaine de recherches de jurisprudence interne par jour. C'est surtout la recherche qui prend du temps. » | Volumes par jour, pas par semaine, pour tout le cabinet. Ma lecture : la recherche passe avant les courriers. Calcul indicatif : 10 recherches × 30 min ≈ 5 h/jour, soit environ 25 min par avocat. Le gain d'1 h/jour/avocat (12 h/jour) n'est donc pas démontré côté recherche seule. |
| **R11** — Quel budget avez-vous prévu ? | « Serré. On est un cabinet de douze, pas un grand groupe. Mettons 15 000 euros pour démarrer, et ensuite un abonnement mensuel raisonnable, pas plus de quelques centaines d'euros par mois. » | Contrainte de coût forte. Ce que couvrent les 15 000 € (hébergement, numérisation, formation) n'est pas dit, ni si le budget est ferme. |
| **R12** — Quel délai visez-vous pour la mise en place ? | « Pas d'urgence absolue. Je préfère quelque chose de fiable dans six mois que quelque chose de risqué dans un mois. » | La fiabilité passe avant la vitesse. Six mois est un horizon, pas un engagement ferme. |
| **R13** — Vos décisions sont-elles classées par type d'affaire ? | « Une assistante tient un registre des décisions : numéro, date, matière, juridiction, issue, et le nom du fichier. Je vous en transmets un extrait, seulement le registre, pas les décisions elles-mêmes, vous comprendrez pourquoi. » *(fichier transmis : 19 lignes)* | Des étiquettes existent déjà (matière, issue), mais le registre est tenu à la main. Les décisions ne sortent pas : je suppose le secret professionnel (non dit). Extrait vu : matières dominantes recouvrement (8/19) et bail commercial (4), famille (4), prud'hommes (2), sociétés (1). Dates 2020-2025 alors que le client parle de quinze ans : couverture à confirmer. Extrait non représentatif (identifiants consécutifs). « TJ Bordeaux » sur toutes les lignes, y compris des affaires prud'homales : erreur de saisie ou valeur par défaut. Les noms de fichiers (`decision_NNNN.pdf`) ne disent rien du contenu. Le registre décrit le dossier, pas le contenu (point de droit, motifs). |
| **R14** — Quel est le nom de votre logiciel de gestion de cabinet ? | « Un logiciel de gestion de cabinet du marché pour les dossiers et la facturation, hébergé en France, Microsoft 365 pour les mails et Word, et un serveur de fichiers au cabinet pour les documents. » | Le nom n'est pas donné : intégration inconnue. Point de tension : refus du « cloud américain » mais Microsoft 365 déjà utilisé, sans dire si cela la gêne. Les décisions sont probablement sur le serveur local. |
| **IMPRÉVU (14h30)** — message de Maître Devalle, objet « changement côté informatique » | « Notre prestataire informatique nous a annoncé ce matin qu'il arrête son contrat au 31 décembre. On va en chercher un autre, mais d'ici là on n'aura plus personne pour s'occuper du serveur du cabinet. Est-ce que ça change quelque chose à ce que vous allez nous proposer ? » | Oui. Le serveur, qui contient les décisions, n'aura plus d'administrateur : sauvegardes, mises à jour de sécurité et droits d'accès ne sont plus assurés à partir du 1er janvier. Nouveau risque pour le secret professionnel. L'outil ne doit pas dépendre de ce serveur. Non dit : ce que le contrat couvre (logiciel de gestion, Microsoft 365, postes), l'état des sauvegardes, qui détient les accès administrateur, la date de choix du remplaçant. |

_Relances non prévues : la question sur le volume (HS-a → R3) et celle sur l'accès (HS-b, HS-c → R8) ont dû être reformulées après réponse hors sujet du bot. Réponse surprenante à relancer : le registre existe (matière, issue, nom de fichier) mais la recherche prend quand même « trente minutes »._

### Boussole — ce que j'ai déjà obtenu

🟢 obtenu · 🟠 partiel / à vérifier · 🔴 à obtenir · ⬜ pas demandé (→ §3)

| Information | Statut | Réponse n° |
|---|---|---|
| Besoin réel (≠ demande exprimée) | 🟢 Deux besoins : retrouver le savoir interne (décisions du cabinet) et arrêter de réécrire les courriers. Ordre non tranché, la recherche semble prioritaire. | R1, R2, R9, R10 |
| Processus actuel | 🟢 Décisions : recherche par nom de fichier ou par la mémoire d'un collègue. Courriers : copier-coller, assistantes préparent, l'avocat relit et signe. | R1, R2 |
| Données : existence | 🟢 Environ 2 000 décisions, un registre, des milliers de courriers archivés. | R3, R13 |
| Données : volume | 🟢 2 000 décisions (15 ans), environ 15 courriers/jour, environ 10 recherches/jour. | R3, R10 |
| Données : qualité | 🟠 PDF et Word, anciens scans peu lisibles (part inconnue). Registre : extrait non représentatif, juridiction douteuse, couverture inconnue. | R3, R13 |
| Données : extrait obtenu | 🟠 Registre de 19 lignes reçu. Aucune décision ni courrier. | R13 |
| Données personnelles / confidentialité | 🟢 Clients, parties adverses, salariés, enfants, non anonymisées. Secret professionnel sur tous les dossiers. | R4, R8 |
| Critère de succès chiffré | 🟠 Gain d'une heure par jour et par avocat, moins d'une minute par recherche. Pas de situation de départ mesurée ni de seuil de fiabilité. | R5, R9 |
| Coût d'une erreur | 🟢 Responsabilité professionnelle et personnelle devant le Barreau, exigence de vérifiabilité. Non chiffré. | R7, R8 |
| Erreurs tolérées (chiffre) | 🟠 « Jamais » pour une décision inventée, « tout doit être vérifiable ». Aucun taux chiffré. | R7 |
| Utilisateurs | 🟠 Avocats et assistantes cités, usage réel de l'outil non précisé. | R2, R8 |
| Validation humaine / qui décide | 🟠 Courriers : l'avocat relit et signe. Décisions retrouvées : qui vérifie, non dit. | R2, R7 |
| SI / hébergement | 🟠 Pas de cloud américain, hébergeur français envisageable. Logiciel de gestion hébergé en France (nom inconnu), Microsoft 365, serveur de fichiers au cabinet. **Imprévu : le prestataire informatique s'arrête au 31/12, serveur sans administrateur ensuite, remplaçant non choisi.** Sauvegarde et accès administrateur inconnus. | R6, R14, imprévu |
| Budget | 🟢 15 000 € au démarrage, quelques centaines d'euros par mois. Périmètre et fermeté non précisés. | R11 |
| Délai | 🟢 Fiable dans six mois, pas d'urgence. | R12 |
| Ce qui a déjà été essayé | ⬜ Pas demandé | — |

## 3. Après — ce que je n'ai pas pu demander → questions ouvertes

| Je n'ai pas pu demander / pas eu de réponse claire | Pourquoi c'est important | → §6 du cadrage |
|---|---|---|
| Le registre contient-il toutes les décisions ? À jour ? | Détermine si les étiquettes existantes couvrent les 2 000 décisions. | Question ouverte |
| Part des décisions en scan papier | Coût de numérisation et délai, budget de 15 000 €. | Question ouverte |
| Contenu réel et lisibilité des décisions (aucune décision reçue) | Qualité des données estimée à l'aveugle. | Question ouverte |
| Les avocats consultent-ils le registre aujourd'hui ? Pourquoi la recherche prend-elle 30 min malgré lui ? | Sépare deux causes : registre ignoré ou insuffisant. | Question ouverte |
| Temps de rédaction d'un courrier type | Sans lui, le KPI « 1 h/jour/avocat » n'est pas vérifiable côté courriers. | Question ouverte |
| Mesure du temps de recherche actuel (30 min : mesuré ou estimé ? fréquence) | Situation de départ des KPI. | Question ouverte |
| Droits d'accès des assistantes, journal des accès | Secret professionnel : risque rouge (accès ouvert entre avocats). | Question ouverte |
| Nom du logiciel de gestion de cabinet et ses possibilités d'intégration | Architecture (intégration). | Question ouverte |
| Microsoft 365 et refus du « cloud américain » : compatibles ? | Périmètre de la contrainte d'hébergement. | Question ouverte |
| Garanties « sérieuses » attendues d'un hébergeur | Contrat, conformité, choix d'hébergement. | Question ouverte |
| Ce que couvrent les 15 000 € ; budget ferme ou indicatif | Périmètre de la solution. | Question ouverte |
| Arbitrage définitif entre courriers et recherche | Périmètre de la première version. | Question ouverte |
| Seuil de fiabilité attendu (taux de bonnes décisions retrouvées) | KPI et seuil d'acceptabilité. | Question ouverte |
| Types de données sensibles dans les affaires familiales (art. 9) | Base légale RGPD et hébergement. | Question ouverte |
| Raison du non-envoi des décisions | Confirmer l'hypothèse du secret professionnel. | Question ouverte |
| Ce qui a déjà été essayé | Éviter de répéter un essai abandonné. | Question ouverte |
| Existe-t-il une sauvegarde du serveur, testée ? | Sans elle, risque de perte ou de blocage des décisions dès le 1er janvier. | Question ouverte, §6 |
| Qui détient les accès administrateur ? Le prestataire sortant a-t-il des accès à révoquer ? | Secret professionnel et sécurité après la fin du contrat. | Question ouverte, §6 |
| Le contrat qui s'arrête couvre-t-il aussi le logiciel de gestion, Microsoft 365 et les postes ? | Étendue de l'impact de l'imprévu. | Question ouverte, §6 |
| Quand le nouveau prestataire sera-t-il choisi ? | Calendrier : aucun branchement technique avant. | Question ouverte, §6 |
| Copie chiffrée chez un hébergeur français ou déplacement de tout le serveur ? | Arbitrage entre une seconde copie des décisions et la dépendance à un serveur sans administrateur. | Question ouverte, §6 |
| Le coût du nouveau prestataire est-il hors du budget de 15 000 € ? | Périmètre du budget après l'imprévu. | Question ouverte, §6 |