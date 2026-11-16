# 00 · Documento de inicio del proyecto

## 1. Datos del alumno/a

| | |
|---|---|
| **Nombre** (real o alias, como prefieras: [por qué](publicacion-y-privacidad.md)) | Saúl |
| **Usuario de GitHub** | Saulpa  |
| **Repositorio del proyecto** | https://github.com/Saulpa/proyecto-final-daw-saul |
| **Ciclo y curso** | DAW, 2.º · curso 2026-27 |
| **Fecha** | 2026-11-06 (última revisión: 2026-11-16) |

## 2. Nombre del proyecto

**Concesionario multimarca con showroom 3D interactivo** (nombre provisional, puede cambiar).

Aplicación web comercial que combina un catálogo de vehículos (nuevos, km 0 y de ocasión) con una experiencia tridimensional interactiva para explorar y personalizar determinados modelos.

## 3. Qué quiero hacer

Desarrollar la plataforma digital de un concesionario multimarca: una aplicación web con una página principal de vehículos destacados y un catálogo con búsqueda, filtros, ordenación y fichas (marca, modelo, precio, año, kilometraje, combustible y estado: nuevo, km 0 u ocasión) y, para determinados modelos, un showroom en 3D.

Desde el showroom, el usuario podrá ver el vehículo desde varias perspectivas: vistas predefinidas (frontal, lateral, trasera, superior), vista libre para girar alrededor del modelo y acercarse o alejarse, y una vista rotativa automática en la que el coche gira sobre una plataforma virtual. La cámara se desplaza con transiciones animadas al abrir el vehículo y al cambiar de vista.

También se podrá personalizar el vehículo cambiando el color de la carrocería y, si el modelo lo permite, las llantas, viendo el cambio reflejado en el modelo 3D. La personalización se plantea para vehículos nuevos y km 0 (un coche de ocasión no se puede repintar); en los de ocasión, el showroom se complementa con puntos de información sobre partes del vehículo (equipamiento, estado real) y con fotografías reales.

La parte comercial incluirá la ficha técnica, favoritos, comparación de vehículos y un formulario para solicitar información al concesionario.

Se usaría así: la persona que busca coche entra en la web, filtra el catálogo, abre el vehículo que le interesa en el showroom 3D, lo personaliza, lo guarda o lo compara y pide información.

Por detrás, un backend y una base de datos gestionan la información del catálogo que se muestra en la interfaz.

## 4. Qué problema o necesidad resuelve

Las webs de compraventa de vehículos convencionales tienden a quedarse en fotos fijas y una ficha plana: la persona compradora no puede explorar el vehículo con detalle ni, en nuevos y km 0, ver cómo queda con otro acabado antes de contactar, y los concesionarios multimarca carecen de un escaparate digital que ofrezca esa experiencia.

Cubrir esa necesidad con un catálogo completo más un showroom 3D interactivo permitiría al concesionario diferenciarse de un anuncio clasificado genérico y recoger consultas mejor cualificadas. El showroom no sustituye la revisión física de un coche de ocasión concreto: sirve para preseleccionar y llegar al concesionario mejor informado.

**Cómo lo sabes:** documentado en parte en `01-analisis.md` (apartado 2: Faconauto/GANVAM, OCU, Wallapop) y en `01b-sota.md` (apartados 2 y 5). Sigue siendo una hipótesis que la propuesta de valor del showroom 3D mejora la consulta; **pendiente** una fuente directa sobre la demanda de visualización 3D y comprobar qué ofrecen los concesionarios online de ocasión (antes de H1, 26-nov-2026).

## 5. Para quién

- **Cliente / promotor:** un concesionario multimarca, planteado como **encargo simulado** (sin usar información de ninguna empresa real).
- **Personas usuarias:** personas que buscan un vehículo (nuevo, km 0 o de ocasión) y quieren verlo en detalle, comparar modelos y plantear una consulta antes de desplazarse al concesionario.
- **Contexto:** proyecto académico de fin de ciclo; uso público de la web por parte de cualquier persona visitante.

## 6. Funcionalidades principales

| # | Funcionalidad | ¿Imprescindible? (sí / no) |
|---|---|---|
| 1 | Catálogo con búsqueda, filtros (marca, modelo, precio, año, kilometraje, combustible, estado), ordenación y fichas de vehículo | sí |
| 2 | Showroom 3D con transición de cámara, vistas predefinidas, vista libre y vista rotativa automática | sí |
| 3 | Backend y base de datos que alimenten el catálogo y las fichas | sí |
| 4 | Personalización visual en el modelo 3D: color de carrocería (sí); llantas, solo si el modelo lo permite (no) | sí (color) |
| 5 | Formulario de solicitud de información / contacto con el concesionario | sí |
| 6 | Favoritos y comparación de vehículos | no (deseable) |
| 7 | Página principal con vehículos destacados | no (deseable) |
| 8 | Puntos de información sobre partes del vehículo (equipamiento, estado real) | no (deseable) |

**Fuera de la primera versión mínima** (la que se quiere tener funcionando antes del 31-mar): vista inferior, vista interior del habitáculo y cambio de llantas. Dependrán de los modelos 3D disponibles y de la viabilidad técnica, y se concretarán con el tutor (apartado 5 de la propuesta).

## 7. Tecnologías previstas

| Tecnología | Para qué | Nivel actual (nada / algo / bien) |
|---|---|---|
| HTML5 + CSS3 (responsive) | Estructura y estilo de la interfaz, fichas y diseño adaptable | pendiente |
| JavaScript (ES6+) | Lógica de cliente: filtros, favoritos, comparación, control del showroom | pendiente |
| Three.js (WebGL) | Showroom 3D: cámara, transiciones, materiales y personalización | pendiente (habrá que aprenderlo) |
| Spring Boot con Java 21 | Backend REST que sirve el catálogo | pendiente |
| SQL (MySQL o PostgreSQL) | Almacenar vehículos y datos del catálogo | pendiente |
| Git y GitHub | Control de versiones y entrega de avances | pendiente |
| Despliegue de aplicaciones web | Publicar la aplicación (según módulo 0614) | pendiente |
| Modelos 3D (glTF/GLB) | Obtener, optimizar y licenciar los modelos del showroom | pendiente |

**Pendiente (Saúl):** rellenar la columna «Nivel actual» con tu nivel real (nada / algo / bien).

Los niveles se ajustan en la conversación con el tutor; el PDF define el qué, no el cómo técnico definitivo.

## 8. Dónde se integra con los módulos de 2.º

- [x] Desarrollo web en entorno cliente (0612) — filtros, fichas, favoritos, comparación y toda la lógica del visor 3D en el navegador.
- [x] Desarrollo web en entorno servidor (0613) — backend REST y base de datos con el catálogo de vehículos.
- [ ] Despliegue de aplicaciones web (0614) — **propuesta:** incluir un despliegue básico (demo pública) en la fase final, antes del 31-mar; pendiente de confirmar con el tutor.
- [x] Diseño de interfaces web (0615) — interfaz comercial moderna, clara y adaptable a distintos tamaños de pantalla.

## 9. Datos y empresas

- ¿El proyecto parte de una **empresa** (por ejemplo, de tus prácticas)? **No**. Se plantea como un **encargo simulado** para un concesionario multimarca, sin usar información real de ninguna empresa; no hace falta autorización escrita.
- ¿Usará **datos personales reales**? **No**: vehículos y fichas de ejemplo, mensajes de ejemplo y ninguna persona real identificada. Si se despliega públicamente, el formulario mostrará un aviso de demo («no introduzcas datos reales») y habrá un aviso legal y una política de privacidad mínimos.
- ¿Usará **contenido de terceros**? **Sí**: modelos 3D y fotografías de vehículos. Solo se usarán con licencia que permita su uso y modificación, anotando autor, licencia y enlace de cada uno.

## 10. Riesgos y dudas iniciales

- **Modelos 3D:** disponibilidad, licencia, peso y formato de los modelos; si los materiales permiten cambiar color o llantas, y si tienen detalle para la vista inferior o la interior, y si reproducen marcas o logotipos reales. Es lo que más condiciona el alcance.
- **Curva de aprendizaje:** Three.js y la integración del visor con la interfaz y el backend.
- **Alcance:** las funcionalidades 3D pueden crecer sin control; definir el alcance definitivo con el tutor (apartado 5 de la propuesta).
- **Tiempo:** conseguir la primera versión mínima antes del 31-mar sin descuidar la documentación de H1 y H2.
- **Orden de trabajo:** si el 3D (lo diferenciador y lo menos conocido) se deja para el final, un problema con los modelos llegaría tarde. Se propone una pequeña prueba de viabilidad 3D en diciembre (cargar un modelo, cambiar un material, mover la cámara) antes de cerrar el alcance.
- **Datos reales en un formulario público:** al desplegar la demo, alguien podría escribir datos personales reales; se mitiga con aviso visible y sin almacenar más de lo necesario.

## 11. Qué espero aprender

Integrar una experiencia 3D real dentro de una aplicación web comercial y aprender a llevar un proyecto de punta a punta —análisis, requisitos, backend, base de datos, interfaz y despliegue— organizándolo por hitos y con plazos.

---

## Aprobación del tutor

*Esta parte la rellena el tutor.*

| Criterio mínimo | Cumple |
|---|---|
| Necesidad real y documentada | ☐ |
| Alcance abordable en el tiempo disponible | ☐ |
| Integra contenidos de al menos tres módulos de 2.º | ☐ |
| No usa datos personales reales | ☐ |

**Estado:** ☐ Aprobada · ☐ Aprobada con cambios · ☐ Necesita rehacerse

**Fecha:** 

**Comentarios del tutor:**
