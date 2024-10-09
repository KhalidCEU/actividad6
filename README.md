## Actividad 6


### 1.3 El preincremento y el posincremento

**P:** Explique la diferencia entre pre-incremento y el pos-incremento.

**R:** La diferencia entre pre-incremento y el pos-incremento es:

- En el **pre-incremento** primero **incrementamos** el valor de la variable y luego la **evaluamos**.

    Por ejemplo, en este caso hacemos un pre-incremento de la variable **i**:
```
    int i = 0;
    int preIncremento = ++i;
    System.out.println("El valor de i es " + i);
    System.out.println("El resultado de su pre-incremento es " + preIncremento);

    // Output:
    //  El valor de i es 1
    //  El resultado de su pre-incremento es 1

```

- En el **pos-incremento** esto sucede al revés, primero **evaluamos** la variable y luego **incrementamos** su valor.

    Por ejemplo, en este caso hacemos un pos-incremento de la variable **i**:

```
    int i = 0;
    int posIncremento = i++;
    System.out.println("El valor de i es " + i);
    System.out.println("El resultado de su pos-incremento es " + posIncremento);

    // Output:
    //  El valor de i es 1
    //  El resultado de su pos-incremento es 0;
```


### 1.4 Bucles y arrays


**Ejercicio 20.1**


**P:** Explique el siguiente código

```
    public class Principal {
        public static void main(String[] args)
        {
            int i = 1;
            while(i <= 10) System.out.println(i++);
        }
    }
```

**R:**
En este código que se ejecuta directamente en la funcion **main** (punto de entrada del programa), perteneciente a la clase **Principal**, lo que ocurre es lo siguiente:

1. Inicializamos una **variable i** con un **valor de 1**
2. Usamos un bucle "**while**" que se **ejecutará** mientras que la condición que le hemos dado sea verdadera (es decir mientras que el valor de i sea menor o igual a 10)
3. En cada iteración de este while, se ejecutará un **println** del **posincremento** de esta variable. Al ser un posincremento, primero se hará el print del valor de i y después se incrementará

Con lo cual obtendremos como output una lista del 1 al 10 (separada por saltos de línea)

<br>

---

<br>

**Ejercicio 20.2**

**P:** Explique el siguiente código

```
    public class Principal {
        public static void main(String[] args)
        {
            for(int i = 1; i <= 10; i++) System.out.println(i);
        }
    }
```

**R:**
Este código nos dará el mismo resultado que la anterior, solo que se utiliza un bucle de tipo "**for**".
A diferencia del while, en el for :

1. Definimos e inicializamos directamente la variable i con un valor de 1 (```int i = 1```)
2. Ponemos la condición bajo la cual debe ejecutarse el for    (```ì <= 10```)
3. Incrementamos el valor de la variable i en cada iteración (```ì++```)
4. Dentro de este for, hacemos un **println** del valor de **i**

PS:  Aquí ya que incrementamos el valor de i dentro del **for**, nos basta con hacer ```...println(i)``` y no ```...println(i++)``` como hicimos en el caso del while (donde el valor se imprime antes del incremento).

Obtendremos como resultado lo mismo que en el caso anterior, una lista del 1 al 10 separada por saltos de línea.

<br>

---

<br>

**Ejercicio 20.3**

**P:** Explique el siguiente código

```
    public class Principal{
        public static void main(String[] args)
        {
            System.out.println("Ejecutándose primer bucle while...");
            int i = 1;
            while(i <= 10) System.out.println(i++);

            System.out.println("Ejecutándose primer bucle do-while...");
            i = 1;
            do System.out.println(i++); while(i <= 10);

            System.out.println("Ejecutándose segundo bucle while...");
            i = 1;
            while(i < 0) System.out.println(i++);

            System.out.println("Ejecutándose segundo bucle do-while...");
            i = 1;
            do System.out.println(i++); while(i < 0);
        }
    }
```

**R:**
En este código hay 4 casos:

- **Primer** bucle **while**: Sucede lo mismo que en el ejercicio 20.1:

    Se declara la variable i y se incializa a 1, mientras que i sea menor o igual que 10, imprimimos el resultado del posincremento de esta variable.

    **Output:**  Lista del 1 al 10 separada por saltos de línea.

- **Primer** bucle **do-while**:

    Se le asigna a i el valor a 1. Con el keyword "**do**" definiremos lo que queremos ejecutar (es decir, imprimir el posincremento de i) y luego el "**while**" que nos indicará la condición que se evaluará (mientras i sea menor o igual que 10).

    **Output:** Lista del 1 al 10 separada por saltos de línea.

- **Segundo** bucle **while**:

    Se le asigna a i el valor a 1. Mientras que i sea inferior a 0 (es decir **nunca**, ya que 1 es mayor que 0), hacemos un print del posincremento de i (pero esto nunca se ejecutará ya que como hemos dicho, la condición del while no se cumple).

    **Output:** Nada

- **Segundo** bucle **do-while**:

    Se le asigna a i el valor a 1. Con el keyword "**do**" definiremos lo que queremos ejecutar primero (es decir, imprimir el resultado del posincremento de i) y luego el "**while**" que
    nos indicará la condición que se evaluará (mientras i sea menor que 0).

    **Output:**  1

    Qué sucede ? En este caso, al ser un posincremento
     1. Se imprime primero el valor de i (que es 1) y luego se incrementa (ahora i = 2)
     2. Se evalua la condición i < 0, lo que sería 2 < 0 con lo cual es **falso**
     3. Se para de ejecutar el bucle

<br>

---

<br>

**Ejercicio 20.4**

**P:** Explique el siguiente código

```
    public class Principal{
        public static void main(String[] args)
        {
            int i = 1;
            int suma = 0;
            while(i <= 100){
                suma = suma + i;
                i++;
            }
            System.out.println(suma);
        }
    }
```

**R:**
1. Declaramos e inicializamos la variable **i** con un valor de 1
2. Declaramos e inicializamos la variable **suma** con un valor de 0
3. Creamos un bucle **while** donde la condición que se evalúa es : "mientras que **i** sea menor o igual a 100"
4. Dentro del bucle sumamos el valor actual de **i** a **suma**
5. Incrementamos el valor de **i** (equivalente a hacer ```i = i + 1``` o ```i += 1```)
6. Si la condición ```i <= 100``` sigue siendo verdadera, el bucle se sigue ejecutando hasta que la condición sea falsa.
7. Una vez que el bucle termina, hacemos un print del valor de **suma**

<br>

---

<br>

**Ejercicio 20.5**

**P:** Explique el siguiente código

```
    public class Principal{
        public static void main(String[] args)
        {
            int suma = 0;
            for(int i = 1; i <= 100; i++){
                suma = suma + i;
            }
            System.out.println(suma);
        }
    }
```

**R:**

Este código nos dará el mismo resultado que el anterior, solo que en vez de usar un bucle **while**, usamos un bucle **for**.

1. Declaramos e inicializamos la variable **suma** con un valor de 0
2. Creamos un bucle **for** donde:
    - Declaramos e inicializamos la variable **i** con un valor de 1 ```int i = 1```
    - Ponemos la condición que se evalúa  : "mientras que **i** sea menor o igual a 100" ```i <= 100```
    - Incrementamos el valor de **i** en cada iteración ```i++```
3. Dentro del bucle, sumamos el valor actual de **i** a **suma** en cada iteración
4. Una vez que termina el bucle (es decir, una vez que ya no sea menor o igual a 100), imprimimos el valor de suma

<br>

---

<br>

**Ejercicio 20.6**

**P:** Explique el siguiente código

```
public class Principal
{
    public static void main(String[] args)
    {
        int[] x = new int[10];

        x[0] = 3;
        x[1] = 6;
        x[2] = 8;

        int j = 0;

        System.out.println(x[j++]);
        System.out.println("BUCLE WHILE");
        System.out.println("===========");
        int i = 0;
        while(i < x.length) System.out.println(x[i++]);

        System.out.println("nBUCLE FOR");
        System.out.println("==========");
        for(int k = 0; k < x.length; k++) System.out.println(x[k]);

        System.out.println("nBUCLE DO");
        System.out.println("=========");
        int l = 0;
        do System.out.println(x[l++]);while(l < x.length - 1);
    }
}
```

**R:**

En este código :

1. Primero declaramos un array de int's (enteros) con una longitud de 10```int[] x = new int[10];``` (las posiciones / "índices" van del 0 al 9).

2. ```x[0] = 3;```: En la posición 0 de este array (es decir, su primer índice) le asignamos el valor 3.

3. ```x[1] = 6;```: En la posición 1 de este array (es decir, su segundo índice) le asignamos el valor 6.

4. ```x[2] = 8;```: En la posición 2 de este array (es decir, su tercer índice) le asignamos el valor 8.

5. ```int j = 0;```: Declaramos una variable **j** con el valor **0**.

6. Después lo que hacemos es imprimir el valor de la **posición** del **posincremento de j** en el **array x**  : ```System.out.println(x[j++])```.

Como aqui es **posincremento** de j, primero se évalua el valor de **j** (que sería 0) y después se incrementa, con lo cual se imprimirá el valor de x[0], que es **3**.


**Bucle while** :

            int i = 0;
            while(i < x.length) System.out.println(x[i++]);

1. Declaramos e inicializamos la variable i con un valor de 0 ```int i = 0```;
2. Declaramos un bucle **while** en la que se evalúa la condición : "mientras que i sea estrictamente menor a la longitud del array x (```while(i < x.length)```)
3. Dentro de este bucle, se imprimirá a cada iteración el valor de la posición actual del array **x** en el que se encuentra el índice **i** y depues se hace el incremento de i (ya que es **posincremento**) ```System.out.println(x[i++]);```

Esto quiere decir que se como resultado obtendremos los valores de todas las posiciones del array **x**, separados por saltos de línea. He aqui una representación del array (valores y posiciones) :

```
(3 6 8 0 0 0 0 0 0 0)   <- Valores
 ^ ^ ^ ^ ^ ^ ^ ^ ^ ^
 0 1 2 3 4 5 6 7 8 9    <- Posiciones / índices
```

(Los 0's que van después se deben a que es el valor por defecto de las posiciones a las que no les hemos asignado un valor después de haber declarado el array)

**Bucle for** :

        for(int k = 0; k < x.length; k++) System.out.println(x[k]);

1. Declaramos un bucle **for** en el que:
    - Declaramos e inicializamos la variable k con un valor de 0 : ```int k = 0```;
    - Declaramos la condición que se evaluará : "mientras que k sea estrictamente menor a la longitud del array x : ```k < x.length)```
    - Incrementamos el valor de k a cada iteración : ```k++```
2. Dentro de este bucle, imprimimos el valor de la **posición k** del array **x** ```System.out.println(x[k]);```

Esto nos dará el mismo resultado que el bucle while anterior, la única diferencia es que el incremento de **k** se hace dentro de la declaración del for, mientras que en el while se hacía dentro del print.

**Bucle do** :

            int l = 0;
            do System.out.println(x[l++]);while(l < x.length - 1);

1. Declaramos e inicializamos la variable **l** con un valor de 0;  ```int l = 0;```
2. Declaramos un **do** en el que indicamos que queremos ejecutar un print de la posición posincremento de l en el array **x**  ```do System.out.println(x[l++])```
3. Declaramos un **while** en el que indicamos hasta cuando se ejecutara ese **do** (mientras que el valor de **l** sea estrictamente menor que el resultado de (**longitud del array x** - **1**)) ```while(l < x.length - 1);```

Como la longitud del array x es 10 (posiciones del 0 al 9), aquí lo que sucederá es que nos imprimirá un valor menos (hasta que l sea igual a 9 -> posición 8 del array). El resultado sería lo siguiente (únicamente los valores y separados por un salto de línea). He aqui una representación del array (valores y posiciones):

```
(3 6 8 0 0 0 0 0 0)   <- Valores
 ^ ^ ^ ^ ^ ^ ^ ^ ^
 0 1 2 3 4 5 6 7 8    <- Posiciones / índices
```

<br>

---

<br>

**Ejercicio 20.7**

**P:** ¿Qué ocurre si se intenta acceder a una posición mayor o igual a la
longitud del array?

**R:** Si intentamos acceder a una posición mayor o igual a la longitud del array, obtendremos un error que nos indicará que estamos accediendo a una posición que está fuera de rango (un error "**IndexOutOfBounds**"), ya que estaríamos intentando acceder a un lugar de la memoria que no hemos reservado para ese array.

<br>

---

<br>

**Ejercicio 20.8**

**P:** ¿Por qué el bucle do-while tiene una condición diferente a la de los otros dos?

**R:** A diferencia de los otros bucles, **do-while** siempre se ejecuta al menos una vez, aunque la condición que haya en el **while** sea falsa. Aqui utilizamos ```x.length - 1``` para imprimir hasta la penultima posición del array, es decir no imprimir el ultimo elemento. Aún así, en nuestro ejemplo si hubieramos usado un ```x.length``` en el **do-while** tambien habría funcionado y nos hubiera impreso todos los elementos.

<br>

---

<br>

**Ejercicio 20.9**

**P:** ¿Qué criterio se utiliza para utilizar un bucle do-while en lugar de un
bucle while.

**R:** Como indiqué en la respuesta anterior, el **do-while** siempre se ejecuta al menos una vez

Por ejemplo, en nuestro caso:

```
    do System.out.println(x[l++]);  // < Esto siempre se ejecutará al principio (1 vez)
    while(l < x.length - 1);        // < aunque esta condición sea falsa
```

Con lo cual, el criterio para elegir entre un **do-while** y un **while** es si queremos que se ejecute nuestro código al menos una vez, o si queremos que se verifique estrictamente nuestra condición antes de ejecutarlo o no.
