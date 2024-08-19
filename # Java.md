# Java
## Mes premier pas
1. je cree un fichier java
2. j'ecrit du code java
```java
   public class Main {
    public static void main(String[]args){
        System.out.println("bonjour à tous ");
    }
}
```
3. je lance la commande : javac Main.java
4. le fichier Main.class est cree
5. je compile avec la commande:java Main

### C’est quoi le mécanisme
Chaque ligne de code exécutée en Java doit se trouver dans un fichier class. Dans notre exemple, nous avons nommé la classe Main. Une Class doit toujours commencer par une première lettre majuscule.
Remarque : Java est sensible à la casse : `« MyClass »` et `« myclass »` ont des significations différentes. Le nom du fichier Java doit correspondre au nom de la classe.  Lors de l'enregistrement du fichier, enregistrez-le en utilisant le nom de la classe et ajoutez ".java" à la fin du nom de fichier.
La méthode principale
La main() méthode est obligatoire et vous la verrez dans chaque programme Java

## Variables
les varables permettent de stocker dans un emplacement memoire les données  et de les transformer en utilisant des opérateurs.
pour declarer une variable , je dois d'abord definir le type de la variable en suite le nom de la variable .si je souhaite ne plus reassigné de valeur à la variable je dois le faire precede du mot cle `final`.
Il existe plusieurs type de variable entre autre : int , foat(nombre à virgule) , char , boolean ,string;
les types de données sont divisé en deux groupe
1. les types de données primitifs (byte,int,long, float , double , boolean et les char )
2. les types non primitifs tel que string les arrays et les classes
le type est different de la taille
byte =>1byte
short => 2bytes
int => 4bytes
char => 2bytes

les types de données non primitifs sont appelé types  de reference car ils font référence à des objets.
la difference
- les types non primitif commence par une lettre en majiscule tansdisque le type primitif par une lettre minuscule

**NB** : en dehors d'une methode les variables sont considere comme des variables d'instance .et dans une methode elles sont des variables locales
### les types primitifs
il y a 8 types de données primitifs .
on a :
byte => 1 octet => 8bits => -128 à 127
short =>2 octet => 16bits => -32 768 à 32 767
int => 4 octet => 32bits => -2 147 483 648 à 2 147 483 647.
long =>8 octet => 64 bits => -9 223 372 036 854 775 808 à 9 223 372 036
float => 4 octet => 32bits => 6 à 7 chiffres décimaux
double => 8 octet =>64bits =>  15 chiffres décimaux
boolaen => 1octet => 1bit => vrai ou faux
char => 2octets => 16bit => stocke les carectere ou les valeurs ascii

### les differences entre les variables primitifs  et non primitifs
1. Les types primitifs sont prédéfinis (déjà définis) en Java. Les types non primitifs sont créés par le programmeur et ne sont pas définis par Java (à l'exception de String).
2. Les types non primitifs peuvent être utilisés pour appeler des méthodes afin d'effectuer certaines opérations, tandis que les types primitifs ne le peuvent pas.
3. Un type primitif a toujours une valeur, tandis que les types non primitifs peuvent être nuls.
4. Un type primitif commence par une lettre minuscule, tandis que les types non primitifs commencent par une lettre majuscule
```java
public class PrimitiveExample {
    // Déclaration de variables primitives sans initialisation explicite
    byte aByte;
    short aShort;
    int anInt;
    long aLong;
    float aFloat;
    double aDouble;
    char aChar;
    boolean aBoolean;

    public void printDefaults() {
        // Affichage des valeurs par défaut
        //sans meme affecter de valeur au differentes variables , nous avons quand  des valeur par defaut
        System.out.println("byte par défaut : " + aByte); // 0
        System.out.println("short par défaut : " + aShort); // 0
        System.out.println("int par défaut : " + anInt); // 0
        System.out.println("long par défaut : " + aLong); // 0L
        System.out.println("float par défaut : " + aFloat); // 0.0f
        System.out.println("double par défaut : " + aDouble); // 0.0d
        System.out.println("char par défaut : '" + aChar + "'"); // '\u0000' (caractère nul)
        System.out.println("boolean par défaut : " + aBoolean); // false
    }
}

//Dans le cas des variables non primitifs

public class NonPrimitiveExample {
    // Déclaration de variables non primitives sans initialisation explicite
    String aString;
    Integer anInteger;
    int[] anArray;
    ArrayList<String> aList;

    public void printDefaults() {
        // Affichage des valeurs par défaut
        System.out.println("String par défaut : " + aString); // null
        System.out.println("Integer par défaut : " + anInteger); // null
        System.out.println("Tableau int[] par défaut : " + anArray); // null
        System.out.println("ArrayList<String> par défaut : " + aList); // null
    }
}
```
## Convertion de type ou Type Casting
### widening Casting
quand on fait du widening casting c'est une conversion vers un type plus grand
```java
    public static void main(String[]args){

        int myvar  = 9;
        double mydouble = myvar;
        System.out.println(myvar);// 9
        System.out.println(mydouble);//9.0
    }
```
### Narrowing Casting (explicite)
Faire narrowing casting c'est convertir un type plus grand en un type plus petit
```java
    public static void main(String[]args){

        double myvar  = 9;
        int mydouble =(double) myvar; // narrowing
        System.out.println(myvar);// 9
        System.out.println(mydouble);//9.0
    }
```
## Opérateurs
**Opérateurs de logique**
&& => Renvoie vrai si les deux déclarations sont vraies
||=> Renvoie vrai si l'une des déclarations est vraie
! => Inverse le résultat, renvoie false si le résultat est vrai

**Opérateurs de comparaison**
- en java nous n'avons pas de tripe egalité
**Opérateur d'affectation**
les habituelles

### Exercice 1 : Déclaration et taille des variables
**Objectif :** Pratiquer la déclaration de différentes variables et comprendre leurs tailles en mémoire.

- **Énoncé :** Déclarez des variables de différents types primitifs (`byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`) et affichez leurs tailles respectives en octets.

- **Indications :**
  - Utilisez la méthode `System.out.println()` pour afficher la taille des types primitifs.
  - Par exemple, pour obtenir la taille d'un type `int`, utilisez `System.out.println("Taille de int : " + Integer.BYTES + " octets");`.

### Exercice 2 : Concaténation et comparaison de chaînes de caractères
**Objectif :** Travailler avec la concaténation et les opérateurs de comparaison.

- **Énoncé :** Déclarez deux chaînes de caractères `str1` et `str2`. Concaténez-les pour obtenir une troisième chaîne `str3`. Comparez `str1` et `str2` à l'aide des opérateurs de comparaison (`==`, `equals()`) et affichez les résultats.

- **Indications :**
  - Utilisez l'opérateur `+` pour la concaténation.
  - Pour comparer les chaînes, utilisez à la fois `==` et `equals()`.
  - Affichez les résultats des comparaisons pour montrer la différence entre `==` et `equals()`.

### Exercice 3 : Opérateurs logiques et d'affectation
**Objectif :** Utiliser des opérateurs logiques et d'affectation dans des expressions conditionnelles.

- **Énoncé :** Déclarez trois variables entières `a`, `b`, et `c`. Utilisez les opérateurs d'affectation pour initialiser `b` et `c` avec des valeurs calculées à partir de `a`. Utilisez les opérateurs logiques pour créer une condition qui vérifie si `a` est supérieur à `b` ET `b` est inférieur à `c`. Affichez le résultat.

- **Indications :**
  - Utilisez des expressions comme `b = a + 2;` et `c = b * 2;`.
  - Utilisez l'opérateur `&&` pour l'opération logique.
  - Affichez un message comme "La condition est vraie" ou "La condition est fausse".

### Exercice 4 : Conversion de types (Widening et Narrowing)
**Objectif :** Mettre en pratique la conversion de types entre différentes tailles.

- **Énoncé :** Déclarez une variable entière `intVar` et affectez-lui une valeur. Effectuez une conversion widening pour convertir `intVar` en `double`, et une conversion narrowing pour convertir `doubleVar` en `short`. Affichez les résultats après chaque conversion.

- **Indications :**
  - Utilisez `doubleVar = intVar;` pour le widening.
  - Utilisez `shortVar = (short) doubleVar;` pour le narrowing.
  - Affichez les valeurs avant et après chaque conversion.

### Exercice 5 : Comparaison de valeurs et opérations combinées
**Objectif :** Combiner les notions d'opérateurs de comparaison, d'affectation et de logique.

- **Énoncé :** Déclarez deux variables `x` et `y` de types différents (`int` et `float`). Comparez-les après avoir effectué une conversion (widecasting ou narrowing) pour rendre leur comparaison possible. Utilisez un opérateur de comparaison pour vérifier si `x` est supérieur à `y` après conversion, et affichez le résultat.

- **Indications :**
  - Par exemple, effectuez une conversion de `x` en `float` pour le comparer à `y`.
  - Utilisez `>` pour comparer les valeurs et affichez "x est supérieur à y" ou "x n'est pas supérieur à y".


## Structure de controles
Les strutures de controles , nous aident à prendre des decisions si une condition est vérifiée
- if , if else
- l'opérateur ternaire :(condition)?expressionVrai : expressionFausse
- switch
  ```java
    String langue  = "Fr";
        switch (langue) {
            case "Fr":
                System.out.println("France");
                break;//permet de sortir des que le cas est verifé
            case "US":
                System.out.println("USA");
                break;

            default:// quand aucun cas n'est verifier
                break;
        }

  ```

  ## Exercice
  ### Exercice 1 : Vérification d'un nombre pair ou impair
**Objectif :** Utiliser les conditions simples et l'opérateur ternaire pour vérifier si un nombre est pair ou impair.

- **Énoncé :** Écrivez un programme qui prend un nombre entier en entrée et utilise une condition ternaire pour déterminer si le nombre est pair ou impair. Affichez un message indiquant "Le nombre X est pair" ou "Le nombre X est impair", où X est le nombre saisi.

- **Indications :**
  - Utilisez l'opérateur `%` pour vérifier si un nombre est divisible par 2.
  - Utilisez l'opérateur ternaire pour simplifier la condition.

### Exercice 2 : Comparaison de trois nombres
**Objectif :** Pratiquer les conditions imbriquées pour trouver le plus grand de trois nombres.

- **Énoncé :** Écrivez un programme qui prend trois nombres en entrée et détermine lequel est le plus grand. Utilisez des conditions imbriquées pour faire cette comparaison.

- **Indications :**
  - Utilisez des conditions `if-else` pour comparer les trois nombres.
  - Affichez "Le plus grand nombre est : X", où X est le plus grand des trois nombres.

### Exercice 3 : Classification des âges
**Objectif :** Utiliser les conditions multiples pour classer les âges dans différentes catégories.

- **Énoncé :** Écrivez un programme qui prend l'âge d'une personne en entrée et détermine sa catégorie :
  - "Enfant" pour les âges de 0 à 12 ans.
  - "Adolescent" pour les âges de 13 à 19 ans.
  - "Adulte" pour les âges de 20 à 64 ans.
  - "Sénior" pour les âges de 65 ans et plus.

- **Indications :**
  - Utilisez des conditions `if-else if-else` pour gérer les différentes catégories.
  - Affichez la catégorie correspondante.

### Exercice 4 : Calcul de la note finale
**Objectif :** Utiliser une condition ternaire pour déterminer la réussite ou l'échec d'un étudiant.

- **Énoncé :** Écrivez un programme qui prend une note sur 100 en entrée et utilise une condition ternaire pour déterminer si l'étudiant a réussi ou échoué. La limite de réussite est fixée à 50. Affichez "Réussi" si la note est supérieure ou égale à 50, sinon affichez "Échoué".

- **Indications :**
  - Utilisez l'opérateur ternaire pour évaluer si la note est suffisante pour réussir.
  - Affichez le résultat.

### Exercice 5 : Calcul du prix avec remise
**Objectif :** Utiliser les conditions pour appliquer une remise en fonction du montant d'achat.

- **Énoncé :** Écrivez un programme qui prend un montant d'achat en entrée et applique une remise selon les règles suivantes :
  - Pas de remise si le montant est inférieur à 100.
  - 10% de remise si le montant est compris entre 100 et 500.
  - 20% de remise si le montant est supérieur à 500.

  Calculez et affichez le montant final après remise.

- **Indications :**
  - Utilisez des conditions `if-else` pour appliquer la bonne remise.
  - Affichez le montant final après remise.

## Boucles
Les boucles peuvent exécuter un bloc de code tant qu'une condition spécifiée est atteinte.
- while
- do while
  ```java
  do{
    // du code
  }while (condition)
  ```
- for

```java
 for( int i =0 ; i<10 ; i=i+2){
//code
 }

 //int i =0 => est exécutée (une fois) avant l'exécution du bloc de code
//i<10  => définit la condition d'exécution du bloc de code.
// i=i+2 =>est exécutée (à chaque fois) après l'exécution du bloc de code.
```
### Break and continue
Break : L' instruction break peut également être utilisée pour sortir d'une boucle .
continue : L' instruction continue interrompt une itération (dans la boucle), si une condition spécifiée se produit, et continue avec l'itération suivante dans la boucle.

## Exercice
### Exercice 1 : Affichage de nombres pairs
**Objectif :** Utiliser une boucle `for` pour afficher les nombres pairs entre 1 et 20.

**Énoncé :**
Écrivez un programme qui utilise une boucle `for` pour afficher tous les nombres pairs entre 1 et 20.

---

### Exercice 2 : Somme des entiers avec `while`
**Objectif :** Utiliser une boucle `while` pour calculer la somme des entiers de 1 à 10.

**Énoncé :**
Écrivez un programme qui utilise une boucle `while` pour calculer et afficher la somme des entiers de 1 à 10.

---

### Exercice 3 : Inverser un nombre avec `do-while`
**Objectif :** Utiliser une boucle `do-while` pour inverser les chiffres d'un nombre.

**Énoncé :**
Écrivez un programme qui prend un nombre entier en entrée et utilise une boucle `do-while` pour inverser ses chiffres. Par exemple, pour le nombre `1234`, le programme doit afficher `4321`.

---

### Exercice 4 : Trouver le maximum d'une série d'entiers
**Objectif :** Utiliser une boucle `for` pour trouver le plus grand nombre dans une série de nombres donnés par l'utilisateur.

**Énoncé :**
Écrivez un programme qui demande à l'utilisateur d'entrer 5 nombres entiers. Utilisez une boucle `for` pour trouver et afficher le plus grand de ces nombres.

---

### Exercice 5 : Compter les chiffres pairs dans un nombre
**Objectif :** Utiliser une boucle `while` pour compter le nombre de chiffres pairs dans un nombre donné.

**Énoncé :**
Écrivez un programme qui prend un nombre entier en entrée et utilise une boucle `while` pour compter combien de chiffres pairs il contient. Par exemple, pour `123456`, le programme doit afficher `3`.

## Les tableaux
Les tableaux sont utilisés pour stocker plusieurs valeurs dans une seule variable
```java
String[]car = {"toyota","citoen","bugati","audi"} ;
car = new String[] {"toyota", "citroen", "bugatti", "audi"};
String[] car = new String[4];
        car[0] = "toyota";
        car[1] = "citroen";
        car[2] = "bugatti";
        car[3] = "bugatti1";



// for each
for (String string : car) {
    System.out.println(string);
}
//for
   for (int i = 0; i < car.length; i++) {
       System.out.println(car[i]);
   }
// affichage litteral
 System.out.println(Arrays.toString(car));

```

## Exercice



### Exercice 1 : Trier un tableau d'entiers

**Objectif :** Trier un tableau d'entiers en ordre croissant.

**Énoncé :**
Écrivez un programme qui crée un tableau d'entiers non triés, puis utilise `Arrays.sort()` pour trier le tableau en ordre croissant et affiche le tableau trié.

**Exemple :**
Pour le tableau `{5, 2, 9, 1, 5, 6}`, le programme doit afficher `{1, 2, 5, 5, 6, 9}`.

---

### Exercice 2 : Filtrer les éléments pairs d'un tableau

**Objectif :** Filtrer et afficher uniquement les éléments pairs d'un tableau d'entiers.

**Énoncé :**
Écrivez un programme qui crée un tableau d'entiers et utilise une boucle pour filtrer et afficher uniquement les nombres pairs.

**Exemple :**
Pour le tableau `{1, 2, 3, 4, 5, 6}`, le programme doit afficher `2, 4, 6`.

---

### Exercice 3 : Trouver le maximum et le minimum d'un tableau

**Objectif :** Trouver et afficher le plus grand et le plus petit nombre dans un tableau d'entiers.

**Énoncé :**
Écrivez un programme qui crée un tableau d'entiers, puis utilise une boucle pour trouver et afficher le plus grand et le plus petit nombre dans le tableau.

**Exemple :**
Pour le tableau `{3, 5, 7, 2, 8}`, le programme doit afficher `Max: 8, Min: 2`.

---

### Exercice 4 : Rechercher un élément dans un tableau trié

**Objectif :** Rechercher un élément dans un tableau trié en utilisant la recherche binaire.

**Énoncé :**
Écrivez un programme qui crée un tableau d'entiers triés, puis demande à l'utilisateur d'entrer un nombre. Utilisez `Arrays.binarySearch()` pour rechercher le nombre dans le tableau et afficher sa position.

**Exemple :**
Pour le tableau `{1, 3, 5, 7, 9}` et la recherche du nombre `7`, le programme doit afficher `Index: 3`.

---

### Exercice 5 : Supprimer les doublons d'un tableau

**Objectif :** Supprimer les éléments dupliqués d'un tableau et afficher le tableau sans doublons.

**Énoncé :**
Écrivez un programme qui crée un tableau d'entiers avec des doublons. Utilisez un `Set` pour éliminer les doublons, puis convertissez-le en tableau et affichez le tableau sans doublons.

**Exemple :**
Pour le tableau `{1, 2, 2, 3, 4, 4, 5}`, le programme doit afficher `1, 2, 3, 4, 5`.

## Methodes
Une méthode est un bloc de code qui ne s'exécute que lorsqu'elle est appelée.

### comment créé une methode
une methode doit etre déclaré dans une classe .
```java
public class Main {
  static void myMethod(){
    //code
  }
}
```
- `Static` signifie que la méthode appartient à la classe Main et non à un objet de la classe Main.
- `myMethod()` est le nom de la méthode
- `void` signifie que cette méthode n'a pas de valeur de retour.
### comment l'utiliser ?
```java
public class Main {
    // dans ce exemple nous avons abordé la notion de surcharge
    /**
     * sans parametre
     * sans valeur de retour
     */
  static void myMethod(){
    System.out.println("bonjour")
  }
  /**
   * avec parametre
   * sans valeur de retour
   */
  static void myMethod(String nom){
    System.out.println("bonjour"+ nom);
  }

  static int myMethod(String nom){
    System.out.println("bonjour"+ nom);
     return nom.length();
  }

   public static void main(String[]args){
    myMethod();
   }
}
```
### Surcharge de fonction
plusieurs méthodes peuvent avoir le même nom avec des paramètres différents.

**signature de fonction** :  la signature d'une méthode (ou fonction) est une partie essentielle de sa définition qui permet d'identifier de manière unique une méthode au sein d'une classe

signature = nom de la methode + liste des parametres

elle ne tient pas compte du type de retour , de la visibilité ,des exceptions ou encore des modificateurs de methodes

### Exercice

### Exercice 1 : Méthode de Calcul de la Somme

**Objectif :** Définir une méthode pour calculer la somme de deux entiers.

**Énoncé :**
Écrivez une méthode `sum(int a, int b)` qui retourne la somme de deux entiers. Appelez cette méthode depuis la méthode `main` avec différents paramètres et affichez les résultats.

**Exemple :**
Pour les entrées `5` et `7`, le résultat doit être `12`.

---

### Exercice 2 : Méthode de Vérification de Parité

**Objectif :** Définir une méthode pour vérifier si un nombre est pair ou impair.

**Énoncé :**
Écrivez une méthode `isEven(int number)` qui retourne `true` si le nombre est pair et `false` sinon. Utilisez cette méthode dans la méthode `main` pour vérifier plusieurs nombres.

**Exemple :**
Pour l'entrée `4`, le résultat doit être `true`. Pour l'entrée `7`, le résultat doit être `false`.

---

### Exercice 3 : Méthode de Calcul de la Factorielle

**Objectif :** Définir une méthode pour calculer la factorielle d'un nombre entier positif.

**Énoncé :**
Écrivez une méthode `factorial(int n)` qui retourne la factorielle de `n`. La factorielle de `n` (notée `n!`) est le produit de tous les entiers de 1 à `n`. Testez cette méthode avec différents nombres dans la méthode `main`.

**Exemple :**
Pour l'entrée `5`, le résultat doit être `120`.

---

### Exercice 4 : Méthode de Surcharge

**Objectif :** Pratiquer la surcharge de méthodes.

**Énoncé :**
Écrivez une classe `Calculator` avec plusieurs méthodes `multiply` :
1. `multiply(int a, int b)` qui retourne le produit de deux entiers.
2. `multiply(double a, double b)` qui retourne le produit de deux nombres à virgule flottante.

Testez ces méthodes dans la méthode `main`.

**Exemple :**
Pour les entrées `3` et `4` dans la première méthode, le résultat doit être `12`. Pour les entrées `3.5` et `4.2` dans la seconde méthode, le résultat doit être `14.7`.

---

### Exercice 5 : Méthode de Manipulation de Chaînes

**Objectif :** Définir une méthode qui retourne la chaîne inversée.

**Énoncé :**
Écrivez une méthode `reverseString(String str)` qui retourne la chaîne de caractères inversée. Utilisez cette méthode dans `main` pour inverser plusieurs chaînes.

**Exemple :**
Pour l'entrée `"hello"`, le résultat doit être `"olleh"`.