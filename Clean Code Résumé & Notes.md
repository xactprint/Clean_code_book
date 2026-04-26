 # Clean Code — Résumé & Notes

> Un résumé concis de *Clean Code par Robert C. Martin (Uncle Bob)*

![Licence](https://img.shields.io/badge/license-MIT-green)
![Niveau](https://img.shields.io/badge/niveau-débutant--intermédiaire-blue)
![Sujet](https://img.shields.io/badge/sujet-clean--code-orange)

---

## À propos

Ce dépôt contient un **résumé clair et structuré** des chapitres clés du livre :

> **Clean Code : A Handbook of Agile Software Craftsmanship**  
> Auteur : Robert C. Martin

 Objectif : aider les développeurs à écrire un code **propre, lisible et maintenable**

---

## Table des matières

- [Noms significatifs](#-1-noms-significatifs-chapitre-2)
- [Fonctions](#-2-fonctions-chapitre-3)
- [Commentaires](#-3-commentaires-chapitre-4)
- [Objets & structures de données](#-4-objets--structures-de-données-chapitre-6)
- [Loi de Déméter](#-loi-de-déméter)
- [Conclusion](#-conclusion)

---

## 1. Noms significatifs (Chapitre 2)

Un bon nommage est essentiel en programmation.

✔ Un nom doit :
- Révéler l’intention  
- Être clair et non ambigu  
- Être facile à rechercher et à prononcer  

 À éviter :
- Noms trompeurs (`accountList` si ce n’est pas une liste)
- Noms à une lettre (sauf dans de petits contextes)

 Règles :
- Classes → **Noms (substantifs)**  
- Méthodes → **Verbes**

---

## 2. Fonctions (Chapitre 3)

Les fonctions doivent être :

✔ Petites  
✔ Focalisées  
✔ Faire **une seule chose**

 Bonnes pratiques :
- Moins de 20 lignes (idéalement)
- Même niveau d’abstraction

### Paramètres :
- 0 → Idéal  
- 1 → Bien  
- 2 → Acceptable  
- 3+ → À éviter  

Une fonction doit être :
- Soit une **commande**
- Soit une **requête**
- Pas les deux

---

## 3. Commentaires (Chapitre 4)

> « Les commentaires sont un mal nécessaire »

✔ Préférer le **code propre aux commentaires**

### Bons commentaires :
- Informations légales
- Explications complexes
- Décisions de conception

### Mauvais commentaires :
- Redondants
- Obsolètes
- Code commenté

 La vérité doit être dans le **code**, pas dans les commentaires.

---

## 4. Objets & structures de données (Chapitre 6)

### Objets :
- Cachent les données
- Exposent des comportements

### Structures de données :
- Exposent les données
- Peu ou pas de comportement

 Compromis :
- Procédural → facile d’ajouter des fonctions  
- POO → facile d’ajouter de nouvelles classes  

---

## Loi de Déméter

> « Parle à tes amis, pas aux étrangers »

 Éviter les chaînes profondes :

```js
obj.getA().getB().getC().doSomething(); // Mauvais
