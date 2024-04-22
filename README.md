En este *repl* puedes encontrar varios ejemplos que te pueden ayudar con las tareas de estructura.

## Código de Ejemplo (main)
Para ejecutar el main primero debemos compilar (en la carpeta raíz)
````
gcc tdas/*.c main.c -Wno-unused-result -o main
````

Y luego ejecutar:
````
./main
````

## TDAs
En la carpeta `tdas` se encuentran implementados distintos TDAs que puedes utilizar (lista, pila, cola, cola con prioridad y mapas). 

Las implementaciones no son las más eficientes (todas usan como estructura de datos una **lista enlazada**), por lo que puedes reemplazarlas por las que has realizado en los labs.

## Otros códigos (en carpeta examples)
Para ejecutar los distintos ejemplos que hay en la carpeta `examples`, primero debes compilarlos. Si estamos en la carpeta raíz:
````
gcc tdas/*.c examples/example2_menu.c -Wno-unused-result -o example
````
Y luego ejecutarlos:
````
./example
````

Se incluyen los siguientes ejemplos:
* `example1_list`: Uso del TDA Lista, inserción y eliminación de elementos.
* `example2_menu`: Ejemplo de menú con submenús.
* `example3_readcsv`: Ejemplo de lectura desde un archivo csv y almacenamiento en datos estructurados.
* `example4_map`: Ejemplo de uso del TDA mapa.


## Funcionalidades

### Funcionando correctamente:

- Registrar pacientes con sus datos básicos y una prioridad inicial.
- Asignar o modificar la prioridad de los pacientes.
- Ver la lista de espera de pacientes, ordenada por prioridad y hora de registro.
- Atender al siguiente paciente, respetando el orden de prioridad.

### Problemas conocidos:

- Asumiendo que el usuario ingresa los datos adecuadamente no debería haber errores

### A mejorar:

- El usuario puede ingresar numeros en el nombre y sintomas
- El usuario puede ingresar letras en la edad

## Ejemplo de uso

**Paso 1: Registrar un Nuevo Paciente**

Se comienza registrando un nuevo paciente que acaba de llegar al hospital.

```
Opción seleccionada: 1) Registrar paciente
Ingrese el nombre del paciente: Bresman Vargas
Ingrese la edad del paciente: 29
Ingrese el síntoma del paciente: Dolor abdominal agudo
```

El sistema registra a Bresman Vargas con una prioridad inicial "Bajo" y guarda la hora actual de registro. La prioridad inicial puede ser ajustada más tarde basada en una evaluación médica más detallada.

**Paso 2: Asignar Prioridad a un Paciente**

Tras una evaluación inicial, el médico determina que el estado de Ana requiere atención prioritaria.

```
Opción seleccionada: 2) Asignar prioridad a paciente
Ingrese el nombre del paciente: Bresman Vargas
Seleccione el nuevo nivel de prioridad (Alto, Medio, Bajo): Alto
```

El sistema actualiza la prioridad de Bresman Vargas a "Alto", asegurando que será una de las próximos pacientes en ser atendido.

**Paso 3: Ver la Lista de Espera**

El usuario revisa la lista de espera para ver todos los pacientes y sus prioridades.

```
Opción seleccionada: 3) Mostrar lista de espera
```

La lista muestra a Bresman Vargas en la parte superior, indicando su prioridad alta y que es la siguiente en línea para recibir atención.

**Paso 4: Atender al Siguiente Paciente**

Bresman Vargas es llamada para ser atendida basándose en su prioridad.

```
Opción seleccionada: 4) Atender al siguiente paciente
```

El sistema muestra que Bresman Vargas está siendo atendida y la elimina de la lista de espera.

