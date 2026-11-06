# TP : Programmation Orientée Objet en C++

## Présentation générale

Ce TP regroupe trois exercices réalisés en **langage C++**, dans le cadre de l'apprentissage de la Programmation Orientée Objet (POO).

L'objectif principal est de maîtriser la **surcharge des constructeurs et la surcharge des méthodes**, tout en appliquant ces notions à des situations pratiques.

Les trois exercices ont été développés en C++, testés et exécutés correctement. Les fonctionnalités demandées ont été implémentées et vérifiées à travers des exemples dans la fonction `main()`.

---

## Technologies utilisées

- **Langage :** C++
- **Environnement de développement :** Eclipse
- **Bibliothèques :** `iostream`, `string`, `vector`
- **Paradigme :** Programmation Orientée Objet (POO)

---

## Exercice 1 : Gestion d'un carnet d'adresses avec surcharge de constructeurs

### Objectif

Créer une classe `Contact` permettant de représenter un contact dans un carnet d'adresses.

Cet exercice permet de comprendre le principe de la surcharge des constructeurs en C++.

### Fonctionnalités réalisées

La classe `Contact` contient trois attributs privés :

- `nom` : nom du contact.
- `telephone` : numéro de téléphone.
- `email` : adresse électronique.

Trois constructeurs surchargés ont été implémentés :

1. Un constructeur prenant uniquement le nom.
2. Un constructeur prenant le nom et le numéro de téléphone.
3. Un constructeur prenant le nom, le numéro de téléphone et l'adresse email.

Une méthode `afficher()` permet d'afficher toutes les informations du contact.

Lorsque certaines informations ne sont pas fournies, elles sont initialisées avec la valeur « Non disponible ».

### Tests et exécution

Plusieurs objets ont été créés avec les trois constructeurs afin de vérifier leur fonctionnement.

**Résultat :** les trois constructeurs fonctionnent correctement et chaque contact affiche les informations correspondant aux paramètres fournis.

---

## Exercice 2 : Système de facturation – Surcharge de méthodes

### Objectif

Créer une classe `Facture` permettant de gérer plusieurs articles et de calculer le montant total d'une facture.

Cet exercice permet de maîtriser la surcharge des méthodes et l'utilisation d'un tableau dynamique.

### Fonctionnalités réalisées

La classe `Facture` utilise une structure `Article` contenant :

- `nom` : nom de l'article.
- `prix` : prix unitaire.
- `quantite` : quantité achetée.
- `tva` : taux de TVA.

Les articles sont stockés dans un `std::vector`, qui permet d'ajouter dynamiquement plusieurs articles.

La méthode `ajouterArticle()` est surchargée en trois versions :

1. Avec le nom et le prix unitaire.
2. Avec le nom, le prix unitaire et la quantité.
3. Avec le nom, le prix unitaire, la quantité et le taux de TVA.

Des valeurs par défaut sont utilisées lorsque la quantité ou le taux de TVA ne sont pas fournis.

La méthode `afficherTotal()` permet de :

- Parcourir tous les articles.
- Calculer le montant hors taxes (HT).
- Calculer le montant toutes taxes comprises (TTC).
- Afficher les informations de chaque article.
- Calculer et afficher le total général de la facture.

### Tests et exécution

Plusieurs articles ont été ajoutés en utilisant les trois versions de `ajouterArticle()`.

Les calculs du montant TTC et du total général ont été vérifiés.

**Résultat :** les trois versions de la méthode fonctionnent correctement. Les articles sont enregistrés dans le tableau dynamique et le montant total de la facture est calculé et affiché correctement.

---

## Exercice 3 : Banque – Constructeurs surchargés et logique métier

### Objectif

Créer une classe `CompteBancaire` permettant de gérer un compte bancaire avec un solde et un code de sécurité.

Cet exercice permet d'appliquer la surcharge des constructeurs et des méthodes dans un contexte de gestion bancaire.

### Fonctionnalités réalisées

La classe `CompteBancaire` contient deux attributs privés :

- `solde` : montant disponible dans le compte.
- `codeSecurite` : code utilisé pour sécuriser les retraits.

Deux constructeurs surchargés ont été implémentés :

1. Un constructeur sans paramètre qui initialise le solde à zéro.
2. Un constructeur prenant un solde initial, avec vérification de sa validité.

La méthode `afficherSolde()` permet d'afficher le solde actuel du compte.

La méthode `retrait()` est surchargée en deux versions :

1. `retrait(double montant)` : effectue un retrait sans code de sécurité.
2. `retrait(double montant, int code)` : effectue un retrait après vérification du code de sécurité.

Des contrôles ont été ajoutés pour garantir le bon fonctionnement des opérations :

- Vérification que le montant du retrait est positif.
- Vérification que le solde est suffisant.
- Vérification du code de sécurité pour le retrait sécurisé.

Le solde est modifié uniquement lorsque toutes les conditions nécessaires sont respectées.

### Tests et exécution

Plusieurs scénarios ont été testés :

- Création d'un compte sans solde initial.
- Création d'un compte avec un solde initial.
- Retrait avec montant uniquement.
- Retrait avec montant et code correct.
- Tentative de retrait avec un code incorrect.

**Résultat :** les constructeurs et les deux versions de la méthode `retrait()` fonctionnent correctement. Les vérifications empêchent les opérations invalides et le solde reste inchangé lorsqu'un retrait est refusé.

---

## Bilan général

Ce TP a permis de mettre en pratique plusieurs notions fondamentales de la Programmation Orientée Objet en C++ :

- La création de classes et d'objets.
- L'encapsulation avec les attributs privés.
- La surcharge des constructeurs.
- La surcharge des méthodes.
- L'utilisation de `std::vector` pour gérer des données dynamiques.
- Les conditions et les vérifications avec `if / else`.
- La manipulation et le calcul des données.

## Conclusion

Les trois exercices ont été réalisés en **C++** et exécutés avec succès dans l'environnement Eclipse.

Les tests effectués ont permis de vérifier le bon fonctionnement des différentes fonctionnalités demandées. Les constructeurs surchargés, les méthodes surchargées, la gestion des articles et les opérations bancaires répondent correctement aux scénarios prévus.

Ce travail a permis de renforcer la compréhension de la surcharge en C++ et son utilisation dans des applications pratiques de Programmation Orientée Objet.

**Statut du TP : Réalisé et testé avec succès.**
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/41523e44-154f-43b1-9801-652e92881d66" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/b69f8944-351a-4c00-a5f3-82665d48ea03" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/0d8d8d34-0646-447e-b011-d9390b344056" />
