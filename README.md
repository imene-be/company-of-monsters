# Company of Monsters

Petit combat de monstres en Java, pour s'exercer à la programmation orientée objet : classe abstraite, héritage et polymorphisme.

## Le principe

Trois types de monstres s'affrontent au tour par tour dans une arène. Chaque monstre démarre avec **40 points de vie** et une valeur d'attaque. Les types se contrent comme dans un jeu de pierre, feuille, ciseaux : une attaque contre un type faible inflige **le double de dégâts**.

| Type | Fort contre |
|---|---|
| Feu | Air |
| Eau | Feu |
| Air | Eau |

## Structure

```
CompanyOfMonster/
  Monster.java        classe abstraite : nom, attaque, vie, type, état KO
  FireMonster.java    monstre de feu
  WaterMonster.java   monstre d'eau
  AirMonster.java     monstre d'air
  Arena.java          point d'entrée : organise le combat
```

Chaque type hérite de `Monster` et redéfinit la méthode `attack`, qui applique le bonus de dégâts selon le type de l'adversaire.

## Lancer le combat

Java 17 ou plus récent est recommandé.

```bash
git clone https://github.com/imene-be/company-of-monsters.git
cd company-of-monsters/CompanyOfMonster
javac *.java
java Arena
```

Dans `Arena`, un dragon de feu affronte une grenouille d'eau. Le combat se déroule tour par tour jusqu'à ce qu'un des deux soit KO, puis le gagnant est annoncé.

## Concepts illustrés

- Classe abstraite et méthode abstraite
- Héritage et redéfinition de méthode
- Encapsulation (attributs privés, accesseurs)
- Boucle de jeu et conditions d'arrêt

---

Réalisé par [Imène Bentifraouine](https://imenebe.fr).
