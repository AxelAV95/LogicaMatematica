# Guía: Cómo transformar textos a proposiciones y premisas, y validar la conclusión con reglas de lógica e inferencia

## ¿Qué tipo de ejercicio es este?

Este tipo de ejercicio te da un texto en lenguaje normal (como una conversación) que contiene varias afirmaciones (premisas) y una conclusión. Tu tarea es:

- Convertir el texto en símbolos lógicos (proposiciones).
- Identificar las premisas (lo que sabes que es cierto) y la conclusión (lo que quieres demostrar).
- Usar las leyes de la lógica y las reglas de inferencia para demostrar que la conclusión se deduce de las premisas.

El ejercicio que resolvimos fue:

"Si practico deportes, entonces mejoro mi salud. Si voy al gimnasio, entonces practico deportes. Voy al gimnasio o como saludable. Si no como saludable o no descanso, entonces no mejoro mi salud. Por lo tanto, como saludable."

## Herramientas que necesitas saber de antemano

Antes de empezar, necesitas conocer estas cosas básicas:

### Símbolos lógicos y su significado (con ejemplos cotidianos):

- **¬ (Negación):** "No". Cambia el valor. Ejemplo: Si $P$ es "hoy llueve" y es cierto, entonces $\neg P$ ("no llueve hoy") es no cierto.
- **∨ (Disyunción):** "O". Es cierto si al menos una de las dos cosas es cierta. Ejemplo: Si $P$ es "hoy llueve" y $Q$ es "hace sol", $P \lor Q$ ("hoy llueve o hace sol") es cierto si llueve, o hace sol, o ambas cosas.
- **∧ (Conjunción):** "Y". Es cierto solo si ambas cosas son ciertas. Ejemplo: $P \land Q$ ("hoy llueve y hace sol") es cierto solo si llueve y hace sol al mismo tiempo.
- **→ (Implicación):** "Si... entonces...". Es no cierto solo si la primera parte es cierta y la segunda no lo es. Ejemplo: Si $R$ es "estudio mucho" y $S$ es "saco buena nota", $R \rightarrow S$ ("si estudio mucho, entonces saco buena nota") es no cierto solo si estudio mucho pero no saco buena nota.

### Leyes de la lógica (para simplificar expresiones):

- **Ley de De Morgan:**
  - $\neg (A \lor B)$ se convierte en $\neg A \land \neg B$. Ejemplo: "No (llueve o hace sol)" es lo mismo que "no llueve y no hace sol".
  - $\neg (A \land B)$ se convierte en $\neg A \lor \neg B$. Ejemplo: "No (llueve y hace sol)" es lo mismo que "no llueve o no hace sol".
- **Doble negación:** $\neg (\neg A)$ se convierte en $A$. Ejemplo: "No (no llueve)" es lo mismo que "llueve".
- **Definición de implicación:** $A \rightarrow B$ es lo mismo que $\neg A \lor B$. Ejemplo: "Si llueve, entonces hace frío" es lo mismo que "no llueve o hace frío".
- **Distributiva:** $A \land (B \lor C)$ es lo mismo que $(A \land B) \lor (A \land C)$. Ejemplo: "Llueve y (hace sol o hace frío)" es lo mismo que "(llueve y hace sol) o (llueve y hace frío)".

### Reglas de inferencia (para deducir cosas):

- **Modus Ponens:** Si tienes $A \rightarrow B$ y $A$ es cierto, entonces $B$ es cierto. Ejemplo: Si "si llueve, entonces hace frío" y "llueve", entonces "hace frío".
- **Modus Tollens:** Si tienes $A \rightarrow B$ y $\neg B$ es cierto, entonces $\neg A$ es cierto. Ejemplo: Si "si llueve, entonces hace frío" y "no hace frío", entonces "no llueve".
- **Silogismo hipotético:** Si tienes $A \rightarrow B$ y $B \rightarrow C$, entonces $A \rightarrow C$. Ejemplo: Si "si voy al gimnasio, entonces practico deportes" y "si practico deportes, entonces estoy sano", entonces "si voy al gimnasio, entonces estoy sano".
- **Simplificación:** Si tienes $A \lor B$ y $A$ no es cierto, entonces $B$ debe ser cierto. Ejemplo: Si "llueve o hace sol" y "no llueve", entonces "hace sol".

## Paso a paso para resolver el ejercicio

### Paso 1: Convertir el texto en proposiciones (forma simbólica)

El texto es:

"Si practico deportes, entonces mejoro mi salud. Si voy al gimnasio, entonces practico deportes. Voy al gimnasio o como saludable. Si no como saludable o no descanso, entonces no mejoro mi salud. Por lo tanto, como saludable."

Primero, asignamos letras a cada afirmación simple:

- $P$: "Practico deportes". Ejemplo: "Hago fútbol los fines de semana".
- $S$: "Mejoro mi salud". Ejemplo: "Me siento más fuerte y sano".
- $G$: "Voy al gimnasio". Ejemplo: "Voy al gym tres veces por semana".
- $C$: "Como saludable". Ejemplo: "Como ensaladas y frutas todos los días".
- $D$: "Descanso". Ejemplo: "Duermo 8 horas cada noche".

Ahora, traducimos cada frase a símbolos:

- "Si practico deportes, entonces mejoro mi salud."
  - Esto es "si $P$, entonces $S$". En símbolos: $P \rightarrow S$.
  - Ejemplo: "Si hago fútbol, entonces me siento más sano".
- "Si voy al gimnasio, entonces practico deportes."
  - Esto es "si $G$, entonces $P$". En símbolos: $G \rightarrow P$.
  - Ejemplo: "Si voy al gym, entonces hago fútbol".
- "Voy al gimnasio o como saludable."
  - Esto es $G$ o $C$. En símbolos: $G \lor C$.
  - Ejemplo: "Voy al gym o como ensaladas".
- "Si no como saludable o no descanso, entonces no mejoro mi salud."
  - "No como saludable" es $\neg C$.
  - "No descanso" es $\neg D$.
  - "No como saludable o no descanso" es $\neg C \lor \neg D$.
  - "No mejoro mi salud" es $\neg S$.
  - Esto es "si $\neg C \lor \neg D$, entonces $\neg S$". En símbolos: $(\neg C \lor \neg D) \rightarrow \neg S$.
  - Ejemplo: "Si no como ensaladas o no duermo 8 horas, entonces no me siento sano".
- "Por lo tanto, como saludable."
  - Esto es la conclusión: $C$.
  - Ejemplo: "Entonces, como ensaladas".

### Resumen:

- Premisa 1: $P \rightarrow S$
- Premisa 2: $G \rightarrow P$
- Premisa 3: $G \lor C$
- Premisa 4: $(\neg C \lor \neg D) \rightarrow \neg S$
- Conclusión: $C$

### Paso 2: Simplificar las premisas (si es necesario)

Algunas premisas pueden ser más fáciles de trabajar si las simplificamos usando las leyes de la lógica. Vamos a simplificar la premisa 4:

$(\neg C \lor \neg D) \rightarrow \neg S$

Usamos la definición de implicación: $A \rightarrow B$ es lo mismo que $\neg A \lor B$. Aquí, $A$ es $\neg C \lor \neg D$ y $B$ es $\neg S$:

$(\neg C \lor \neg D) \rightarrow \neg S$ se convierte en $\neg (\neg C \lor \neg D) \lor \neg S$

Ahora, usamos la Ley de De Morgan para simplificar $\neg (\neg C \lor \neg D)$:

$\neg (\neg C \lor \neg D)$ se convierte en $\neg (\neg C) \land \neg (\neg D)$

Y aplicamos la doble negación: $\neg (\neg C)$ es $C$, $\neg (\neg D)$ es $D$:

$\neg (\neg C) \land \neg (\neg D)$ se convierte en $C \land D$

Entonces, la premisa 4 se convierte en:

$(C \land D) \lor \neg S$

Ejemplo cotidiano: Esto es como decir: "(Como ensaladas y duermo 8 horas) o no me siento sano". Para que esta afirmación sea cierta, al menos una de las dos partes debe serlo: o como bien y duermo bien, o no estoy sano.

### Paso 3: Combinar las premisas para deducir información

Ahora usamos las premisas para deducir cosas nuevas que nos ayuden a llegar a la conclusión ($C$).

#### Paso 3.1: Combinar las premisas 1 y 2

- Premisa 1: $P \rightarrow S$ ("Si practico deportes, entonces mejoro mi salud").
- Premisa 2: $G \rightarrow P$ ("Si voy al gimnasio, entonces practico deportes").

Usamos la regla de inferencia silogismo hipotético: Si tienes $A \rightarrow B$ y $B \rightarrow C$, entonces $A \rightarrow C$. Aquí:

- $G \rightarrow P$ (si voy al gimnasio, entonces practico deportes).
- $P \rightarrow S$ (si practico deportes, entonces mejoro mi salud).

Entonces, deducimos:

$G \rightarrow S$ (si voy al gimnasio, entonces mejoro mi salud)

Ejemplo cotidiano: Si "voy al gym, entonces hago fútbol" y "hago fútbol, entonces estoy sano", entonces "voy al gym, entonces estoy sano".

#### Paso 3.2: Usar la premisa 3

La premisa 3 es:

$G \lor C$ (voy al gimnasio o como saludable)

Esto nos dice que al menos una de las dos es cierta: o $G$ es cierto, o $C$ es cierto. Como nuestro objetivo es demostrar $C$, vamos a considerar ambos casos (esto se llama disyunción de casos).

Ejemplo cotidiano: Esto es como decir "o voy al gym o como ensaladas". No sabemos cuál es cierta, así que probaremos qué pasa si voy al gym y qué pasa si no voy.

#### Paso 3.3: Usar $G \rightarrow S$ y la premisa 4

Sabemos que:

$G \rightarrow S$ (si voy al gimnasio, entonces mejoro mi salud)

Reescribimos $G \rightarrow S$ usando la definición de implicación:

$\neg G \lor S$

Y tenemos la premisa 4 simplificada:

$(C \land D) \lor \neg S$

Esto significa que al menos una de las dos debe ser cierta: o $C \land D$ es cierto (como saludable y descanso), o $\neg S$ es cierto (no mejoro mi salud).

Ejemplo cotidiano: Esto es como decir: "O (como ensaladas y duermo 8 horas) o no estoy sano". Si estoy sano ($S$ es cierto), entonces la segunda parte ($\neg S$) no es cierta, así que la primera ($C \land D$) debe serlo.

Vamos a combinar esta información con $\neg G \lor S$:

Si $S$ es cierto (mejoro mi salud), entonces:

$(C \land D) \lor \neg S$ se convierte en $(C \land D) \lor \text{no cierto}$

$(C \land D) \lor \text{no cierto}$ es lo mismo que $C \land D$ (simplificación)

Para que la premisa 4 sea cierta, $C \land D$ debe ser cierto, lo que significa:

- $C$ es cierto (como saludable).
- $D$ es cierto (descanso).

Esto nos dice que si $S$ es cierto, entonces $C$ es cierto, que es un paso hacia nuestra conclusión.

#### Paso 3.4: Considerar los casos de $G \lor C$

Volvamos a la premisa 3 ($G \lor C$) y usemos $G \rightarrow S$:

- Caso 1: $G$ es cierto (voy al gimnasio).
  - Si $G$ es cierto, entonces por $G \rightarrow S$, $S$ es cierto (mejoro mi salud).
  - Si $S$ es cierto, entonces por la premisa 4 ($(C \land D) \lor \neg S$), $C \land D$ debe ser cierto (como vimos en el paso anterior).
  - Si $C \land D$ es cierto, entonces $C$ es cierto (como saludable).
- Caso 2: $G$ no es cierto ($\neg G$ es cierto, no voy al gimnasio).
  - Si $G$ no es cierto, entonces por $G \lor C$, $C$ debe ser cierto (porque si $G$ no es cierto, la única manera de que $G \lor C$ sea cierto es que $C$ lo sea).
  - Esto significa que $C$ es cierto (como saludable).

Ejemplo cotidiano: Si voy al gym ($G$), entonces estoy sano ($S$), y si estoy sano, entonces como ensaladas y duermo bien, así que como ensaladas ($C$). Si no voy al gym, entonces por "voy al gym o como ensaladas", debo comer ensaladas ($C$).

### Paso 4: Llegar a la conclusión

En ambos casos (si $G$ es cierto o no), llegamos a que $C$ es cierto:

- Si $G$ es cierto, entonces $S$ es cierto, y por la premisa 4, $C \land D$ es cierto, así que $C$ es cierto.
- Si $G$ no es cierto, entonces por $G \lor C$, $C$ es cierto.

Por lo tanto, la conclusión $C$ (como saludable) es válida.

### Paso 5: Justificar cada paso

Escribe los pasos con las leyes o reglas que usaste:

- Traducimos el texto a símbolos:
  - Premisa 1: $P \rightarrow S$ (dado).
  - Premisa 2: $G \rightarrow P$ (dado).
  - Premisa 3: $G \lor C$ (dado).
  - Premisa 4: $(\neg C \lor \neg D) \rightarrow \neg S$ (dado).
  - Conclusión: $C$.
- Simplificamos la premisa 4:
  - $(\neg C \lor \neg D) \rightarrow \neg S$ se convierte en $\neg (\neg C \lor \neg D) \lor \neg S$ (definición de implicación).
  - $\neg (\neg C \lor \neg D)$ se convierte en $C \land D$ (Ley de De Morgan y doble negación).
  - $(C \land D) \lor \neg S$.
- Combinamos las premisas 1 y 2:
  - $G \rightarrow P$ y $P \rightarrow S$ implica $G \rightarrow S$ (silogismo hipotético).
- Usamos $G \rightarrow S$ y $G \lor C$:
  - Caso 1: Si $G$ es cierto, entonces $S$ es cierto (Modus Ponens).
  - Si $S$ es cierto, entonces $(C \land D) \lor \neg S$ se convierte en $C \land D$ (simplificación).
  - Caso 2: Si $G$ no es cierto, entonces por $G \lor C$, $C$ debe ser cierto (simplificación).
- Conclusión:
  - $C$ es cierto en ambos casos (disyunción de casos).

## Herramientas aplicadas en cada paso

- Paso 1 (Convertir el texto a símbolos): Herramienta: Conocer los símbolos ($\neg$, $\lor$, $\land$, $\rightarrow$) y cómo traducir frases como "si... entonces...", "o", "y", "no". No necesitas leyes aquí, solo entender el lenguaje.
- Paso 2 (Simplificar las premisas): Herramienta: Usa leyes de la lógica como la definición de implicación, Ley de De Morgan, doble negación para hacer las premisas más fáciles.
- Paso 3 (Combinar las premisas):
  - Usa reglas de inferencia como Modus Ponens, Modus Tollens, silogismo hipotético.
  - Usa disyunción de casos para manejar $A \lor B$.
  - Usa simplificación para deducir cosas nuevas.
- Paso 4 (Llegar a la conclusión): Herramienta: Verifica si la conclusión se cumple en todos los casos posibles.
- Paso 5 (Justificar): Herramienta: Escribe las leyes o reglas que usaste en cada paso.

## Consejos
- Toma tu tiempo: Traduce el texto con cuidado para no equivocarte al asignar símbolos.
- Usa ejemplos cotidianos: Piensa en las letras como cosas simples (como "llueve", "como ensaladas") para entender mejor lo que dice el texto.
- Escribe todo: Anota las premisas y la conclusión en un papel para no perderte.
- Busca conexiones: Mira qué letras (como $G$, $P$, $S$) aparecen en varias premisas y úsalas para conectarlas con reglas como el silogismo hipotético.
- Practica las reglas: Las leyes de De Morgan y las reglas como Modus Ponens son muy comunes. Practica con ejemplos pequeños.
