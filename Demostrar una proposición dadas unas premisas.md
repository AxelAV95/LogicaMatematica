
# Guía: Cómo demostrar una proposición dadas unas premisas

## ¿Qué tipo de ejercicio es este?

Este tipo de ejercicio te da varias afirmaciones (las premisas) que sabes que son ciertas, y te pide demostrar otra afirmación (el objetivo o conclusión) usando las premisas. Para hacerlo, usamos las leyes de la lógica y las reglas de inferencia para conectar las premisas y llegar al objetivo, paso a paso.

El ejercicio que resolvimos fue:

**Premisas:**
1. $¬(P∨¬Q)$
2. $R→¬Q$
3. $S∨R$
4. $T→P$

**Objetivo:** $¬(T∨¬S)$

Queríamos demostrar que $¬(T∨¬S)$ se deduce de las premisas.

## Herramientas que necesitas saber de antemano

### Símbolos lógicos y su significado (con ejemplos cotidianos):

- **¬**: "No". Cambia el valor. Ejemplo: Si $P$ es "hoy llueve" y es cierto, entonces $¬P$ ("no llueve hoy") es no cierto.
- **∨**: "O". Es cierto si al menos una de las dos cosas es cierta. Ejemplo: Si $P$ es "hoy llueve" y $Q$ es "hace sol", $P∨Q$ ("hoy llueve o hace sol") es cierto si llueve, o hace sol, o ambas cosas.
- **∧**: "Y". Es cierto solo si ambas cosas son ciertas. Ejemplo: $P∧Q$ ("hoy llueve y hace sol") es cierto solo si llueve y hace sol al mismo tiempo.
- **→**: "Si... entonces...". Es no cierto solo si la primera parte es cierta y la segunda no lo es. Ejemplo: Si $T$ es "estudio mucho" y $P$ es "saco buena nota", $T→P$ ("si estudio mucho, entonces saco buena nota") es no cierto solo si estudio mucho pero no saco buena nota.

### Leyes de la lógica (para simplificar expresiones):

1. **Ley de De Morgan**:
   - $¬(A∨B)$ se convierte en $¬A∧¬B$. Ejemplo: "No (llueve o hace sol)" es lo mismo que "no llueve y no hace sol".
   - $¬(A∧B)$ se convierte en $¬A∨¬B$. Ejemplo: "No (llueve y hace sol)" es lo mismo que "no llueve o no hace sol".

2. **Doble negación**: $¬(¬A)$ se convierte en $A$. Ejemplo: "No (no llueve)" es lo mismo que "llueve".

3. **Definición de implicación**: $A→B$ es lo mismo que $¬A∨B$. Ejemplo: "Si llueve, entonces hace frío" es lo mismo que "no llueve o hace frío".

4. **Distributiva**: $A∧(B∨C)$ es lo mismo que $(A∧B)∨(A∧C)$. Ejemplo: "Llueve y (hace sol o hace frío)" es lo mismo que "(llueve y hace sol) o (llueve y hace frío)".

5. **Simplificación**:
   - Si tienes $A∨B$ y $B$ no es cierto, entonces $A$ debe ser cierto. Ejemplo: Si "llueve o hace sol" y "no hace sol", entonces "llueve".
   - $A∧(B∨C)$ es lo mismo que $(A∧B)∨(A∧C)$.

### Reglas de inferencia (para deducir cosas):

1. **Modus Ponens**: Si tienes $A→B$ y $A$ es cierto, entonces $B$ es cierto. Ejemplo: Si "si llueve, entonces hace frío" y "llueve", entonces "hace frío".
2. **Modus Tollens**: Si tienes $A→B$ y $¬B$ es cierto, entonces $¬A$ es cierto. Ejemplo: Si "si llueve, entonces hace frío" y "no hace frío", entonces "no llueve".
3. **Silogismo hipotético**: Si tienes $A→B$ y $B→C$, entonces $A→C$. Ejemplo: Si "si estudio, entonces aprendo" y "si aprendo, entonces paso el examen", entonces "si estudio, entonces paso el examen".
4. **Conjunción**: Si $A$ es cierto y $B$ es cierto, entonces $A∧B$ es cierto. Ejemplo: Si "llueve" y "hace frío", entonces "llueve y hace frío".
5. **Simplificación**: Si tienes $A∨B$ y $A$ no es cierto, entonces $B$ debe ser cierto. Ejemplo: Si "llueve o hace sol" y "no llueve", entonces "hace sol".

**Qué hacer**: Escribe estas leyes y reglas en un papel para tenerlas a la mano mientras resuelves el ejercicio.

## Paso a paso para resolver el ejercicio

### Paso 1: Entender las premisas y el objetivo

**Premisas:**
1. $¬(P∨¬Q)$
2. $R→¬Q$
3. $S∨R$
4. $T→P$

**Objetivo:** $¬(T∨¬S)$

**Ejemplo cotidiano**: Piensa que:
- $P$: "hoy llueve"
- $Q$: "hace sol"
- $R$: "salgo a correr"
- $S$: "leo un libro"
- $T$: "veo televisión"

Las premisas serían:
1. "No es cierto que (hoy llueve o no hace sol)"
2. "Si salgo a correr, entonces no hace sol"
3. "Leo un libro o salgo a correr"
4. "Si veo televisión, entonces hoy llueve"

Y el objetivo es: "No es cierto que (veo televisión o no leo un libro)".

**Qué hacer**: Escribe las premisas y el objetivo. Si te ayuda, asigna significados cotidianos a las letras para entender mejor lo que significan.

### Paso 2: Simplificar el objetivo

El objetivo es $¬(T∨¬S)$. Vamos a simplificarlo para ver qué necesitamos demostrar:

1. Usamos la Ley de De Morgan:
   $$¬(T∨¬S) \text{ se convierte en } ¬T∧¬(¬S)$$

2. Aplicamos la doble negación:
   $$¬(¬S) \text{ se convierte en } S$$

Entonces, el objetivo se convierte en:
$$¬T∧S$$

**Ejemplo cotidiano**: "No es cierto que (veo televisión o no leo un libro)" es lo mismo que "no veo televisión y leo un libro".

Esto significa que para demostrar $¬(T∨¬S)$, necesitamos demostrar que:
1. $¬T$ es cierto (no veo televisión), y
2. $S$ es cierto (leo un libro).

**Qué hacer**: Usa las leyes de la lógica (como la Ley de De Morgan y la doble negación) para simplificar el objetivo y ver qué necesitas demostrar.

### Paso 3: Simplificar las premisas

Vamos a simplificar las premisas para que sean más fáciles de trabajar.

**Premisa 1**: $¬(P∨¬Q)$
1. Usamos la Ley de De Morgan:
   $$¬(P∨¬Q) \text{ se convierte en } ¬P∧¬(¬Q)$$

2. Aplicamos la doble negación:
   $$¬(¬Q) \text{ se convierte en } Q$$

Entonces, la premisa 1 se convierte en:
$$¬P∧Q$$

Esto nos dice que:
- $¬P$ es cierto (no llueve hoy)
- $Q$ es cierto (hace sol)

**Ejemplo cotidiano**: "No es cierto que (hoy llueve o no hace sol)" es lo mismo que "no llueve y hace sol".

**Premisa 2**: $R→¬Q$
Usamos la definición de implicación:
$$R→¬Q \text{ se convierte en } ¬R∨¬Q$$

**Ejemplo cotidiano**: "Si salgo a correr, entonces no hace sol" es lo mismo que "no salgo a correr o no hace sol".

**Premisa 3**: $S∨R$
Esto ya está simplificado: "Leo un libro o salgo a correr".

**Premisa 4**: $T→P$
Usamos la definición de implicación:
$$T→P \text{ se convierte en } ¬T∨P$$

**Ejemplo cotidiano**: "Si veo televisión, entonces hoy llueve" es lo mismo que "no veo televisión o llueve".

**Qué hacer**: Usa las leyes de la lógica (como la Ley de De Morgan, doble negación, definición de implicación) para simplificar las premisas y extraer información útil.

### Paso 4: Buscar lo que necesitas para el objetivo

Queremos demostrar $¬T∧S$. Esto significa que necesitamos:
1. Demostrar que $¬T$ es cierto (no veo televisión)
2. Demostrar que $S$ es cierto (leo un libro)

Vamos a buscar estas dos cosas por separado.

#### Paso 4.1: Demostrar que $¬T$ es cierto

Miremos las premisas que tienen $T$. La premisa 4 dice:
$$T→P \text{, que es lo mismo que } ¬T∨P$$

Esto significa que al menos una de estas dos debe ser cierta:
1. $¬T$ (no veo televisión), o
2. $P$ (hoy llueve)

De la premisa 1 ($¬P∧Q$), ya sabemos que:
- $¬P$ es cierto (no llueve hoy)

Si $¬P$ es cierto, entonces $P$ no puede ser cierto.

**Ejemplo cotidiano**: Sabemos que "no llueve hoy" ($¬P$), así que "llueve" ($P$) no puede ser cierto.

Regresemos a la premisa 4 ($¬T∨P$):
- No podemos usar $P$ como cierto, porque $¬P$ es cierto
- Entonces: $¬T∨P$ se convierte en $¬T∨ \text{no cierto}$

Usamos la simplificación: Si tienes $A∨B$ y $B$ no es cierto, entonces $A$ debe serlo para que la premisa sea cierta. Aquí, $A$ es $¬T$, $B$ es $P$, y $P$ no es cierto, así que:
$$¬T∨ \text{no cierto} \text{ significa que } ¬T \text{ debe ser cierto}$$

La premisa 4 debe ser cierta (porque es una premisa), así que $¬T$ es cierto.

**Ejemplo cotidiano**: La premisa 4 dice "no veo televisión o llueve". Pero sabemos que no llueve ($¬P$), así que para que la premisa sea cierta, debe ser cierto que no veo televisión ($¬T$).

Hemos encontrado que $¬T$ es cierto.

**Qué hacer**: Busca premisas que tengan las letras que necesitas (como $T$) y usa simplificación o Modus Tollens para deducir información.

#### Paso 4.2: Demostrar que $S$ es cierto

Miremos las premisas que tienen $S$. La premisa 3 dice:
$$S∨R \text{ (leo un libro o salgo a correr)}$$

Esto significa que al menos una de las dos es cierta. No sabemos cuál todavía, así que necesitamos información sobre $R$.

Vamos a la premisa 2:
$$R→¬Q \text{, que es lo mismo que } ¬R∨¬Q$$

De la premisa 1 ($¬P∧Q$), sabemos que:
- $Q$ es cierto (hace sol)

Si $Q$ es cierto, entonces $¬Q$ no puede serlo.

**Ejemplo cotidiano**: Sabemos que "hace sol" ($Q$), así que "no hace sol" ($¬Q$) no puede ser cierto.

Sustituimos en la premisa 2 ($¬R∨¬Q$):
$$¬R∨¬Q \text{ se convierte en } ¬R∨ \text{no cierto}$$

Usamos la simplificación:
$$¬R∨ \text{no cierto} \text{ significa que } ¬R \text{ debe ser cierto}$$

La premisa 2 debe ser cierta, así que $¬R$ es cierto, lo que significa que $R$ no es cierto.

**Ejemplo cotidiano**: La premisa 2 dice "no salgo a correr o no hace sol". Pero sabemos que hace sol ($Q$), así que "no hace sol" no es cierto. Para que la premisa sea cierta, debe ser cierto que no salgo a correr ($¬R$).

Regresemos a la premisa 3 ($S∨R$):
- Sabemos que $R$ no es cierto ($¬R$)
- Entonces: $S∨R$ se convierte en $S∨ \text{no cierto}$

Usamos la simplificación:
$$S∨ \text{no cierto} \text{ es lo mismo que } S$$

La premisa 3 debe ser cierta, así que $S$ debe ser cierto.

**Ejemplo cotidiano**: La premisa 3 dice "leo un libro o salgo a correr". Pero sabemos que no salgo a correr ($¬R$), así que para que la premisa sea cierta, debe ser cierto que leo un libro ($S$).

Hemos encontrado que $S$ es cierto.

**Qué hacer**: Busca premisas que tengan las letras que necesitas (como $S$) y usa simplificación o Modus Tollens para deducir información. Conecta las premisas para eliminar variables que no necesitas.

### Paso 5: Juntar lo que encontraste

Queríamos demostrar $¬T∧S$. Ya sabemos que:
1. $¬T$ es cierto (no veo televisión, del paso 4.1)
2. $S$ es cierto (leo un libro, del paso 4.2)

Usamos la regla de conjunción: Si $A$ es cierto y $B$ es cierto, entonces $A∧B$ es cierto. Aquí, $A$ es $¬T$, $B$ es $S$:
$$¬T∧S$$

Y como $¬T∧S$ es lo mismo que $¬(T∨¬S)$ (lo vimos en el paso 2), ¡hemos demostrado el objetivo!

**Ejemplo cotidiano**: Queríamos demostrar "no veo televisión y leo un libro". Ya sabemos que no veo televisión ($¬T$) y que leo un libro ($S$), así que podemos juntarlas: "no veo televisión y leo un libro", que es lo mismo que "no es cierto que (veo televisión o no leo un libro)".

**Qué hacer**: Si tu objetivo es un "y" ($A∧B$), y ya demostraste que $A$ y $B$ son ciertos, júntalos con la regla de conjunción.

### Paso 6: Justificar cada paso

Escribe los pasos con las leyes o reglas que usaste:

1. Simplificamos el objetivo:
   $$¬(T∨¬S) \text{ se convierte en } ¬T∧S \text{ (Ley de De Morgan y doble negación)}$$

2. Simplificamos la premisa 1:
   $$¬(P∨¬Q) \text{ se convierte en } ¬P∧Q \text{ (Ley de De Morgan y doble negación, Premisa 1)}$$
   Esto nos dice que $¬P$ es cierto y $Q$ es cierto.

3. Usamos la premisa 4 para encontrar $¬T$:
   $$T→P \text{ se convierte en } ¬T∨P \text{ (definición de implicación, Premisa 4)}$$
   Como $¬P$ es cierto (por el paso 2), $P$ no es cierto, así que:
   $$¬T∨ \text{no cierto} \text{ es lo mismo que } ¬T \text{ (simplificación)}$$
   Para que la premisa 4 sea cierta, $¬T$ debe ser cierto.

4. Usamos la premisa 2 para encontrar información sobre $R$:
   $$R→¬Q \text{ se convierte en } ¬R∨¬Q \text{ (definición de implicación, Premisa 2)}$$
   Como $Q$ es cierto (por el paso 2), $¬Q$ no es cierto, así que:
   $$¬R∨ \text{no cierto} \text{ es lo mismo que } ¬R \text{ (simplificación)}$$
   Para que la premisa 2 sea cierta, $¬R$ debe ser cierto, así que $R$ no es cierto.

5. Usamos la premisa 3 para encontrar $S$:
   $$S∨R \text{ (Premisa 3)}$$
   Como $R$ no es cierto (por el paso 4):
   $$S∨ \text{no cierto} \text{ es lo mismo que } S \text{ (simplificación)}$$
   Para que la premisa 3 sea cierta, $S$ debe ser cierto.

6. Juntamos todo:
   $$¬T∧S \text{ (conjunción de los pasos 3 y 5)}$$
   $$¬T∧S \text{ es lo mismo que } ¬(T∨¬S) \text{ (por el paso 1, Ley de De Morgan)}$$

**Qué hacer**: Justifica cada paso diciendo qué ley o regla usaste (como Ley de De Morgan, simplificación, etc.).

## Herramientas aplicadas en cada paso

- **Paso 1 (Entender las premisas y el objetivo)**: Conocer los símbolos y escribir las premisas y el objetivo.
- **Paso 2 (Simplificar el objetivo)**: Usa leyes como la Ley de De Morgan y doble negación.
- **Paso 3 (Simplificar las premisas)**: Usa leyes como la Ley de De Morgan, doble negación, definición de implicación.
- **Paso 4 (Buscar lo que necesitas)**:
  - Usa simplificación para deducir cosas nuevas.
  - Usa Modus Tollens o Modus Ponens para conectar premisas.
  - Busca letras comunes entre las premisas para combinarlas.
- **Paso 5 (Juntar lo que encontraste)**: Usa la conjunción si el objetivo es un "y" ($A∧B$).
- **Paso 6 (Justificar)**: Escribe las leyes o reglas que usaste en cada paso.

## Consejos 

- **Ve despacio**: Simplifica una premisa a la vez y revisa que cada paso sea correcto.
- **Usa ejemplos cotidianos**: Piensa en las letras como cosas simples (como "llueve", "leo un libro") para entender mejor lo que significan las premisas.
- **Escribe todo**: Anota lo que vas encontrando (por ejemplo, "$¬P$ es cierto", "$R$ no es cierto").
- **Busca conexiones**: Mira qué letras (como $P,Q,R$) aparecen en varias premisas y úsalas para conectarlas con reglas como Modus Tollens o simplificación.
- **Practica las reglas**: Las leyes de De Morgan y las reglas como simplificación son muy comunes. Practica con ejemplos pequeños.
