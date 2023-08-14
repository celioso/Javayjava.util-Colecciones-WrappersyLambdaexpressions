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

## Cast explícito e implícito

Ya hemos hablado mucho sobre *Type Cast* que no es más que convertir de un tipo a otro.

Cast implícito y explícito de primitivos

Para ser correctos, ya hemos visto cast sucediendo incluso antes de definirlo. Tenemos dos ejemplos, el primero en el mundo de los primitivos:

```java
int numero = 3;
double valor = numero; //cast implícito
```

Observe que colocamos un valor de la variable *numero* (tipo int) en la variable valor (tipo double), sin usar un cast explícito. ¿Esto funciona? La respuesta es sí, ya que cualquier entero cabe dentro de un double. Por eso el compilador se queda quieto y no exige un cast *explícito*, pero nada le impide escribir lo:

```java
int numero = 3;
double valor = (double) numero; //cast explícito
```

Ahora bien, lo contrario no funciona sin cast, ya que un *double* no cabe en un *int*:

```java
double valor = 3.56;
int numero = (int) valor; //cast explícito es exigido por el compilador
```

En este caso, el compilador desecha todo el valor fraccionario y almacena solo el valor entero.

## Cast implícito y explícito de referencias

En las referencias, se aplica el mismo principio. Si el cast siempre funciona no es necesario hacerlo explícito, por ejemplo:

```java
CuentaCorriente cc1 = new CuentaCorriente(22, 33);
Cuenta cuenta = cc1; //cast implícito
```

Aquí también podría ser explícito, pero nuevamente, el compilador no lo requiere porque cualquier CuentaCorriente es una Cuenta:

```java
CuentaCorriente cc1 = new CuentaCorriente(22, 33);
Cuenta Cuenta = (Cuenta) cc1; //cast explícito mas desnecessário
```

## Cast posible e imposible

¿Type cast explícito siempre funciona?

La respuesta es no. El cast explícito solo funciona si es posible, pero hay casos en los que el compilador sabe que un cast es imposible y luego ni compila ni con *type* cast. Por ejemplo:

```java
Cliente cliente = new Cliente();
Cuenta cuenta = (Cuenta) cliente; //imposible, no compila
```

Como el cliente no extiende la clase de *Cuenta* ni implementa una interfaz de tipo de *Cuenta*, es imposible que funcione ese *cast*, ya que una referencia de tipo de Cuenta nunca puede apuntar a un objeto del tipo de *Cliente*.

La certificación Java tiene muchas de estas preguntas sobre cast posible, imposible, explícita e implícita. Si pretendes obtener esta certificación, vale la pena estudiar este tema con mucha tranquilidad.

