# Schéma d'architecture cible — Cabinet Maître Devalle

```mermaid
flowchart LR
    subgraph FR["Hébergement en France, accès authentifié"]
        SRC[("Serveur du cabinet<br/>décisions + registre")]
        PREP["Préparation<br/>reconnaissance de texte des scans<br/>+ rattachement au registre"]
        IDX[("Index de recherche<br/>texte des décisions + filtres du registre")]
        UI["Interface de recherche<br/>avocats et assistantes"]
        MOD[("Bibliothèque de courriers types<br/>validés et à jour")]
        DRAFT["Assemblage du brouillon de courrier"]
        LOG[("Journal des consultations<br/>+ indicateurs")]
    end

    SRC --> PREP --> IDX
    UI -->|"question"| IDX
    IDX --> S{"Résultat trouvé<br/>et texte lisible ?"}
    S -->|"oui"| RES["Liste de décisions réelles<br/>avec lien vers l'original"]
    S -->|"non ou scan illisible"| MAN["Message clair : aucun résultat n'est<br/>pas une preuve d'absence<br/>+ recherche manuelle via le registre"]
    RES --> AV["Vérification par l'avocat"]
    MAN --> AV

    UI -->|"demande de courrier"| DRAFT
    MOD --> DRAFT
    DRAFT --> REL["Relecture, correction et signature<br/>par l'avocat"]
    DRAFT -.->|"intégration à préciser"| WORD["Word (Microsoft 365)<br/>et logiciel de gestion du cabinet"]

    UI --> LOG
    IDX --> LOG
```

**Composants**
1. **Serveur du cabinet** : source unique des décisions et du registre, déjà existant. Rien n'est envoyé hors de France.
2. **Préparation** : transforme les anciens scans en texte lisible (reconnaissance automatique de texte) et rattache chaque décision à sa ligne du registre (matière, date, issue).
3. **Index de recherche** : un moteur de recherche dans le texte des documents, combiné aux filtres du registre. Il ne renvoie que des documents qui existent.
4. **Interface de recherche** : accès par identifiant pour les avocats et assistantes. Chaque résultat ouvre le document d'origine.
5. **Bibliothèque de courriers types** : modèles à jour, validés par un avocat, à la place des vieux courriers copiés-collés. L'assemblage remplit un brouillon que l'avocat relit et signe.
6. **Journal et indicateurs** : trace des consultations (secret professionnel) et mesure du temps de recherche et du taux de décisions retrouvées (§6).

**Où les risques 🔴 sont traités**
- **Décision inventée** : l'index ne renvoie que des documents réels, avec lien vers l'original. L'avocat vérifie (nœud « Vérification par l'avocat »).
- **Secret professionnel** : tout est dans le périmètre « hébergement en France, accès authentifié », et le journal garde la trace des consultations.
- **Données de tiers et de mineurs** : pas de copie vers un service externe ; droits d'accès par dossier ou par matière à trancher avec le cabinet (§6).
- **Scans mal lus** : le nœud « résultat trouvé et texte lisible ? » évite qu'un silence soit pris pour une absence.

**Ce qu'on n'a PAS mis (et pourquoi)**
- **Modèle de langage qui rédige ou cite des décisions** : c'est le risque d'invention que la cliente exclut (« jamais chez nous »).
- **Assistant qui répond en langage naturel à partir des documents (RAG) et base de recherche par sens** : autre produit, avec un coût et un risque d'erreur en plus, pas nécessaire tant que la recherche dans le texte suffit.
- **Agents qui agissent seuls** : rien ne doit s'envoyer sans l'avocat.
- **Modèle entraîné sur les décisions du cabinet** : aucune donnée d'entraînement à exposer, et 2 000 décisions sans thème étiqueté ne le justifient pas.
- **Service hébergé hors de France** : refusé par la cliente.

**Sobriété en 3 lignes** : recommandation de départ, une recherche dans le texte des documents du cabinet, avec ses filtres, et une bibliothèque de courriers types à jour. Aucun modèle de langage à ce stade : le besoin est de retrouver des documents réels, pas d'en générer. Condition de bascule : si un essai sur un échantillon montre que la recherche par mots ne retrouve pas la bonne décision dans un taux à fixer avec le cabinet, on envisagera une aide à la recherche par un modèle hébergé en France, sans qu'il produise de citation (à évaluer avec la grille C4).

**Cohérence avec les KPI** : le journal et les indicateurs mesurent les chiffres du §6 (temps de recherche, décisions retrouvées, temps de rédaction d'un courrier).

**Imprévu de 14h30** : _à compléter après le message du client._