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
3. En cada iteración de este while, se ejecutará un **println** del **posincremento** de esta variable. Al ser un posincremento, primero se hará el print del valor de i y despues se incrementará

Con lo cual obtendremos como output una lista del 1 al 10 (separada por saltos de linea)


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

Obtendremos como resultado lo mismo que en el caso anterior, una lista del 1 al 10 separada por saltos de linea.

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

    **Output:**  Lista del 1 al 10 separada por saltos de linea.

- **Primer** bucle **do-while**:

    Se le asigna a i el valor a 1. Con el keyword "**do**" definiremos lo que queremos ejecutar (es decir, imprimir el posincremento de i) y luego el "**while**" que nos indicará la condición que se evaluará (mientras i sea menor o igual que 10).

    **Output:** Lista del 1 al 10 separada por saltos de linea.

- **Segundo** bucle **while**:

    Se le asigna a i el valor a 1. Mientras que i sea inferior a 0 (es decir **nunca**, ya que 1 es mayor que 0), hacemos un print del posincremento de i (pero esto nunca se ejecutará ya que como hemos dicho, la condición del while no se cumple).

    **Output:** Nada

- **Segundo** bucle **do-while**:

    Se le asigna a i el valor a 1. Con el keyword "**do**" definiremos lo que queremos ejecutar primero (es decir, imprimir el resultado del posincremento de i) y luego el "**while**" que
    nos indicará la condición que se evaluará (mientras i sea menor que 0).

    **Output:**  1

    Que sucede ? En este caso, al ser un posincremento
     1. Se imprime primero el valor de i (que es 1) y luego se incrementa (ahora i = 2)
     2. Se evalua la condicion i < 0, lo que sería 2 < 0 con lo cual es **falso**
     3. Se para de ejecutar el bucle



