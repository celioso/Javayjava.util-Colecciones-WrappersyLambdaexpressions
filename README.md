# Javayjava.util: Colecciones, Wrappers y Lambda expressions

## Trabajando con arrays

Ha llegado el momento de que pongas en práctica lo visto en clase. Para hacer esto, siga los pasos que se enumeran a continuación.

**Arrays**

1. En el proyecto bytebank-heredado-cuenta, en el paquete *com.bytebank.banco.test*, cambie el nombre de la clase *Test* a *TestObject*. Después de eso, también en el mismo paquete, crea una nueva clase *TestArrayDePrimitivos*, ya con el método *main*:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {
    }
}
```

2. Para almacenar edades, cree un array de números enteros, con cinco posiciones:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

    }
}
```

3. Luego, inicialice cada posición del array con una edad:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

        edades[0] = 29;
        edades[1] = 39;
        edades[2] = 49;
        edades[3] = 59;
        edades[4] = 69;

    }
}
```

4. Al acceder a cualquier posición del array, devuelve el valor almacenado en esa posición. Luego, guarde el valor de la cuarta posición del array en una variable e imprímalo:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

        edades[0] = 29;
        edades[1] = 39;
        edades[2] = 49;
        edades[3] = 59;
        edades[4] = 69;

        int edad4 = edades[3];

        System.out.println(edad4);

    }

}
```

5. Imprime el tamaño del array accediendo a su atributo de **length**:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

        edades[0] = 29;
        edades[1] = 39;
        edades[2] = 49;
        edades[3] = 59;
        edades[4] = 69;

        int edad4 = edades[3];

        System.out.println(edad4);
        System.out.println(edades.length);

    }

}
```

6.  Inicializa el array dentro de un bucle, pero primero elimine todo el código, dejando solo la inicialización del array:

```java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

    }

}
```

7. Ahora, inicializa el array en un bucle, por ejemplo:

````java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

        for (int i = 0; i < edades.length; i++) {
            edades[i] = i * i;
        }

    }

}
```

8. Luego haz otro bucle e imprime cada elemento del array:

````java
public class TestArrayDePrimitivos {

    public static void main(String[] args) {

        int[] edades = new int[5];

        for (int i = 0; i < edades.length; i++) {
            edades[i] = i * i;
        }

        for (int i = 0; i < edades.length; i++) {
            System.out.println(edades[i]);
        }

    }

}
```

Arrays de referencia

9. En el proyecto *bytebank-heredado-cuenta*, en el paquete *com.bytebank.banco.test*, crea la clase *TestArrayReferencias*, ya con el método *main*:

```java
public class TestArrayReferencias {

    public static void main(String[] args) {

    }
}
```

10. Para guardar cuentas, cree un array de CuentaCorriente, con cinco posiciones:

````java
public class TestArrayReferencias {

    public static void main(String[] args) {

        CuentaCorriente[] cuentas = new CuentaCorriente[5];

    }

}
```

11. Cree una instancia de dos cuentas y guárdalas en las dos primeras posiciones del array, por ejemplo:

```java
public class TestArrayReferencias {

    public static void main(String[] args) {

        CuentaCorriente[] cuentas = new CuentaCorriente[5];

        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        CuentaCorriente cc2 = new CuentaCorriente(22, 22);

        cuentas[0] = cc1;
        cuentas[1] = cc2;

    }

}
```

12. A través del array, acceda a la cuenta de la primera posición e imprima su número:

```java
public class TestArrayReferencias {

    public static void main(String[] args) {

        CuentaCorriente[] cuentas = new CuentaCorriente[5];

        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        CuentaCorriente cc2 = new CuentaCorriente(22, 22);

        cuentas[0] = cc1;
        cuentas[1] = cc2;

        System.out.println(cuentas[0].getNumero());

    }

}
```

## Forma literal

Hasta ahora hemos visto la forma "clásica" de crear un objeto array utilizando la palabra clave new, por ejemplo:

```java
int[] numeros = new int[6];
numeros[0] = 1;
numeros[1] = 2;
numeros[2] = 3;
numeros[3] = 4;
numeros[4] = 5;
```

Sin embargo, también existe una forma literal. *Literal*, en este contexto, significa usar valores directamente, menos burocrático, más directo. Vea la diferencia:

```java
int[] refs = {1,2,3,4,5};
```

Usamos las llaves {} para indicar que es un array y los valores ya están declarados dentro de las llaves.

### ¿Qué aprendimos?

En esta clase sobre *arrays* aprendimos:

- Un array es una estructura de datos y se usa para almacenar elementos (valores primitivos o referencias)
- Los arrays usan corchetes ([]) sintácticamente
- ¡Los arrays tienen un tamaño fijo!
- ¡Un array también es un objeto!
- Los arrays son *zero-based*(el primer elemento se encuentra en la posición 0)
- Un array siempre se inicializa con los valores padron.
- Al acceder a una posición no válida recibimos la excepción ArrayIndexOutOfBoundException
- Las matrices tienen un atributo *length* para conocer el tamaño
- La forma literal de crear un array, utilizando llaves {}.
En el próximo capítulo hablaremos un poco más sobre arrays (de tipo Object) y veremos cómo funciona este parámetro del método main.

### Proyecto del aula anterior

¿Comenzando en esta etapa? Aquí puedes descargar los archivos del proyecto que hemos avanzado hasta el aula anterior.

[Descargue los archivos en Github](https://github.com/alura-es-cursos/java-util-collections-lambdas/tree/clase-1 "Descargue los archivos en Github") o haga clic [aquí](https://github.com/alura-es-cursos/java-util-collections-lambdas/archive/clase-1.zip "aquí") para descargarlos directamente.


