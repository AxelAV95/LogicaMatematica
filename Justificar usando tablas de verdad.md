# Guía: Cómo justificar una proposición usando una tabla de verdad (con 1 y 0)

## ¿Qué tipo de ejercicio es este?

Este tipo de ejercicio te pide verificar si una proposición lógica es siempre verdadera (una tautología), siempre falsa (una contradicción), o si depende de los valores de las variables. Lo hacemos usando una tabla de verdad, que es como una tabla donde pruebas todas las combinaciones posibles de valores (1 para verdadero, 0 para falso) para las variables y ves qué pasa con la proposición.

El ejercicio que resolvimos fue:

$$[(P \lor Q) \land (R \rightarrow \neg P)] \rightarrow (\neg Q \rightarrow \neg R)$$

Queríamos justificar si esta implicación es siempre verdadera (una tautología).

## Herramientas que necesitas saber de antemano

Antes de empezar, necesitas conocer estas cosas básicas:

### Símbolos lógicos y su significado (con ejemplos cotidianos):

- **¬ (Negación):** "No". Cambia el valor. Ejemplo: Si $P$ es "hoy llueve" y es 1 (verdadero), entonces $\neg P$ ("no llueve hoy") es 0 (falso).
- **∨ (Disyunción):** "O". Es 1 si al menos una de las dos cosas es 1. Ejemplo: Si $P$ es "hoy llueve" y $Q$ es "hace sol", $P \lor Q$ ("hoy llueve o hace sol") es 1 si llueve, o hace sol, o ambas cosas.
- **∧ (Conjunción):** "Y". Es 1 solo si ambas cosas son 1. Ejemplo: $P \land Q$ ("hoy llueve y hace sol") es 1 solo si llueve y hace sol al mismo tiempo.
- **→ (Implicación):** "Si... entonces...". Es 0 solo si la primera parte es 1 y la segunda es 0. Ejemplo: Si $R$ es "estudio mucho" y $P$ es "saco buena nota", $R \rightarrow P$ ("si estudio mucho, entonces saco buena nota") es 0 solo si estudio mucho (1) pero no saco buena nota (0).

### Cómo hacer una tabla de verdad:

Si tienes $n$ variables (letras como $P$, $Q$, $R$), hay $2^n$ combinaciones posibles. Por ejemplo, con 3 variables ($P$, $Q$, $R$), hay $2^3 = 8$ filas.

En las primeras columnas, pones todas las combinaciones de 1 y 0 para las variables.

### Valores de verdad para cada símbolo:

#### Negación (¬)
| P | ¬P |
|---|----|
| 1 | 0  |
| 0 | 1  |

#### Disyunción (O, ∨)
| P | Q | P ∨ Q | Regla mnemotécnica |
|---|---|-------|--------------------|
| 1 | 1 |   1   | Verdadero si al menos uno es verdadero |
| 1 | 0 |   1   |                    |
| 0 | 1 |   1   |                    |
| 0 | 0 |   0   | Falso solo si ambos son falsos |

#### Conjunción (Y, ∧)
| P | Q | P ∧ Q | Regla mnemotécnica |
|---|---|-------|--------------------|
| 1 | 1 |   1   | Verdadero solo si ambos son verdaderos |
| 1 | 0 |   0   |                    |
| 0 | 1 |   0   |                    |
| 0 | 0 |   0   |                    |

#### Implicación (→)
| P | Q | P → Q | Explicación |
|---|---|-------|-------------|
| 1 | 1 |   1   | Si P es verdadero y Q es verdadero |
| 1 | 0 |   0   | La única combinación falsa |
| 0 | 0 |   1   | "Falso implica falso" es verdadero |
| 0 | 1 |   1   | "Falso implica verdadero" es verdadero |

#### Resumen rápido
| Operador | Nombre | Se lee como | Ejemplo cotidiano |
|----------|--------|-------------|-------------------|
| ¬        | NOT    | "No"        | "No está lloviendo" |
| ∨        | OR     | "O"         | "Llueve o hace sol" |
| ∧        | AND    | "Y"         | "Llueve y hace frío" |
| →        | THEN   | "Si... entonces" | "Si llueve, entonces me mojo" |

## Paso a paso para resolver el ejercicio

### Paso 1: Identificar las variables y las partes de la proposición

La proposición es:

$$[(P \lor Q) \land (R \rightarrow \neg P)] \rightarrow (\neg Q \rightarrow \neg R)$$

Variables: Hay tres letras: $P$, $Q$, $R$. Esto significa que tendremos $2^3 = 8$ combinaciones.

Partes de la proposición: Esto es una implicación de la forma $A \rightarrow B$, donde:
- $A$ es $[(P \lor Q) \land (R \rightarrow \neg P)]$
- $B$ es $(\neg Q \rightarrow \neg R)$

Queremos saber si $A \rightarrow B$ es siempre 1 (una tautología). En una implicación, $A \rightarrow B$ es 0 solo si $A$ es 1 y $B$ es 0; en todos los demás casos es 1.

### Paso 2: Hacer las columnas iniciales de la tabla

Como tenemos 3 variables ($P$, $Q$, $R$), hacemos 8 filas con todas las combinaciones posibles de 1 y 0 (aquí se debe alternar entre mitad y mitad, hasta descomponer todo y quede 1 y 0 sucesivamente):

| P | Q | R |
|---|---|---|
| 1 | 1 | 1 |
| 1 | 1 | 0 |
| 1 | 0 | 1 |
| 1 | 0 | 0 |
| 0 | 1 | 1 |
| 0 | 1 | 0 |
| 0 | 0 | 1 |
| 0 | 0 | 0 |

### Paso 3: Calcular cada parte de la proposición por separado

Vamos a calcular cada pedacito de la proposición, columna por columna, hasta llegar al resultado final.

#### Paso 3.1: Calcular $P \lor Q$

$P \lor Q$ es 1 si al menos uno de $P$ o $Q$ es 1.

| P | Q | $P \lor Q$ |
|---|---|-----------|
| 1 | 1 |     1     |
| 1 | 1 |     1     |
| 1 | 0 |     1     |
| 1 | 0 |     1     |
| 0 | 1 |     1     |
| 0 | 1 |     1     |
| 0 | 0 |     0     |
| 0 | 0 |     0     |

#### Paso 3.2: Calcular $\neg P$

$\neg P$ es lo opuesto a $P$.

| P | $\neg P$ |
|---|----------|
| 1 |    0     |
| 1 |    0     |
| 1 |    0     |
| 1 |    0     |
| 0 |    1     |
| 0 |    1     |
| 0 |    1     |
| 0 |    1     |

#### Paso 3.3: Calcular $R \rightarrow \neg P$

$R \rightarrow \neg P$ es 0 solo si $R$ es 1 y $\neg P$ es 0.

| R | $\neg P$ | $R \rightarrow \neg P$ |
|---|----------|------------------------|
| 1 |    0     |          0             |
| 0 |    0     |          1             |
| 1 |    0     |          0             |
| 0 |    0     |          1             |
| 1 |    1     |          1             |
| 0 |    1     |          1             |
| 1 |    1     |          1             |
| 0 |    1     |          1             |

#### Paso 3.4: Calcular $(P \lor Q) \land (R \rightarrow \neg P)$

Esto es $A$, la parte izquierda de la implicación. Es 1 solo si ambas partes son 1.

| $P \lor Q$ | $R \rightarrow \neg P$ | $(P \lor Q) \land (R \rightarrow \neg P)$ |
|------------|------------------------|-------------------------------------------|
|     1      |          0             |                    0                     |
|     1      |          1             |                    1                     |
|     1      |          0             |                    0                     |
|     1      |          1             |                    1                     |
|     1      |          1             |                    1                     |
|     1      |          1             |                    1                     |
|     0      |          1             |                    0                     |
|     0      |          1             |                    0                     |

#### Paso 3.5: Calcular $\neg Q$

$\neg Q$ es lo opuesto a $Q$.

| Q | $\neg Q$ |
|---|----------|
| 1 |    0     |
| 1 |    0     |
| 0 |    1     |
| 0 |    1     |
| 1 |    0     |
| 1 |    0     |
| 0 |    1     |
| 0 |    1     |

#### Paso 3.6: Calcular $\neg R$

$\neg R$ es lo opuesto a $R$.

| R | $\neg R$ |
|---|----------|
| 1 |    0     |
| 0 |    1     |
| 1 |    0     |
| 0 |    1     |
| 1 |    0     |
| 0 |    1     |
| 1 |    0     |
| 0 |    1     |

#### Paso 3.7: Calcular $\neg Q \rightarrow \neg R$

Esto es $B$, la parte derecha de la implicación. $\neg Q \rightarrow \neg R$ es 0 solo si $\neg Q$ es 1 y $\neg R$ es 0.

| $\neg Q$ | $\neg R$ | $\neg Q \rightarrow \neg R$ |
|----------|----------|-----------------------------|
|    0     |    0     |            1                |
|    0     |    1     |            1                |
|    1     |    0     |            0                |
|    1     |    1     |            1                |
|    0     |    0     |            1                |
|    0     |    1     |            1                |
|    1     |    0     |            0                |
|    1     |    1     |            1                |

#### Paso 3.8: Calcular la implicación completa $A \rightarrow B$

Ahora juntamos $A$ y $B$. La implicación $A \rightarrow B$ es 0 solo si $A$ es 1 y $B$ es 0.

| $(P \lor Q) \land (R \rightarrow \neg P)$ | $\neg Q \rightarrow \neg R$ | $[(P \lor Q) \land (R \rightarrow \neg P)] \rightarrow (\neg Q \rightarrow \neg R)$ |
|-------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------|
|                    0                     |            1                |                               1                               |
|                    1                     |            1                |                               1                               |
|                    0                     |            0                |                               1                               |
|                    1                     |            1                |                               1                               |
|                    1                     |            1                |                               1                               |
|                    1                     |            1                |                               1                               |
|                    0                     |            0                |                               1                               |
|                    0                     |            1                |                               1                               |

### Paso 4: Analizar el resultado

Mira la última columna, que es la proposición completa:

$$[(P \lor Q) \land (R \rightarrow \neg P)] \rightarrow (\neg Q \rightarrow \neg R)$$

Todos los valores son 1. Esto significa que la proposición es siempre verdadera (una tautología). En otras palabras, no importa si llueve, hace sol o salgo a correr, la implicación siempre se cumple.

### Paso 5: Concluir

La proposición $[(P \lor Q) \land (R \rightarrow \neg P)] \rightarrow (\neg Q \rightarrow \neg R)$ es una tautología, porque la tabla de verdad muestra que siempre es 1. Esto significa que la implicación es correcta y siempre se cumple.
