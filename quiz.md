# QUIZ FINAL – Redes de Inferencia con AND / OR

**Nombre completo:** Felipe Corredor Silva

**ID completo:** 0045168694

------

## Instrucciones

1. Utilice únicamente el **último dígito de su ID** para personalizar el quiz.
2. Según ese último dígito, defina:

### Compuerta principal (AND / OR)

- Si el último dígito es **par**, use **AND**.
- Si es **impar**, use **OR**.

### Conjunto de hechos asignados

- Dígito **0–3** → hechos: **(a, b, c)**
- Dígito **4–6** → hechos: **(d, e, f)**
- Dígito **7–9** → hechos: **(g, h, i)**

### Meta final (salida del ejercicio)

- Dígito 0 → Z
- Dígito 1 → Q
- Dígito 2 → W
- Dígito 3 → R
- Dígito 4 → K
- Dígito 5 → P
- Dígito 6 → M
- Dígito 7 → T
- Dígito 8 → FINAL
- Dígito 9 → S

1. Reemplace los hechos (X1, X2, etc.) y compuertas (COMP) según su ID.
2. Responda en los espacios indicados.

------

# PREGUNTA 1 – Activación básica

```
X1 ----\
         COMP(1) ---- P ----> META
X2 ----/
```

1.1 ¿Qué compuerta corresponde a COMP(1)?

 corresponde a aun AND 

 ------

1.2 ¿Qué hechos corresponden a X1 y X2 según su ID?

(d,e,f) por que mi ultimo digito es 4

**X1** = d
**X2** = e

----

1.3 ¿En qué condición se activa META?

META se activa cuando d y e son verdaderos al mismo tiempo y nos da k

----

# PREGUNTA 2 – Ruta doble hacia la meta

```
X1 ----\
         COMP(1) ---- R ----\
X2 ----/                     \
                               OR(3) ----> META
X3 ---------------------------/
```

2.1 Red personal con los hechos asignados:
X1 = d
X2 = e
X3 = f
COMP = AND
OR = OR
META = K

```
d ----\
         AND ---- R ----\
e ----/                     \
                               OR ----> k
f ---------------------------/
```

----

2.2 ¿Qué rutas activan META?

hay dos rutas para poder activar META

Ruta 1:
d ∧ e -> R -> OR -> K

Ruta 2:
f -> OR -> K

----

2.3 ¿Existe conflicto entre caminos? Explique:

no existe conflictos entre caminos por que la compuerta OR acepta cualquier camino valido , el camino superior (d ∧ e -> R) y el camino inferior (f) no se bloquean ni se contradiicen entre si y ambos caminos pueden activar independientemente, y si llegan a tiempo R simplemente recibe dos señales validas, pero no causa conflicto

----

# PREGUNTA 3 – Encuentro de caminos

```
X1 ----\
         COMP(1) ---- P ----\
X2 ----/                    \
                              COMP(3) ---> META
X3 ----\                    /
         COMP(2) ---- Q ---/
X4 ----/
```

3.1 Dibuje su red personalizada:

X1 = d
X2 = e
X3 = f
X4 = d
COMP(1) = AND
COMP(2) = AND
COMP(3) = AND 
META = k

```
d ----\
         AND ---- P ----\
e ----/                    \
                              AND ---> K
f ----\                    /
         AND ---- Q ---/
d ----/
```

------

3.2 ¿Cuál camino es más corto hacia META?

existen dos caminos hacia la meta el superior y el inferior pero los dos tienen la misma longitud por lo cual no existe camino mas corto si no que son iguales 

------

3.3 ¿Pueden activarse ambos caminos? Justifique.

Sí, ambos caminos pueden activarse al mismo tiempo porque requieren conjuntos de hechos compatibles (d, e, f). Si P y Q se activan juntos, la compuerta AND final activa META


------


# PREGUNTA 4 – Camino alterno profundo

```
X1 ---- COMP(1) ---- A ----\
                            OR(4) ----> META
X2 ---- COMP(2) ---- B ----/
X3 ------------------------/
```

4.1 Describa las tres rutas posibles hacia META:

Ruta 1: A -> OR -> K

Para activar A:

d ->

AND ->

A -> OR -> K

Condición:
d verdadero


Ruta 2: B -> OR -> K

Para activar B:

e ->

AND ->

B -> OR -> K

Condición:
e verdadero

Ruta 3: f -> OR -> K

Ruta directa:

f -> OR -> K

Esta ruta no depende de A ni B.

------

4.2 ¿Cuál ruta requiere menos hechos?

 La ruta que requiere menos hechos es: Ruta 3: f -> OR -> K

------

# PREGUNTA 5 – Compuerta final condicionada

```
   X1 ----\
            COMP(1) ---- P ----\
   X2 ----/                     \
                                   COMP(4) -----> META
   X3 ------ COMP(2) ---- Q -----/
```

5.1 ¿Qué compuerta corresponde a COMP(4)?

COMP(4) esa compuerta coresponde a un AND 

------

5.2 Indique el conjunto mínimo de hechos para activar META:

El conjunto mínimo de hechos para poder activar META es: d, e y f.

------

# PREGUNTA 6 – Activación encadenada

```
X1 ----\
         COMP(1) ---- A ----\
X2 ----/                     \
                               COMP(3) ----> META
X3 ----\                     /
         COMP(2) ---- B ----/
X4 ----/
```

6.1 ¿Qué se activa primero, A o B?

no existe un orden, A o B se activan segun el par de hechos que activan primero segun el par de hechos este completo antes 


------

6.2 ¿Cómo influye COMP(3) en la decisión final?

COMP(3) exige que tanto A como B estén activos al mismo tiempo.

------

# PREGUNTA 7 – Hecho obligatorio

```
           X1 ---- COMP(1) ---- P ----\
                                        COMP(3) ---> META
X_OBLIG ------------------------------/
```

El hecho obligatorio **X_OBLIG** es el segundo hecho del conjunto asignado:
 (a,b,c → b) (d,e,f → e) (g,h,i → h)

7.1 ¿META puede activarse sin X_OBLIG?

No, META NO puede activarse sin X_OBLIG (e).

------

7.2 ¿Qué camino opcional complementa la activación?

El camino opcional que complementa la activación es el que activa P:

d -> P -> K.

------

# PREGUNTA 8 – Camino alterno opcional

```
X1 ---- COMP(1) ---- R ----\
                             OR(4) ----> META
X2 -------------------------/
X3 ---- COMP(2) ---- S ----/
```

8.1 ¿Cuáles rutas permiten activar META?

Las rutas que activan META (K) son:

d ∧ e -> R -> K

e -> K

d ∧ f -> S -> K

------

8.2 ¿Cuál ruta es más robusta?

La ruta más robusta es la que activa R: d ∧ e -> R -> K.

------


# PREGUNTA 9 – Triple combinación

```
X1 -----\
          COMP(1) ---- A ----\
X2 -----/                     \
                                OR(5) ----> META
X3 -----\                     /
          COMP(2) ---- B ----/
X4 -----/
```

9.1 ¿Qué camino tiene prioridad lógica?

------

9.2 ¿Qué ocurre si COMP(1) es OR y COMP(2) es AND?

------

------

# PREGUNTA 10 – Red final con múltiples caminos

```
X1 ---- COMP(1) ---- P ----\
                             OR(6) ----> META
X2 ---- COMP(2) ---- Q ----/
X3 ------------------------/
```

10.1 Construya su red final personalizada:

------

10.2 Explique el papel de la compuerta OR(6):

------

10.3 Conjunto mínimo de hechos que activa META:

------

------

Si
