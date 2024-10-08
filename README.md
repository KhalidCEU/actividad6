## Actividad 6


### 1.3 El preincremento y el posincremento

**P:** Explique la diferencia entre pre-incremento y el pos-incremento.

**R:** La diferencia entre pre-incremento y el pos-incremento es:

- En el **pre-incremento** primero incrementamos el valor de la variable y luego la evaluamos.

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

- En el **pos-incremento** esto sucede al revés, primero evaluamos la variable y luego incrementamos su valor.

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