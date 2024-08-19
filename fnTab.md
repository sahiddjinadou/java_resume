En Java, les tableaux sont des structures de données de base qui stockent des éléments de manière séquentielle. Bien que les tableaux eux-mêmes n'aient pas de méthodes intégrées comme les objets, Java fournit plusieurs méthodes utilitaires dans la classe `java.util.Arrays` pour manipuler les tableaux. Voici un aperçu des méthodes et opérations courantes disponibles pour les tableaux en Java :

### Méthodes Utilitaires de `java.util.Arrays`

1. **`Arrays.copyOf()`**
   - **Description :** Crée une copie d'un tableau avec une longueur spécifiée.
   - **Syntaxe :**
     ```java
     T[] Arrays.copyOf(T[] original, int newLength);
     ```
   - **Exemple :**
     ```java
     int[] original = {1, 2, 3};
     int[] copy = Arrays.copyOf(original, 5); // {1, 2, 3, 0, 0}
     ```

2. **`Arrays.copyOfRange()`**
   - **Description :** Copie une partie d'un tableau dans un nouveau tableau.
   - **Syntaxe :**
     ```java
     T[] Arrays.copyOfRange(T[] original, int from, int to);
     ```
   - **Exemple :**
     ```java
     int[] original = {1, 2, 3, 4, 5};
     int[] part = Arrays.copyOfRange(original, 1, 4); // {2, 3, 4}
     ```

3. **`Arrays.sort()`**
   - **Description :** Trie les éléments d'un tableau dans l'ordre naturel.
   - **Syntaxe :**
     ```java
     void Arrays.sort(T[] array);
     ```
   - **Exemple :**
     ```java
     int[] numbers = {3, 1, 4, 1, 5};
     Arrays.sort(numbers); // {1, 1, 3, 4, 5}
     ```

4. **`Arrays.binarySearch()`**
   - **Description :** Recherche une valeur dans un tableau trié et retourne son index.
   - **Syntaxe :**
     ```java
     int Arrays.binarySearch(T[] array, T key);
     ```
   - **Exemple :**
     ```java
     int[] numbers = {1, 2, 3, 4, 5};
     int index = Arrays.binarySearch(numbers, 3); // 2
     ```

5. **`Arrays.fill()`**
   - **Description :** Remplit toutes les positions d'un tableau avec une valeur spécifiée.
   - **Syntaxe :**
     ```java
     void Arrays.fill(T[] array, T value);
     ```
   - **Exemple :**
     ```java
     int[] numbers = new int[5];
     Arrays.fill(numbers, 7); // {7, 7, 7, 7, 7}
     ```

6. **`Arrays.equals()`**
   - **Description :** Compare deux tableaux pour vérifier s'ils sont égaux.
   - **Syntaxe :**
     ```java
     boolean Arrays.equals(T[] a, T[] b);
     ```
   - **Exemple :**
     ```java
     int[] a = {1, 2, 3};
     int[] b = {1, 2, 3};
     boolean isEqual = Arrays.equals(a, b); // true
     ```

7. **`Arrays.stream()`**
   - **Description :** Crée un flux (`Stream`) à partir d'un tableau.
   - **Syntaxe :**
     ```java
     Stream<T> Arrays.stream(T[] array);
     ```
   - **Exemple :**
     ```java
     int[] numbers = {1, 2, 3, 4, 5};
     Arrays.stream(numbers).forEach(System.out::println);
     ```

8. **`Arrays.asList()`**
   - **Description :** Convertit un tableau en une liste (`List`).
   - **Syntaxe :**
     ```java
     List<T> Arrays.asList(T... a);
     ```
   - **Exemple :**
     ```java
     String[] carArray = {"toyota", "citroen", "bugatti"};
     List<String> carList = Arrays.asList(carArray);
     ```

9. **`Arrays.hashCode()`**
   - **Description :** Retourne le code de hachage pour un tableau.
   - **Syntaxe :**
     ```java
     int Arrays.hashCode(T[] array);
     ```
   - **Exemple :**
     ```java
     int[] numbers = {1, 2, 3};
     int hashCode = Arrays.hashCode(numbers);
     ```

10. **`Arrays.deepToString()`**
    - **Description :** Retourne une chaîne de caractères représentant les éléments d'un tableau multidimensionnel.
    - **Syntaxe :**
      ```java
      String Arrays.deepToString(Object[] array);
      ```
    - **Exemple :**
      ```java
      int[][] matrix = {{1, 2}, {3, 4}};
      String matrixString = Arrays.deepToString(matrix); // "[[1, 2], [3, 4]]"
      ```

### Méthodes des Tableaux en Java

