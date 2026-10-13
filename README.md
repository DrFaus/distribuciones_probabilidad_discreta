# Práctica interactiva de distribuciones discretas

Aplicación web educativa para practicar el reconocimiento, cálculo e interpretación de probabilidades mediante las distribuciones **binomial, hipergeométrica y de Poisson**.

La herramienta fue desarrollada como material de apoyo para estudiantes de **Gestión Empresarial** dentro de un curso introductorio de Probabilidad y Estadística.

El objetivo principal no es únicamente sustituir valores en una fórmula, sino que el estudiante aprenda a **identificar qué distribución corresponde a una situación real**, interprete correctamente expresiones como *exactamente*, *a lo sumo* y *al menos*, y obtenga la probabilidad solicitada.

## Características principales

- Banco de **180 problemas**.
- **60 problemas binomiales**.
- **60 problemas hipergeométricos**.
- **60 problemas de Poisson**.
- **5 problemas aleatorios por intento**.
- Cada intento incluye siempre las tres distribuciones.
- Distribución balanceada mediante esquemas **2–2–1**.
- Los problemas **no indican explícitamente qué distribución utilizar**.
- Respuestas numéricas directas.
- Sin preguntas de opción múltiple.
- **Modo estudio** con retroalimentación inmediata.
- Generación aleatoria de nuevos intentos.
- Opción para repasar únicamente los errores.
- Calificación general y desempeño por distribución.
- Generación de reporte imprimible y exportable como PDF.
- Funciona completamente **offline**.
- Todo el proyecto está contenido en **un único archivo HTML**.
- No utiliza librerías externas.

---

## Distribuciones incluidas

La práctica trabaja con tres distribuciones discretas:

1. Binomial.
2. Hipergeométrica.
3. Poisson.

Una parte importante de la actividad consiste en que el estudiante determine cuál de ellas corresponde a cada situación.

---

# 1. Distribución binomial

La distribución binomial se utiliza cuando se realizan $n$ ensayos y, bajo el modelo estudiado:

- cada ensayo tiene dos resultados de interés;
- la probabilidad de éxito $p$ permanece constante;
- los ensayos pueden considerarse independientes;
- se cuenta el número de éxitos obtenidos.

Si:

$$
X\sim Bin(n,p)
$$

entonces:

$$
P(X=k)=
\binom{n}{k}
p^k(1-p)^{n-k}
$$

donde:

- $n$ = número de ensayos;
- $k$ = número de éxitos de interés;
- $p$ = probabilidad de éxito;
- $1-p$ = probabilidad de no éxito.

## Ejemplo

Una campaña de correo electrónico se envía a 12 clientes. Históricamente, cada cliente tiene una probabilidad de $0.20$ de realizar una compra.

La probabilidad de que exactamente 3 clientes realicen una compra se modela mediante:

$$
X\sim Bin(12,0.20)
$$

y se calcula:

$$
P(X=3)
=
\binom{12}{3}
(0.20)^3(0.80)^9
$$

---

# 2. Distribución hipergeométrica

La distribución hipergeométrica se utiliza cuando se selecciona una muestra **sin reemplazo** de una población finita.

Si la población contiene:

- $N$ elementos en total;
- $K$ elementos con la característica de interés;
- se seleccionan $n$ elementos;
- se desea obtener exactamente $k$ elementos con dicha característica;

entonces:

$$
X\sim H(N,K,n)
$$

y:

$$
P(X=k)=
\frac{
\binom{K}{k}
\binom{N-K}{n-k}
}{
\binom{N}{n}
}
$$

## Ejemplo

Una empresa tiene 20 proveedores registrados, de los cuales 6 presentan antecedentes de retrasos.

Se seleccionan 5 proveedores **sin reemplazo** para una auditoría.

La probabilidad de que exactamente 2 de los seleccionados tengan antecedentes de retrasos es:

$$
P(X=2)=
\frac{
\binom{6}{2}
\binom{14}{3}
}{
\binom{20}{5}
}
$$

La expresión **sin reemplazo** es una señal especialmente importante para distinguir este modelo del binomial.

---

# 3. Distribución de Poisson

La distribución de Poisson se utiliza para modelar el número de veces que ocurre un evento dentro de un intervalo cuando se conoce una tasa promedio de ocurrencia.

Si:

$$
X\sim Pois(\lambda)
$$

entonces:

$$
P(X=k)=
\frac{e^{-\lambda}\lambda^k}{k!}
$$

donde:

- $\lambda$ = número promedio de eventos esperado en el intervalo;
- $k$ = número de eventos que se desea observar.

## Ejemplo

Un centro de atención recibe en promedio 4 reclamaciones por hora.

La probabilidad de recibir exactamente 2 reclamaciones durante una hora se obtiene con:

$$
X\sim Pois(4)
$$

y:

$$
P(X=2)=
\frac{e^{-4}4^2}{2!}
$$

---

# Reconocimiento de la distribución

La práctica busca reforzar especialmente la identificación del modelo apropiado.

Una guía rápida es:

| Situación | Distribución |
|---|---|
| Número fijo de ensayos, probabilidad constante e independencia | Binomial |
| Población finita y selección sin reemplazo | Hipergeométrica |
| Número de eventos en un intervalo con una tasa promedio | Poisson |

No obstante, los reactivos del banco **no indican directamente qué distribución debe utilizarse**. El estudiante debe reconocerla a partir del contexto.

---

# Tipos de probabilidades

Los problemas incluyen diferentes expresiones probabilísticas.

## Exactamente

Si se solicita:

> exactamente 3

se calcula:

$$
P(X=3)
$$

---

## A lo sumo

Si se solicita:

> a lo sumo 3

significa:

$$
P(X\leq 3)
$$

por lo que:

$$
P(X\leq3)=
P(X=0)+P(X=1)+P(X=2)+P(X=3)
$$

---

## Al menos

Si se solicita:

> al menos 3

significa:

$$
P(X\geq3)
$$

En muchos casos resulta conveniente utilizar el complemento:

$$
P(X\geq3)=
1-P(X\leq2)
$$

---

## Entre dos cantidades

Si se solicita:

> entre 2 y 5, inclusive

se interpreta como:

$$
P(2\leq X\leq5)
$$

y se calcula:

$$
P(X=2)+P(X=3)+P(X=4)+P(X=5)
$$

---

# Respuestas

Los reactivos no utilizan opción múltiple.

El estudiante debe escribir directamente el valor de la probabilidad obtenida.

Dependiendo del problema, pueden aceptarse distintas representaciones numéricas equivalentes, por ejemplo:

- `0.25`
- `0,25`
- `.25`
- `25%`
- `1/4`

cuando sean equivalentes y el tipo de problema lo permita.

En los problemas que lo requieran se solicita expresar la respuesta con **cuatro decimales**.

---

# Estructura de cada intento

Cada intento contiene **5 problemas** seleccionados aleatoriamente.

Siempre se incluyen problemas de:

- distribución binomial;
- distribución hipergeométrica;
- distribución de Poisson.

Para mantener el equilibrio, la composición utiliza esquemas como:

- 2 binomiales, 2 hipergeométricos y 1 Poisson;
- 2 binomiales, 1 hipergeométrico y 2 Poisson;
- 1 binomial, 2 hipergeométricos y 2 Poisson.

La distribución que aparece una sola vez cambia entre intentos.

De esta manera, al realizar varios intentos, las tres distribuciones reciben una presencia semejante.

---

# Banco de problemas

El banco está compuesto por:

| Distribución | Problemas |
|---|---:|
| Binomial | 60 |
| Hipergeométrica | 60 |
| Poisson | 60 |
| **Total** | **180** |

El tamaño del banco permite generar una gran variedad de intentos sin que los estudiantes reciban continuamente los mismos problemas.

---

# Contextos utilizados

Los problemas están orientados principalmente a situaciones relacionadas con **Gestión Empresarial**.

Entre los contextos utilizados se encuentran:

- campañas de marketing;
- conversiones de ventas;
- renovación de contratos;
- clientes;
- pedidos;
- entregas;
- devoluciones;
- quejas;
- llamadas de atención al cliente;
- proveedores;
- auditorías;
- selección de muestras;
- empleados;
- inventarios;
- productos defectuosos;
- clientes premium;
- incidencias administrativas;
- comportamiento de servicios.

El propósito es que el estudiante identifique la estructura probabilística dentro de situaciones que podrían encontrarse en un entorno empresarial.

---

# Modo estudio

La aplicación incluye un **Modo estudio**.

Cuando se encuentra activado, después de responder un problema se proporciona retroalimentación que explica:

- qué distribución corresponde;
- por qué corresponde esa distribución;
- qué representan sus parámetros;
- qué expresión probabilística debe calcularse;
- el procedimiento;
- el resultado correcto.

Esto permite utilizar el banco no solamente como evaluación, sino también como herramienta de práctica.

---

# Modo de evaluación

Con el modo estudio desactivado, las respuestas no se califican inmediatamente.

El estudiante debe resolver los 5 problemas y posteriormente seleccionar:

**Calificar intento**

La aplicación muestra:

- número de respuestas correctas;
- porcentaje obtenido;
- desempeño por distribución;
- respuesta proporcionada;
- respuesta correcta;
- explicación correspondiente.

---

# Repaso de errores

Después de calificar un intento puede utilizarse la opción:

**Repasar sólo errores**

Esta función oculta temporalmente los problemas contestados correctamente y permite concentrarse en aquellos donde se presentó alguna dificultad.

---

# Reporte

Después de calificar un intento puede generarse un reporte que incluye:

- nombre del estudiante;
- fecha;
- número de intento;
- calificación obtenida;
- problemas presentados;
- respuesta del estudiante;
- respuesta correcta;
- distribución utilizada;
- explicación del procedimiento.

El reporte puede guardarse como PDF mediante la función de impresión del navegador.

---

# Tecnologías utilizadas

El proyecto está desarrollado únicamente con:

- HTML5;
- CSS;
- JavaScript.

No requiere:

- instalación;
- conexión a Internet;
- frameworks;
- bibliotecas externas.

Todo el proyecto se encuentra contenido en **un único archivo HTML**.

---

# Ejecución

No requiere instalación.

1. Descargar el archivo HTML.
2. Abrirlo con un navegador moderno.
3. Escribir el nombre del estudiante.
4. Resolver los 5 problemas.
5. Seleccionar **Calificar intento**.
6. Revisar la retroalimentación.
7. Opcionalmente generar el reporte en PDF.
8. Generar un nuevo intento para continuar practicando.

---

# Uso educativo

Esta herramienta está diseñada como apoyo para cursos introductorios de **Probabilidad y Estadística** en Gestión Empresarial.

Busca reforzar principalmente tres habilidades:

1. **Reconocer la distribución adecuada a partir del contexto.**
2. **Traducir correctamente expresiones como exactamente, a lo sumo y al menos a notación probabilística.**
3. **Calcular e interpretar la probabilidad obtenida.**

La intención es que el estudiante no dependa únicamente de identificar una fórmula por palabras clave, sino que comprenda las características del fenómeno aleatorio que está modelando.

---

# Autor

Material educativo desarrollado para la enseñanza de Probabilidad y Estadística.
