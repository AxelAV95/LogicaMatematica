# Guía para principiantes: Cómo aplicar leyes de la lógica para comprobar equivalencias

## ¿Qué tipo de ejercicio es este?

Este tipo de ejercicio te pide verificar si dos expresiones lógicas son equivalentes, es decir, si siempre tienen el mismo valor de verdad (ambas son ciertas o ambas no son ciertas) para cualquier combinación de valores de las variables. Para hacerlo, usamos las leyes de la lógica para simplificar una o ambas expresiones hasta que sean iguales (o mostremos que no lo son).

El ejercicio que resolvimos fue:

$$(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(R→P) ≡ ¬P$$

Queríamos comprobar si el lado izquierdo es equivalente al lado derecho ($¬P$).

## Herramientas que necesitas saber de antemano

Antes de empezar, necesitas conocer estas cosas básicas:

### Símbolos lógicos y su significado (con ejemplos cotidianos):

- **¬**: "No". Cambia el valor. Ejemplo: Si $P$ es "hoy llueve" y es cierto, entonces $¬P$ ("no llueve hoy") es no cierto.
- **∧**: "Y". Es cierto solo si ambas cosas son ciertas. Ejemplo: $P∧Q$ ("hoy llueve y hace sol") es cierto solo si llueve y hace sol al mismo tiempo.
- **∨**: "O". Es cierto si al menos una de las dos cosas es cierta. Ejemplo: $P∨Q$ ("hoy llueve o hace sol") es cierto si llueve, o hace sol, o ambas cosas.
- **→**: "Si... entonces...". Es no cierto solo si la primera parte es cierta y la segunda no lo es. Ejemplo: Si $R$ es "estudio mucho" y $P$ es "saco buena nota", $R→P$ ("si estudio mucho, entonces saco buena nota") es no cierto solo si estudio mucho pero no saco buena nota.

### Leyes de la lógica (para simplificar expresiones):

1. **Ley de De Morgan**:
   - $¬(A∨B)$ se convierte en $¬A∧¬B$. Ejemplo: "No (llueve o hace sol)" es lo mismo que "no llueve y no hace sol".
   - $¬(A∧B)$ se convierte en $¬A∨¬B$. Ejemplo: "No (llueve y hace sol)" es lo mismo que "no llueve o no hace sol".

2. **Doble negación**: $¬(¬A)$ se convierte en $A$. Ejemplo: "No (no llueve)" es lo mismo que "llueve".

3. **Definición de implicación**: $A→B$ es lo mismo que $¬A∨B$. Ejemplo: "Si llueve, entonces hace frío" es lo mismo que "no llueve o hace frío".

4. **Distributiva**:
   - $A∧(B∨C)$ es lo mismo que $(A∧B)∨(A∧C)$. Ejemplo: "Llueve y (hace sol o hace frío)" es lo mismo que "(llueve y hace sol) o (llueve y hace frío)".
   - $A∨(B∧C)$ es lo mismo que $(A∨B)∧(A∨C)$. (No lo usaremos en este ejercicio, pero es bueno saberlo).

5. **Tautología**: $A∨¬A$ es siempre cierto ($⊤$). Ejemplo: "Llueve o no llueve" es siempre cierto.

6. **Contradicción**: $A∧¬A$ es siempre no cierto ($⊥$). Ejemplo: "Llueve y no llueve" nunca es cierto.

7. **Simplificación**:
   - $A∨⊤$ es $⊤$. Ejemplo: "Llueve o siempre es cierto" es siempre cierto.
   - $A∧⊤$ es $A$. Ejemplo: "Llueve y siempre es cierto" es lo mismo que "llueve".
   - $A∨⊥$ es $A$. Ejemplo: "Llueve o nunca es cierto" es lo mismo que "llueve".
   - $A∧⊥$ es $⊥$. Ejemplo: "Llueve y nunca es cierto" nunca es cierto.

8. **Asociativa**: $(A∨B)∨C$ es lo mismo que $A∨(B∨C)$. Ejemplo: "(Llueve o hace sol) o hace frío" es lo mismo que "llueve o (hace sol o hace frío)".

**Qué hacer**: Escribe estas leyes en un papel para tenerlas a la mano mientras simplificas las expresiones.

## Paso a paso para resolver el ejercicio

### Paso 1: Identificar las dos partes de la equivalencia

La expresión es:

$$(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(R→P) ≡ ¬P$$

- **Lado izquierdo**: $(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(R→P)$
- **Lado derecho**: $¬P$

Queremos simplificar el lado izquierdo usando las leyes de la lógica para ver si se convierte en $¬P$. Si lo hace, las dos partes son equivalentes. Si no, no lo son.

**Ejemplo cotidiano**: Piensa que $P$ es "hoy llueve", $Q$ es "hace sol", y $R$ es "salgo a correr". El lado izquierdo es como decir: "(No llueve y hace sol) o (no llueve y no es cierto que hace sol y salgo a correr) o (si salgo a correr, entonces llueve)". El lado derecho es simplemente "no llueve". Queremos ver si estas dos afirmaciones siempre son lo mismo.

**Qué hacer**: Escribe las dos partes de la equivalencia y decide cuál simplificar (normalmente el lado más complicado, que aquí es el izquierdo).

### Paso 2: Simplificar el lado izquierdo (o el más complicado)

Vamos a simplificar el lado izquierdo paso a paso:

$$(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(R→P)$$

#### Paso 2.1: Reescribir $R→P$

Usamos la definición de implicación: $A→B$ es lo mismo que $¬A∨B$. Aquí, $A$ es $R$ y $B$ es $P$:

$$R→P \text{ se convierte en } ¬R∨P$$

Sustituimos en la expresión:

$$(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(¬R∨P)$$

**Ejemplo cotidiano**: Esto es como decir: "(No llueve y hace sol) o (no llueve y no es cierto que hace sol y salgo a correr) o (no salgo a correr o llueve)".

**Qué hacer**: Siempre que veas una implicación ($→$), reescríbela como $¬A∨B$.

#### Paso 2.2: Simplificar $¬(Q∧R)$

Miremos la parte $¬(Q∧R)$. Usamos la Ley de De Morgan:

$$¬(Q∧R) \text{ se convierte en } ¬Q∨¬R$$

Sustituimos:

$$(¬P∧Q)∨[¬P∧(¬Q∨¬R)]∨(¬R∨P)$$

**Ejemplo cotidiano**: Esto es como decir: "(No llueve y hace sol) o (no llueve y (no hace sol o no salgo a correr)) o (no salgo a correr o llueve)".

**Qué hacer**: Usa la Ley de De Morgan para manejar negaciones con "y" o "o".

#### Paso 2.3: Distribuir $¬P∧(¬Q∨¬R)$

Miremos $¬P∧(¬Q∨¬R)$. Usamos la propiedad distributiva de $∧$ sobre $∨$:

$$A∧(B∨C) \text{ es lo mismo que } (A∧B)∨(A∧C)$$

Aquí, $A$ es $¬P$, $B$ es $¬Q$, y $C$ es $¬R$:

$$¬P∧(¬Q∨¬R) \text{ se convierte en } (¬P∧¬Q)∨(¬P∧¬R)$$

Sustituimos:

$$(¬P∧Q)∨[(¬P∧¬Q)∨(¬P∧¬R)]∨(¬R∨P)$$

**Ejemplo cotidiano**: Esto es como decir: "(No llueve y hace sol) o [(no llueve y no hace sol) o (no llueve y no salgo a correr)] o (no salgo a correr o llueve)".

**Qué hacer**: Usa la propiedad distributiva para separar términos y hacerlos más fáciles de manejar.

#### Paso 2.4: Agrupar términos con $∨$

La expresión ahora es una serie de disyunciones (uniones con $∨$). Usamos la propiedad asociativa de $∨$, que dice que $(A∨B)∨C$ es lo mismo que $A∨(B∨C)$, para quitar los corchetes:

$$(¬P∧Q)∨(¬P∧¬Q)∨(¬P∧¬R)∨(¬R∨P)$$

**Ejemplo cotidiano**: Esto es como decir: "(No llueve y hace sol) o (no llueve y no hace sol) o (no llueve y no salgo a correr) o (no salgo a correr o llueve)".

**Qué hacer**: Si tienes muchos $∨$, usa la propiedad asociativa para tratarlos como una lista larga.

#### Paso 2.5: Factorizar los términos con $¬P$

Observa que los primeros tres términos tienen $¬P$ en común:

$$(¬P∧Q)∨(¬P∧¬Q)∨(¬P∧¬R)$$

Usamos la propiedad distributiva de $∧$ sobre $∨$ en sentido inverso:

$$(A∧B)∨(A∧C)∨(A∧D) \text{ es lo mismo que } A∧(B∨C∨D)$$

Aquí, $A$ es $¬P$, $B$ es $Q$, $C$ es $¬Q$, y $D$ es $¬R$:

$$(¬P∧Q)∨(¬P∧¬Q)∨(¬P∧¬R) \text{ se convierte en } ¬P∧(Q∨¬Q∨¬R)$$

**Ejemplo cotidiano**: Esto es como decir: "No llueve y (hace sol o no hace sol o no salgo a correr)".

**Qué hacer**: Si ves varios términos con una parte en común, factorízala usando la distributiva.

#### Paso 2.6: Simplificar $Q∨¬Q∨¬R$

Miremos $Q∨¬Q∨¬R$:

- $Q∨¬Q$ es una tautología (siempre es cierto, porque siempre una de las dos es cierta). En lógica, esto se escribe como $⊤$.
- Entonces: $Q∨¬Q∨¬R$ se convierte en $⊤∨¬R$
- Y $⊤∨¬R$ es siempre cierto (porque $⊤$ ya es cierto). Esto es una simplificación: $⊤∨¬R$ es $⊤$

Sustituimos:

$$¬P∧(Q∨¬Q∨¬R) \text{ se convierte en } ¬P∧⊤$$

**Ejemplo cotidiano**: "Hace sol o no hace sol o no salgo a correr" es como decir "siempre es cierto o no salgo a correr", que siempre es cierto.

**Qué hacer**: Busca tautologías ($A∨¬A$) y usa la simplificación para reducir la expresión.

#### Paso 2.7: Simplificar $¬P∧⊤$

Usamos la simplificación:

$$A∧⊤ \text{ es lo mismo que } A$$

Entonces:

$$¬P∧⊤ \text{ se convierte en } ¬P$$

Nuestra expresión ahora es:

$$¬P∨(¬R∨P)$$

**Ejemplo cotidiano**: Esto es como decir: "No llueve o (no salgo a correr o llueve)".

**Qué hacer**: Usa las reglas de simplificación para eliminar términos como $⊤$ o $⊥$.

#### Paso 2.8: Simplificar $¬P∨(¬R∨P)$

Reorganicemos usando la propiedad asociativa de $∨$:

$$¬P∨(¬R∨P) \text{ se convierte en } (¬P∨P)∨¬R$$

- $¬P∨P$ es una tautología (siempre es cierto). Esto es $⊤$.
- Entonces: $(¬P∨P)∨¬R$ se convierte en $⊤∨¬R$
- Y usamos la simplificación: $⊤∨¬R$ es $⊤$

**Ejemplo cotidiano**: "No llueve o llueve o no salgo a correr" es como decir "siempre es cierto o no salgo a correr", que siempre es cierto.

**Qué hacer**: Busca más tautologías y simplifica la expresión.

### Paso 3: Comparar los dos lados

El lado izquierdo se simplificó a:

$$⊤ \text{ (siempre cierto)}$$

El lado derecho es:

$$¬P$$

Ahora comparamos:

- $⊤$ es siempre cierto (siempre es 1).
- $¬P$ no es siempre cierto. Por ejemplo:
  - Si $P$ es cierto (llueve), $¬P$ es no cierto (no llueve).
  - Si $P$ no es cierto (no llueve), $¬P$ es cierto (no llueve).

Esto significa que $⊤$ y $¬P$ no son equivalentes, porque $⊤$ siempre es 1, pero $¬P$ puede ser 0 o 1 dependiendo de $P$.

**Ejemplo cotidiano**: El lado izquierdo es como decir "siempre es cierto", pero el lado derecho es "no llueve". Si llueve, el lado derecho es no cierto, pero el lado izquierdo sigue siendo cierto, así que no son lo mismo.

**Qué hacer**: Compara las dos expresiones simplificadas. Si son iguales, son equivalentes. Si no, no lo son.

### Paso 4: Verificar con un contraejemplo (opcional)

Para confirmar que no son equivalentes, probemos con un valor específico. Supongamos $P$ es cierto (llueve):

- Lado izquierdo: $⊤$ (siempre cierto, 1).
- Lado derecho: $¬P$, que es no cierto (porque $P$ es cierto, así que $¬P$ es 0).

Los valores son diferentes (1 vs. 0), lo que confirma que no son equivalentes.

**Qué hacer**: Si las expresiones no parecen iguales, prueba con un valor específico para confirmar.

### Paso 5: Concluir

La expresión:

$$(¬P∧Q)∨[¬P∧¬(Q∧R)]∨(R→P) ≡ ¬P$$

no es una equivalencia lógica, porque el lado izquierdo se simplifica a $⊤$ (siempre cierto), pero el lado derecho ($¬P$) no es siempre cierto.

**Qué hacer**: Escribe tu conclusión: si las expresiones son iguales, son equivalentes; si no, no lo son.

### Paso 6: Justificar cada paso

Escribe los pasos con las leyes que usaste:

1. Reescribimos $R→P$:
   $$R→P \text{ se convierte en } ¬R∨P \text{ (definición de implicación)}$$

2. Simplificamos $¬(Q∧R)$:
   $$¬(Q∧R) \text{ se convierte en } ¬Q∨¬R \text{ (Ley de De Morgan)}$$

3. Distribuimos $¬P∧(¬Q∨¬R)$:
   $$¬P∧(¬Q∨¬R) \text{ se convierte en } (¬P∧¬Q)∨(¬P∧¬R) \text{ (distributiva de ∧ sobre ∨)}$$

4. Factorizamos los términos con $¬P$:
   $$(¬P∧Q)∨(¬P∧¬Q)∨(¬P∧¬R) \text{ se convierte en } ¬P∧(Q∨¬Q∨¬R) \text{ (distributiva de ∧ sobre ∨)}$$

5. Simplificamos $Q∨¬Q∨¬R$:
   - $Q∨¬Q$ es $⊤$ (tautología)
   - $⊤∨¬R$ es $⊤$ (simplificación)

6. Simplificamos $¬P∧⊤$:
   $$¬P∧⊤ \text{ es } ¬P \text{ (simplificación)}$$

7. Simplificamos $¬P∨(¬R∨P)$:
   - $¬P∨(¬R∨P)$ es $(¬P∨P)∨¬R$ (asociativa de ∨)
   - $¬P∨P$ es $⊤$ (tautología)
   - $⊤∨¬R$ es $⊤$ (simplificación)

8. Comparamos:
   - Lado izquierdo: $⊤$, lado derecho: $¬P$ (no son equivalentes)

**Qué hacer**: Justifica cada paso diciendo qué ley usaste (como Ley de De Morgan, distributiva, etc.).

## Herramientas aplicadas en cada paso

- **Paso 1 (Identificar las partes)**: Herramienta: Conocer los símbolos y dividir la expresión en lados izquierdo y derecho. No necesitas leyes aquí.
- **Paso 2 (Simplificar el lado izquierdo)**:
  - Usa la definición de implicación ($A→B$ es $¬A∨B$).
  - Usa la Ley de De Morgan para manejar negaciones.
  - Usa la distributiva para factorizar o distribuir términos.
  - Usa tautologías ($A∨¬A$) y simplificaciones ($A∧⊤$ es $A$).
  - Usa la asociativa para reorganizar términos.
- **Paso 3 (Comparar)**: Herramienta: Compara las expresiones simplificadas para ver si son iguales.
- **Paso 4 (Verificar con un contraejemplo)**: Herramienta: Prueba con un valor específico si las expresiones no parecen iguales.
- **Paso 5 (Concluir)**: Herramienta: Decide si son equivalentes basándote en la simplificación.
- **Paso 6 (Justificar)**: Herramienta: Escribe las leyes que usaste en cada paso.

## Consejos
- **Ve despacio**: Simplifica un paso a la vez y revisa que cada transformación sea correcta.
- **Usa ejemplos cotidianos**: Piensa en las letras como cosas simples (como "llueve", "hace sol") para entender mejor lo que estás simplificando.
- **Escribe todo**: Anota cada paso en un papel para no perderte.
- **Busca patrones**: Si ves cosas como $A∨¬A$, sabes que es una tautología y puedes simplificar.
- **Practica las leyes**: Las leyes de De Morgan, la distributiva y la definición de implicación son muy comunes. Practica con ejemplos pequeños.
