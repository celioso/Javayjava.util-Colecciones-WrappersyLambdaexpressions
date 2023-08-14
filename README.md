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

## Haga lo que hicimos en clase: Arrays

Ha llegado el momento de practicar lo que vimos en este capítulo.

1. Tenemos la siguiente clase:

```java
package com.bytebank.banco.test;

import com.bytebank.banco.modelo.CuentaCorriente;

public class TestArrayReferencias {

    public static void main(String[] args) {

        CuentaCorriente[] cuentas = new CuentaCorriente[5];
        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        cuentas[0] = cc1;

        CuentaCorriente cc2 = new CuentaCorriente(22, 22);
        cuentas[1] = cc2;    

        System.out.println( cuentas[1].getNumero()  );

        CuentaCorriente ref = cuentas[0];
        System.out.println(cc2.getNumero());
        System.out.println(ref.getNumero());
    }
}
```

2. Queremos almacenar instancias de *CuentaCorriente* o *CuentaAhorro* en el array de cuentas. Para eso, necesitamos que la cuenta sea de un tipo más genérico, en el caso de *Cuenta*.

```java
package com.bytebank.banco.test;

import com.bytebank.banco.modelo.CuentaCorriente;
// importo
import com.bytebank.banco.modelo.CuentaAhorro;

public class TestArrayReferencias {

    public static void main(String[] args) {

        // alterando el tipo
        Cuenta[] cuentas = new Cuenta[5];
        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        cuentas[0] = cc1;

        // crea instancia de CuentaAhorro
        CuentaAhorro ca2 = new CuentaAhorro(22, 22);
        cuentas[1] = ca2;    

        System.out.println(cuentas[1].getNumero()  );

        // no compila
        CuentaCorriente ref = cuentas[0];
        System.out.println(cc2.getNumero());
        System.out.println(ref.getNumero());

    }
}
```

Cuando cambiamos el tipo de *array* de *CuentaCorriente*, la siguiente instrucción deja de compilarse:

`CuentaCorriente ref = cuentas[0];`

Debido a que, en tiempo de ejecución, tenemos un objeto de tipo *CuentaCorriente* como primer elemento del array de cuentas, su referencia es del tipo *Cuenta* al acceder a cuentas [0]. Por lo tanto, una solución es cambiar el tipo de variable de *ref* a *Cuenta*:

```java
package com.bytebank.banco.test;

import com.bytebank.banco.modelo.CuentaCorriente;
// importo
import com.bytebank.banco.modelo.CuentaAhorro;

public class TestArrayReferencias {

    public static void main(String[] args) {

        // alterando el tipo
        Cuenta[] cuentas = new Cuenta[5];
        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        cuentas[0] = cc1;

        // crea instancia de CuentaAhorro
        CuentaAhorro ca2 = new CuentaAhorro(22, 22);
        cuentas[1] = ca2;    

        System.out.println(cuentas[1].getNumero()  );

        // alterou o tipo, agora compila
        Cuenta ref = cuentas[0];
        System.out.println(cc2.getNumero());
        System.out.println(ref.getNumero());
    }
}
```

3. Modifique el código para que incluso utilizando el tipo *CuentaCorriente* sea posible asignar a la variable ref el valor de *cuentas[0]*. Como estamos seguros de que el elemento en la posición *cuentas[0]* es una instancia de *CuentaCorriente*, podemos asumir la responsabilidad de la conversión a través de un *type cast*:

```java
package com.bytebank.banco.test;

import com.bytebank.banco.modelo.CuentaCorriente;
// importo
import com.bytebank.banco.modelo.CuentaAhorro;

public class TestArrayReferencias {

    public static void main(String[] args) {

        // alterando el tipo
        Cuenta[] cuentas = new Cuenta[5];
        CuentaCorriente cc1 = new CuentaCorriente(22, 11);
        cuentas[0] = cc1;

        // crea instancia de CuentaAhorro
        CuentaAhorro ca2 = new CuentaAhorro(22, 22);
        cuentas[1] = ca2;    

        System.out.println(cuentas[1].getNumero()  );

        // alterou o tipo, realizando o cast
        CuentaCorriente ref = (CuentaCorriente) cuentas[0];
        System.out.println(cc2.getNumero());
        System.out.println(ref.getNumero());
    }
}
```

4. Ahora intente acceder al elemento en la posición de *cuentas[1]*. Como en tiempo de ejecución es del tipo *CuentaAhorro*, el cast no funcionará y se lanzará una excepción en la consola.

## ¿Qué aprendimos?

En esta clase aprendimos:

- Un array de tipo *Object* puede contener cualquier tipo de referencia.
- Cuando convertimos una referencia genérica a una referencia más específica, necesitamos usar un *type cast*.
- El *cast* solo compila cuando es posible, aún así puede fallar al ejecutarse.
- Cuando falla el *type cast*, podemos recibir un *ClassCastException*.
- Para recibir valores al llamar al programa Java en la línea de comando, podemos usar la matriz *String[]* en el método *main*.
¡En la próxima clase comenzaremos a hablar de listas! Espere :)

## Proyecto del aula anterior

¿Comenzando en esta etapa? Aquí puedes descargar los archivos del proyecto que hemos avanzado hasta el aula anterior.

[Descargue los archivos en Github](https://github.com/alura-es-cursos/java-util-collections-lambdas/tree/clase-2 "Descargue los archivos en Github") o haga clic [aquí](https://github.com/alura-es-cursos/java-util-collections-lambdas/archive/clase-2.zip "aquí") para descargarlos directamente.

## GuardadorDeCuentas

Ha llegado el momento de que pongas en práctica lo visto en clase. Para hacer esto, siga los pasos que se enumeran a continuación.

1. Cree la clase *GuardadorDeCuentas*:

```java
package com.bytebank.banco.modelo;

public class GuardadorDeCuentas {

    private Cuenta[] referencias;

    public GuardadorDeCuentas() {
        this.referencias = new Cuenta[10];
    }
}
```

2. Crea una clase para probar al guardador de cuentas.

```java
public class Test {
    public static void main(String[] args) {
        GuardadorDeCuentas guardador = new GuardadorDeCuentas();

        Cuenta cc = new CuentaCorriente(22, 11);
        guardador.adicionar(cc);
    }
}
```

3. Cree el método adicionar() en el guardador:

```java
public class GuardadorDeCuentas {

    private Cuenta[] referencias;
    private int posicionLibre;

    public GuardadorDeCuentas() {
        this.referencias = new Cuenta[10];
        this.posicionLibre = 0;
    }

    public void adicionar(Cuenta ref) {
        referencias[this.posicionLibre] = ref;
        this.posicionLibre++;
    }

}
```

4. Modifique su clase de Test para incluir una cuenta más:

```java
public class Test {
    public static void main(String[] args) {
        GuardadorDeCuentas guardador = new GuardadorDeCuentas();

        Cuenta cc = new CuentaCorriente(22, 11);
        guardador.adicionar(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        guardador.adicionar(cc2);
    }
}
```

5.  Ahora queremos comprobar si la cantidad de elementos dentro del guardador es 2. Cree el código en la clase de Test y aproveche la sugerencia de Eclipse para crear el método por usted.

````java
public class Test {
    public static void main(String[] args) {
        GuardadorDeCuentas guardador = new GuardadorDeCuentas();

        Cuenta cc = new CuentaCorriente(22, 11);
        guardador.adicionar(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        guardador.adicionar(cc2);

        int tamano = guardador.getCantidadDeElementos();
        System.out.println(tamano);
    }
}
```

Luego complete la implementación del método en la clase *GuardadorDeCuentas*.

```java
public class GuardadorDeCuentas {

    private Cuenta[] referencias;
    private int posicionLibre;

    public GuardadorDeCuentas() {
        this.referencias = new Cuenta[10];
        this.posicionLibre = 0;
    }

    public void adicionar(Cuenta ref) {
        referencias[this.posicionLibre] = ref;
        this.posicionLibre++;
    }

    public int getCantidadDeElementos() {
        return this.posicionLibre;
    }
}
```

6. Agregue una característica más a la clase de Test para recuperar un determinado elemento del guardador desde una posición. Nuevamente use Eclipse para generar el método por usted:

```java
public class Test {
    public static void main(String[] args) {
        GuardadorDeCuentas guardador = new GuardadorDeCuentas();

        Cuenta cc = new CuentaCorriente(22, 11);
        guardador.adicionar(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        guardador.adicionar(cc2);

        int tamano = guardador.getCantidadDeElementos();
        System.out.println(tamano);

        Cuenta ref = guardador.getReferencia(0);
        System.out.println(ref.getNumero());
    }
}
```

7. Ahora implemente el método en *GuardadorDeCuentas*:

```java
public class GuardadorDeCuentas {

    private Cuenta[] referencias;
    private int posicionLibre;

    public GuardadorDeCuentas() {
        this.referencias = new Cuenta[10];
        this.posicionLibre = 0;
    }

    public void adicionar(Cuenta ref) {
        referencias[this.posicionLibre] = ref;
        this.posicionLibre++;
    }

    public int getCantidadDeElementos() {
        return this.posicionLibre;
    }

    public Cuenta getReferencia(int pos) {
        return this.referencias[pos];
    }
}
```

8. Ejecute la clase de Test para verificar que el guardador esté funcionando.

9. (Desafío) Ahora intente crear un guardador que sepa almacenar cualquier tipo de referencias, usando la clase *Object*.

## ArrayList

Ha llegado el momento de que pongas en práctica lo visto en clase. Para hacer esto, siga los pasos que se enumeran a continuación.

1. ¿Realizó el desafío del video anterior? Entonces, verifique si su guardador se ve parecido a el siguiente código:

```java
public class GuardadorDeReferencias {

    private Object[] referencias;
    private int posicionLibre;

    public GuardadorDeReferencias() {
        this.referencias = new Object[10];
        this.posicionLibre = 0;
    }

    public void adicionar(Object ref) {
        referencias[this.posicionLibre] = ref;
        this.posicionLibre++;
    }

    public int getCantidadDeElementos() {
        return this.posicionLibre;
    }

    public Object getReferencia(int pos) {
        return this.referencias[pos];
    }
}
```

2. Cree una prueba(test) para validar el guardador de referencias:

```java
public class TestGuardadorReferencias {
    public static void main(String[] args) {
        GuardadorDeReferencias guardador = new GuardadorDeReferencias();

        Cuenta cc = new CuentaCorriente(22, 11);
        guardador.adicionar(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        guardador.adicionar(cc2);

        int tamano = guardador.getCantidadDeElementos();
        System.out.println(tamano);

        Cuenta ref = (Cuenta)guardador.getReferencia(0);
        System.out.println(ref.getNumero());        
    }
}
```

3. Ya existe una clase para simplificar el acceso al array. Esta clase es *ArrayList*. Cree la clase *Test* dentro del paquete *br.com.bytebank.banco.test.util* para probar esta clase con el siguiente código:

```java
package com.bytebank.banco.test.util;

import java.util.ArrayList;

public class Test {
    public static void main(String[] args) {

        ArrayList lista = new ArrayList();

        Cuenta cc = new CuentaCorriente(22, 11);
        lista.add(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        lista.add(cc2);

        System.out.println("Tamano: " + lista.size());

        Cuenta ref = (Cuenta) lista.get(0);
        System.out.println(ref.getNumero());

        lista.remove(0);
        System.out.println("Tamano: " + lista.size());

        Cuenta cc3 = new CuentaCorriente(33, 311);
        lista.add(cc3);

        Cuenta cc4 = new CuentaCorriente(33, 322);
        lista.add(cc4);

        for(int i = 0; i < lista.size(); i++) {
            Object oRef = lista.get(i);
            System.out.println(oRef);
        }

        System.out.println("----------");

        for(Object oRef : lista) {
            System.out.println(oRef);
        }

    }
}
```

## Generics

Ha llegado el momento de que pongas en práctica lo visto en clase. Para hacer esto, siga los pasos que se enumeran a continuación.

1. Para demostrar problemas en el ArrayList, agregue un objeto de tipo *Cliente* y ejecute la clase Test. Verá que se producirá una excepción del tipo *ClassCastException* porque no fue posible convertir la referencia del tipo *Cliente* en una Cuenta.

```java
package br.com.bytebank.banco.test.util;

import java.util.ArrayList;

public class Test {
    public static void main(String[] args) {

        ArrayList lista = new ArrayList();

        //Cuenta cc = new CuentaCorriente(22, 11);
        Cliente cliente = new Cliente();
        lista.add(cliente);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        lista.add(cc2);

        System.out.println("Tamanho: " + lista.size());

        Cuenta ref = (Cuenta) lista.get(0);
        System.out.println(ref.getNumero());

        lista.remove(0);
        System.out.println("Tamanho: " + lista.size());

        Cuenta cc3 = new CuentaCorriente(33, 311);
        lista.add(cc3);

        Cuenta cc4 = new CuentaCorriente(33, 322);
        lista.add(cc4);

        for(int i = 0; i < lista.size(); i++) {
            Object oRef = lista.get(i);
            System.out.println(oRef);
        }

        System.out.println("----------");

        for(Object oRef : lista) {
            System.out.println(oRef);
        }

    }
}
```

2. Informe al compilador que solo desea crear una matriz de cuentas. Modifique la clase de prueba para hacer esto:

```java
package br.com.bytebank.banco.test.util;

import java.util.ArrayList;

public class Test {
    public static void main(String[] args) {

        ArrayList<Cuenta> lista = new ArrayList<Cuenta>();

        Cuenta cc = new CuentaCorriente(22, 11);
        lista.add(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        lista.add(cc2);

        System.out.println("Tamanho: " + lista.size());

        Cuenta ref = (Cuenta) lista.get(0);
        System.out.println(ref.getNumero());

        lista.remove(0);
        System.out.println("Tamanho: " + lista.size());

        Cuenta cc3 = new CuentaCorriente(33, 311);
        lista.add(cc3);

        Cuenta cc4 = new CuentaCorriente(33, 322);
        lista.add(cc4);

        for(int i = 0; i < lista.size(); i++) {
            Object oRef = lista.get(i);
            System.out.println(oRef);
        }

        System.out.println("----------");

        for(Object oRef : lista) {
            System.out.println(oRef);
        }

    }
}
```

3. Intente agregar un objeto de otro tipo a la lista anterior. ¡El compilador no te dejará!

4. Modifique su código para aprovechar los beneficios de los *generics*, elimine el cast en el método *get()* y al usar enchanced *for*:

```java
package br.com.bytebank.banco.test.util;

import java.util.ArrayList;

public class Test {
    public static void main(String[] args) {

        ArrayList<Cuenta> lista = new ArrayList<Cuenta>();

        Cuenta cc = new CuentaCorriente(22, 11);
        lista.add(cc);

        Cuenta cc2 = new CuentaCorriente(22, 22);
        lista.add(cc2);

        System.out.println("Tamanho: " + lista.size());

        Cuenta ref = lista.get(0);
        System.out.println(ref.getNumero());

        lista.remove(0);
        System.out.println("Tamanho: " + lista.size());

        Cuenta cc3 = new CuentaCorriente(33, 311);
        lista.add(cc3);

        Cuenta cc4 = new CuentaCorriente(33, 322);
        lista.add(cc4);

        for(int i = 0; i < lista.size(); i++) {
            Object oRef = lista.get(i);
            System.out.println(oRef);
        }

        System.out.println("----------");

        for(Cuenta oRef : lista) {
            System.out.println(oRef);
        }

    }
}
```

5. ¡Excelente! ¡Ahora su código es más seguro y expresivo con el uso de **Generics**!

## Otras formas de inicialización

Lista con capacidad predefinida.

Decíamos que el *ArrayList* es un array dinámico, es decir, debajo de la tela se usa un array, pero sin preocuparse por los detalles y limitaciones.

Ahora piense que necesita crear una lista que represente a los 26 estados de Brasil. Le gustaría usar un *ArrayList* para "escapar" del *array*, pero sabe que *ArrayList* crea un array automáticamente, del tamaño que la clase considere conveniente.

¿No hay alguna forma de crear esta lista definiendo el tamaño del array? Por supuesto que lo es y es muy sencillo. El constructor de la clase *ArrayList* es sobrecargado y tiene un parámetro que recibe la capacidad:

```java
ArrayList lista = new ArrayList(26); //capacidad inicial
```

La lista sigue siendo dinámica, ¡pero el tamaño de la matriz inicial es 26!

Lista a partir de otra

Otra forma de inicializar una lista es basada en otra que es muy común en el día a día. Para esto, *ArrayList* tiene un constructor más que recibe la lista base:

```java
ArrayList lista = new ArrayList(26); //capacidad inicial
lista.add("RJ");
lista.add("SP");
//otros estados
ArrayList nueva = new ArrayList(lista); //creando basada en la primera lista
```

Cuanto más sepamos sobre las clases estándar de Java, más fácil será nuestro código.

## ¿Qué aprendimos?

En esta clase comenzamos a hablar sobre la lista y llegamos a conocer la clase *java.util.ArrayList*. Aprendimos:

- Que la clase *java.util.ArrayList* encapsula el uso de array y ofrece varios métodos de más alto nivel.
- Que una lista guarda referencias.
- Cómo usar los métodos *size*, *get*, *remove*.
- Cómo usar *foreach* para iterar a través de *ArrayList*.
- Que los generics parametrizan clases
- Que en el caso de *ArrayList* podemos definir el tipo de los elementos mediante generics.
Este es solo el comienzo de este poderoso paquete *java.util*. ¡En la próxima clase bucearemos más!

## Equals

Ha llegado el momento de replicar lo que se hizo en video.

1. Cambie el nombre de la clase *Test* a *TestArrayList* y cree una copia de esa clase con el nombre *TestArrayListEquals*.

2. Elimine parte del código de la clase *TestArrayListEquals*, dejando solo:

```java
public static void main(String[] args){

    ArrayList<Cuenta> lista = new ArrayList<Cuenta>();

    Cuenta cc1 = new CuentaCorriente(22, 22);
    Cuenta cc2 = new CuentaCorriente(22, 22);

    lista.add(cc1);

    for(Cuenta cuenta : lista){
        System.out.println(cuenta);
    }
}
```

3. Pruebe si su lista contiene una cuenta, usando el método *cuentains*:

```java
public static void main(String[] args){

    ArrayList<Cuenta> lista = new ArrayList<Cuenta>();

    Cuenta cc1 = new CuentaCorriente(22, 22);
    Cuenta cc2 = new CuentaCorriente(22, 22);

    lista.add(cc1);

    boolean existe = lista.contains(cc2); //nuevo

    System.out.println("Ya existe? " + existe);

    for(Cuenta cuenta : lista){
        System.out.println(cuenta);
    }
}
```

Tenga en cuenta que la salida es *false*, pero eso no es lo que queremos porque los dos objetos representan la misma cuenta.

4. En la clase *Cuenta* agregue la funcionalidad que verificará si una cuenta es igual a otra. Vea abajo:

```java
public boolean esIgual(Cuenta otra){

    if(this.agencia != otra.agencia){
        return false;
    }

    if(this.numero != otra.numero){
        return false;
    }

    return true;
}
```

5. En la clase *TestArrayListEquals*, pruebe el método usando el siguiente código:

```java
//creación de cuentas omitidas

boolean igual = cc1.esIgual(cc2);
System.out.println(igual); //debe imprimir true
```

6. Haga la misma prueba ahora con cuentas que tengan diferentes números y valores de agencia.

7. Modificar su método *esIgual* para sobreescribir el método *equals*, y recuerde usar *@Override*. Cambie el nombre del método, consulte el código a continuación:

```java
@Override
public boolean equals(Object ref){

    Cuenta otra = (Cuenta) ref;

    if(this.agencia != otra.agencia){
        return false;
    }

    if(this.numero != otra.numero){
        return false;
    }

    return true;
}
```

8. Corrija el código en la clase Test y ejecútalo. ¡Vea que ahora nuestra salida es del método *cuentains* es *true*!

## De Array para List

De ahora en adelante usaremos las listas para escapar de las desventajas del array. Sin embargo, ¿recuerdas nuestro array *String[]* del método main? Ciertamente, y no podemos cambiar la firma del método *main* ya que la JVM no acepta esto. Bueno, dado que no podemos cambiar la firma, ¿no hay forma de transformar un array en una lista? Por supuesto que la hay, y para eso, ya existe una clase que ayuda en esta tarea: *java.util.Arrays*.

La clase *java.util.Arrays* tiene varios métodos estáticos auxiliares para trabajar con arrays. Vea lo simple que es transformar un array en una lista:

```java
public class Test {

  public static void main(String[] args) {
    List<String> argumentos = Arrays.asList(args);
  }
}
```

Veamos otras características de la clase java.util.Arrays

## ¿Qué aprendimos?
En esta clase aprendemos:

- Cómo implementar el método *equals* para definir la igualdad.
- Que el método *equals* es usado por las listas.
- Que hay más de una lista, *java.util.LinkedList*.
- La diferencia entre *ArrayList* y *LinkedList*.
- La interfaz *java.util.List* que define los métodos de la lista.
En el próximo capítulo veremos otra implementación de la *interfaz List*.

### Proyecto del aula anterior
¿Comenzando en esta etapa? Aquí puedes descargar los archivos del proyecto que hemos avanzado hasta el aula anterior.

[Descargue los archivos en Github](https://github.com/alura-es-cursos/java-util-collections-lambdas/tree/clase-4 "Descargue los archivos en Github") o haga clic [aquí](https://github.com/alura-es-cursos/java-util-collections-lambdas/archive/clase-4.zip "aquí") para descargarlos directamente.
