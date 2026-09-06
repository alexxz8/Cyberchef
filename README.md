````markdown
# CyberChef

Guía práctica para aprender a utilizar **CyberChef** para analizar, decodificar y desofuscar cadenas y comandos.

## 📖 Sobre esta guía

Esta guía está enfocada principalmente a personas que están empezando a utilizar CyberChef en tareas de **ciberseguridad, análisis de comandos y malware**.

El objetivo no es únicamente aprender qué operaciones existen, sino aprender a **razonar qué operación utilizar en cada momento**, identificando patrones, indicadores y pistas presentes en los datos.

La idea principal es:

> **Observa → formula una hipótesis → prueba una operación → analiza el resultado → confirma o descarta la hipótesis → repite.**

## 🧠 Contenido

La guía cubre, entre otros, los siguientes conceptos:

- Introducción a CyberChef
- Interfaz y funcionamiento básico
- Operations, Recipe, Input y Output
- Uso de recetas paso a paso
- Base64
- Hexadecimal
- Binario
- Base32 y Base58
- ROT13 y otras sustituciones
- URL Encoding
- Compresión y descompresión
- File signatures / Magic Bytes
- Reverse
- XOR
- Identificación de patrones
- Indicadores para elegir una operación
- Cómo interpretar los resultados de cada operación
- Cómo detectar cuándo una operación no es correcta
- Uso de **Magic** como herramienta de apoyo
- Construcción iterativa de una receta de CyberChef
- Análisis de comandos ofuscados
- Identificación de comandos y comportamientos sospechosos

## 🔎 Enfoque

Una cadena ofuscada no siempre indica directamente qué método se ha utilizado.

Por ejemplo, una cadena formada únicamente por:

```text
48656C6C6F
````

puede hacer sospechar que se trata de hexadecimal.

Mientras que una cadena como:

```text
SGVsbG8gV29ybGQ=
```

presenta características compatibles con Base64.

La guía explica **qué indicadores permiten formular estas hipótesis** y cómo comprobarlas mediante CyberChef.

## 🧪 Ejemplos prácticos

Se incluyen ejemplos de cadenas con varias capas de ofuscación o codificación.

Un proceso puede requerir varias operaciones consecutivas, por ejemplo:

```text
ROT13
   ↓
From Base64
   ↓
Gunzip
   ↓
From Binary
   ↓
From Base64
   ↓
From Hex
   ↓
Comando
```

La receta no se conoce necesariamente desde el principio. Se construye **iterativamente**, utilizando el resultado de cada operación como una nueva pista.

## ⚠️ Análisis de comandos

Algunos ejemplos de la guía contienen comandos potencialmente maliciosos utilizados para explicar técnicas habituales de **post-explotación, ejecución de código y extracción de credenciales**.

Estos ejemplos tienen únicamente una finalidad educativa y de análisis.

No se recomienda ejecutar comandos desconocidos fuera de un entorno controlado.

## 🛠️ Herramienta

La guía utiliza:

* [CyberChef](https://gchq.github.io/CyberChef/)

CyberChef es una herramienta web desarrollada por **GCHQ** que permite realizar diferentes operaciones sobre datos mediante la creación de recetas.

## 🎯 Objetivo

El objetivo final es pasar de:

> **"¿Qué operación tengo que probar?"**

a:

> **"Veo estos indicadores, por lo que sospecho que esta transformación puede ser X. La pruebo y utilizo el resultado para determinar el siguiente paso."**

Es decir, aprender a **pensar durante el proceso de análisis**, no simplemente a seguir una receta.

## 📚 Estructura

```text
Cyberchef/
│
├── README.md
└── Guia/
    └── CyberChef.pdf / CyberChef.md
```

> La estructura puede variar dependiendo del formato utilizado para publicar la guía.

---

### 📌 Nota

Esta guía está orientada al aprendizaje y al análisis defensivo dentro del ámbito de la ciberseguridad.

```
```
