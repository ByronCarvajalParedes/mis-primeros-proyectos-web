# Transcripción de la Conversación: Introducción al Desarrollo Web ("Introduction to Web ID")

Esta conversación tuvo lugar el 24 de junio de 2026 entre **Byron** y **Antigravity** (asistente de IA). En ella se exploraron las bases del desarrollo web, se crearon cuatro proyectos prácticos y se explicaron conceptos clave de programación e infraestructura.

---

## Índice
1. [Sesión 1: Conceptos Básicos y Tu Primera Web](#sesion-1-conceptos-basicos-y-tu-primera-web)
2. [Sesión 2: Servidores, Dominios y Despliegue en Netlify](#sesion-2-servidores-dominios-y-despliegue-en-netlify)
3. [Sesión 3: Estructura del Desarrollo Web (La Metáfora del Restaurante)](#sesion-3-estructura-del-desarrollo-web-la-metafora-del-restaurante)
4. [Sesión 4: Persistencia y Servidores Locales (Lista de Tareas)](#sesion-4-persistencia-y-servidores-locales-lista-de-tareas)
5. [Sesión 5: Conexión con el Mundo Real (APIs y Perritos)](#sesion-5-conexion-con-el-mundo-real-apis-y-perritos)
6. [Sesión 6: CSS Avanzado y Modo Claro/Oscuro (Tarjeta de Presentación)](#sesion-6-css-avanzado-y-modo-clarooscuro-tarjeta-de-presentacion)
7. [Resumen Técnico de Conceptos](#resumen-tecnico-de-conceptos)

---

## Sesión 1: Conceptos Básicos y Tu Primera Web

**Byron:**
> ¡Hola! Es la primera vez que utilizo un IDE. No sé qué es, pero me han dicho que es el lugar para crear todos los productos web. ¿Es así?

**Antigravity:**
Un **IDE** (*Entorno de Desarrollo Integrado*) es como un "taller digital" para programar. Agrupa en un solo lugar:
1. **Un editor de texto avanzado** que resalta el código con colores.
2. **Un explorador de archivos** para organizar carpetas e imágenes.
3. **Herramientas de ejecución y depuración** para probar y corregir errores.

**Byron:**
> ¡Sí! Me gustaría crear algo y entender qué se necesita para hacerlo posible. ¿Se podría incluso hacer accesible por Chrome? Me haría ilusión.

### Proyecto 1: Mi Primera Web
Creamos una carpeta llamada `mi-primera-web` con un archivo `index.html`. Tiene un diseño moderno (*Glassmorphism*), un fondo degradado animado y un botón que usa **JavaScript** para generar citas inspiradoras de programación de manera interactiva.

* Código disponible en: [mi-primera-web/index.html](file:///C:/Users/I758077/.gemini/antigravity/scratch/mi-primera-web/index.html)

**Byron:**
> ¡Vale! En este documento llamado `index` has escrito todo lo que has dicho: HTML, CSS y Java, ¿cierto?

**Antigravity:**
¡Casi! Usamos HTML, CSS y **JavaScript**.
> [!IMPORTANT]
> **Java** y **JavaScript** son dos lenguajes completamente distintos.
> * **JavaScript:** Es el lenguaje nativo de las páginas web que se ejecuta en tu navegador (Chrome) para dar interactividad.
> * **Java:** Se usa para aplicaciones de servidor, Android y sistemas de escritorio.
> * *El chiste clásico:* "Java es a JavaScript lo que el jamón es al jabón."

---

## Sesión 2: Servidores, Dominios y Despliegue en Netlify

**Byron:**
> He visto que lo que hemos hecho es tener un documento que Google Chrome es capaz de interpretar y abrir. Pero, ¿cómo haríamos para que más gente pueda acceder?

**Antigravity:**
Para que cualquiera acceda desde internet, necesitamos dos cosas:
1. **Alojar el archivo en un Servidor (Hosting):** Un ordenador encendido las 24 horas conectado a internet.
2. **Una dirección web (Dominio o URL):** Una dirección fácil de recordar que apunte al servidor (como `mi-web.com`).

**Byron:**
> ¿Qué me recomiendas tú? ¿Debería conocer el proceso por mí mismo o dejar que lo hagas tú solo?

**Antigravity:**
Te recomiendo un término medio: que entiendas el concepto haciéndolo tú mismo de la forma más sencilla. Usamos **Netlify Drop** (subir la carpeta arrastrándola al navegador).

**Byron:**
> Me han dado algo así:
> `https://byronsprimeraweb.netlify.app/`

**Antigravity:**
¡Felicidades! Tu página ya está en internet y es accesible desde cualquier parte del mundo.

**Byron:**
> ¿Y por qué no puedo poner `byronsprimeraweb.com` por ejemplo?

**Antigravity:**
* El `.netlify.app` es un **subdominio gratuito** cedido por Netlify (como una habitación de alquiler).
* El `.com` es un **dominio propio** (propiedad privada). Debe registrarse globalmente mediante entidades como la ICANN y tiene un coste anual (10-15 USD) para evitar la saturación de nombres en internet.

---

## Sesión 3: Estructura del Desarrollo Web (La Metáfora del Restaurante)

**Byron:**
> No sé qué más podríamos hacer. ¿Qué propones? La gente habla de agentes, bases de datos, frontend, backend, firewall... no entiendo muy bien esto.

**Antigravity:**
Imagina que una página web es un **restaurante**:

* **Frontend (La sala y la mesa):** Todo lo que el cliente ve y toca (el diseño, el menú, los cubiertos). Es el HTML, CSS y JavaScript que se ejecuta en el Chrome del usuario.
* **Backend (La cocina):** El área privada donde se prepara la comida y se procesan los pedidos. El servidor que procesa las contraseñas, pagos o datos complejos.
* **Base de Datos (La despensa):** El almacén donde se guardan las recetas, ingredientes y datos de los clientes de manera organizada.
* **Firewall (El guardia de seguridad):** Verifica quién entra al restaurante y bloquea a los visitantes sospechosos o peligrosos.
* **Agentes (Asistentes de IA):** Programas inteligentes (como yo) que ayudan a construir y automatizar cosas.

---

## Sesión 4: Persistencia y Servidores Locales (Lista de Tareas)

### Proyecto 2: Lista de Tareas Premium (To-Do List)
Creamos una aplicación que guarda tareas en la base de datos interna del navegador llamada **LocalStorage** para que no se borren al recargar.

* Código disponible en: [lista-tareas/index.html](file:///C:/Users/I758077/.gemini/antigravity/scratch/lista-tareas/index.html)

**Byron:**
> He hecho lo siguiente: escribí dos tareas. Cerré la página, volví a abrirla desde el Explorador de Windows y ¡nada!, no estaban las tareas. Luego hice clic, se abrió en Chrome y no aparecían.

**Antigravity:**
Se debe a la seguridad de los archivos locales (`file:///`):
* Chrome aísla los archivos locales del disco duro por seguridad para que un script malicioso no pueda robar datos. Esto significa que **no permite guardar información en LocalStorage de forma permanente** cuando se abre el archivo directamente con doble clic.
* Para solucionarlo, necesitamos un **servidor web** (`http://`).

**Byron:**
> ¿Qué crees que es mejor: subirlo al servidor o a Netlify? Quizás podamos probar lo del servidor. Nunca lo he probado y no sé qué implicaciones tiene esto de generar algo.

**Antigravity:**
Ejecuté un comando en la consola para levantar un servidor de pruebas local en el puerto 8000. Al acceder a `http://localhost:8000`, Chrome permite utilizar el LocalStorage porque detecta un protocolo HTTP legítimo.

**Byron:**
> Cuando hago doble clic en el archivo `index.html` de la lista de tareas en Chrome, no se ve nada de las tareas guardadas. Pero cuando entro al `localhost`, sí. ¿Cómo has enlazado este documento con el localhost? ¿Se hace en el mismo `index.html` o dónde?

**Antigravity:**
El archivo `index.html` no sabe nada de "localhost". Es exactamente el mismo archivo. Lo que cambió fue **cómo se lo entregamos al navegador**. 
* **`file://` (doble clic):** Chrome lee el archivo directamente del disco duro y bloquea funciones.
* **`http://localhost:8000`:** Levantamos un programa (servidor en Python) en esa carpeta. Cuando Chrome pide `localhost:8000`, el servidor lee el archivo `index.html` y se lo envía a Chrome como si fuera una web en internet.

---

## Sesión 5: Conexión con el Mundo Real (APIs y Perritos)

**Byron:**
> Pasemos al siguiente ejercicio. O sea, entiendo que tienes que escribir unos comandos, pero no sé de dónde escribes esos comandos.

**Antigravity:**
Los escribo en la **Terminal** (o Consola) del IDE. Es una interfaz de comandos de texto (como PowerShell en Windows). Puedes abrirla pulsando `Ctrl + \`` en tu IDE. Yo tengo conexión directa para ejecutar comandos automáticos allí.

### Proyecto 3: Conexión a APIs (Perritos y Consejos)
Creamos una aplicación conectada a internet en tiempo real que hace peticiones externas (usando la función `fetch` de JavaScript) a dos servidores públicos:
1. **Dog API (`dog.ceo`):** Trae imágenes aleatorias de perritos.
2. **Advice Slip API (`adviceslip.com`):** Trae consejos al azar en inglés.

* Servidor iniciado localmente en el puerto 8001: [http://localhost:8001](http://localhost:8001)
* Código disponible en: [conexion-api/index.html](file:///C:/Users/I758077/.gemini/antigravity/scratch/conexion-api/index.html)

**Byron:**
> En la primera página, mediante una función, lo has guardado en el local storage de Google Chrome... ¿Qué es storage? ¿Es de mi ordenador? Y en esta segunda, has creado una función para traer información de otras páginas web. Eso es lo que estoy entendiendo.

**Antigravity:**
¡Correcto!
* **LocalStorage (Almacenamiento Local):** Es una carpeta oculta dentro del disco duro administrada por Chrome donde guarda datos en formato Clave-Valor. Nadie en internet puede verlos; solo tú en tu ordenador.
* **APIs (Remoto):** Tu web pide y descarga datos de otros servidores en el mundo en tiempo real.

---

## Sesión 6: CSS Avanzado y Modo Claro/Oscuro (Tarjeta de Presentación)

### Proyecto 4: Tarjeta de Presentación Digital
Desarrollamos una tarjeta personal elegante con un selector de tema Claro/Oscuro (*Dark/Light Mode*).

* Servidor iniciado localmente en el puerto 8002: [http://localhost:8002](http://localhost:8002)
* Código disponible en: [tarjeta-presentacion/index.html](file:///C:/Users/I758077/.gemini/antigravity/scratch/tarjeta-presentacion/index.html)

Conceptos aplicados:
1. **Variables CSS (Custom Properties):** Definimos colores globales como `--bg-color` o `--text-primary`.
2. **Intercambio de Clases:** JavaScript añade o quita la clase `.light-theme` del elemento `body` al pulsar el botón de cambio de tema.
3. **Persistencia del Tema:** Guardamos la preferencia del tema en LocalStorage para que al recargar la página siga en el modo elegido.

---

## Resumen Técnico de Conceptos

| Concepto | Explicación Sencilla |
| :--- | :--- |
| **IDE** | El taller o editor donde escribimos el código y manejamos los archivos del proyecto. |
| **HTML** | La estructura física de la página (textos, botones, imágenes). |
| **CSS** | El estilo visual y estético de la página (colores, fuentes, animaciones). |
| **JavaScript** | El comportamiento inteligente e interactividad de la página. |
| **Hosting** | Almacenar tus archivos web en un servidor público conectado a internet todo el tiempo (ej. Netlify). |
| **Dominio** | El nombre de la dirección de la web (ej. `google.com`). |
| **LocalStorage** | Pequeña memoria local dentro del navegador en tu ordenador para guardar datos. |
| **API** | Una ventanilla en internet que permite que tu web pida información a otros servidores. |
| **Terminal** | La pantalla de texto donde se ejecutan comandos del sistema operativo de forma directa. |
| **Autenticación (OAuth)** | Permitir a los usuarios iniciar sesión de forma segura usando sus cuentas de Google, Apple o Facebook. |
| **Stripe** | Pasarela de pago segura que procesa tarjetas de crédito sin comprometer la seguridad de tu base de datos. |
| **Git / GitHub** | Historial de versiones del código para trabajar en equipo y desplegar automáticamente a producción. |
