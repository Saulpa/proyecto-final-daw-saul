# 01b · Estado del arte (SOTA) de mi proyecto

## 1. Problema y preguntas de búsqueda (CE 1c)

**Problema:** Un concesionario multimarca necesita mostrar sus vehículos (nuevos, km 0 y de ocasión) en tres dimensiones y permitir explorarlos a distancia. En las páginas de los portales de anuncios revisadas, la presentación se apoya sobre todo en fotografías planas y esa exploración no aparece como función estándar (pendiente de comprobar si algunos anuncios incluyen vídeo o vista 360º).

Búsqueda hecha con buscadores web (DuckDuckGo y Google) y navegación directa de las webs oficiales de cada solución, el 13-11-2026. No se han usado tiendas de aplicaciones ni repositorios de proyectos en esta primera fase.

| # | Pregunta | Dónde busqué | Fecha |
|---|---|---|---|
| P1 | ¿Qué soluciones digitales existen ya para buscar, ver y comprar vehículos a distancia? | Buscador web y webs oficiales de los portales de anuncios: coches.net, AutoScout24 y Wallapop | 2026-11-13 |
| P2 | ¿Cómo ganan dinero esas soluciones (publicación gratuita, packs, servicios opcionales de pago)? | Condiciones de uso y páginas de venta o ayuda de los portales; página de precios de CloudPano | 2026-11-13 |
| P3 | ¿Qué tecnologías usan para el 3D y los recorridos 360º? | threejs.org (ejemplo de carrocería), GitHub (licencia del proyecto), mhp.com (configurador de CUPRA) y cloudpano.com | 2026-11-13 |
| P4 | ¿Qué tamaño tiene el mercado español de vehículos de ocasión? | Notas de prensa de Faconauto (faconauto.com) y nota de prensa de Wallapop | 2026-11-13 |
| P5 | ¿Qué propone la alternativa no digital (revisión física y papeleo) a la hora de comprar un coche de ocasión? | Guía «Comprar coche de segunda mano» de la OCU | 2026-11-13 |

**Preguntas pendientes.** P6: ¿qué concesionarios online de ocasión ofrecen ya vistas 360º o 3D en sus fichas? (webs oficiales, todavía por determinar). P7: ¿qué componentes 3D ya hechos existen y qué limitan frente a three.js? (documentación de `<model-viewer>` y de Sketchfab, todavía por determinar).

## 2. Soluciones existentes (CE 1a, 1c, 2a)

| Solución | Para quién | Qué hace | Modelo de precio | Enlace y fecha de acceso | Estado (`leído` / `sin leer`) |
|---|---|---|---|---|---|
| **coches.net** (Adevinta Motor S.L.U.) | Particulares y profesionales en España | Portal de anuncios de vehículos: búsqueda con criterios de clasificación, fichas y publicación de anuncios; publica además en otros portales del grupo | Publicación gratuita con carácter general y «Anuncios gratis» para particulares; servicios de pago para destacar y «Pack Segundamano» para publicar en otros portales | https://www.coches.net/condiciones-de-uso/ (2026-11-13) | `leído` |
| **AutoScout24** (Sumauto S.L.) | Particulares y profesionales, España y Europa | Portal internacional de anuncios de compra y venta de vehículos, con publicación del anuncio y servicios opcionales | Publicación gratuita («Vende tu coche gratis») y servicios de pago opcionales, como el pago seguro (SafeTrade) | https://www.autoscout24.es/vender-coche/ (2026-11-13) | `leído` |
| **Wallapop** | Particulares (venta entre particulares), categoría Motor | Marketplace generalista con anuncios de coches, mensajería con el anunciante y servicios de valor añadido | Publicación gratuita; servicios opcionales de pago, como la Protección Mecánica (pago único del vendedor, prestación de hasta 3.000 € durante 3 meses) | https://about.wallapop.com/los-3-aspectos-a-revisar-antes-de-comprar-un-coche-de-segunda-mano-segun-wallapop y https://ayuda.wallapop.com/hc/es-es/articles/48825530260753-Protecci%C3%B3n-Mec%C3%A1nica-para-venta-de-coches-de-particulares (2026-11-13) | `leído` |
| **Configurador de vehículo de CUPRA desarrollado por MHP** | Fabricante (CUPRA) y su red comercial | Configurador de vehículo en 3D en la nube, «selectable with just one click»; MHP asesora, desarrolla y opera la plataforma 3D y en la nube | No es un producto público: prestación de servicios B2B (consultoría, desarrollo y operación de plataforma) | https://www.mhp.com/en/insights/newsroom/news-detail/view/digital-vehicle-selection-at-cupra-with-just-one-click (2026-11-13) | `leído` |
| **CloudPano** | Concesionarios y profesionales que quieren recorrer un vehículo o un inmueble en 360º | Software en la nube de recorridos 360º y «spins» (giros) de vehículo, con embebido en la web y creación desde el móvil | Freemium: 3 recorridos gratis que caducan a los 120 días; plan PRO 27 $/mes; plan PRO PLUS 33 $/mes facturado anualmente | https://www.cloudpano.com/learn/cloudpano-pricing (2026-11-13) | `leído` |
| **three.js**, ejemplo `webgl_materials_car` | Desarrolladores web | Biblioteca JavaScript de gráficos 3D en el navegador con WebGL; el ejemplo «car materials» pinta la carrocería de un Ferrari 458 Italia sobre su modelo (autor: vicent091036) | Gratuita y de código abierto (licencia MIT) | https://threejs.org/examples/webgl_materials_car.html y https://raw.githubusercontent.com/mrdoob/three.js/dev/LICENSE (2026-11-13) | `leído` |
| **Guía de compra de coche de segunda mano de la OCU** (alternativa no digital) | Consumidores particulares | Proceso físico de compra: revisión del coche y prueba en carretera, contratación de una revisión profesional, revisión de papeles y negociación del precio con guías de valores; sin plataforma ni visualización 3D | Servicio de la OCU (contenido generalmente para socios); el proceso descrito no exige coste de plataforma | https://www.ocu.org/coches/coches/informe/comprar-coche-segunda-mano (2026-11-13) | `leído` |

**Pendiente de comprobar (aún no son soluciones revisadas).** P6: si algún concesionario online de ocasión ofrece vistas 360º o 3D en sus fichas. P7: qué control de cámara, transiciones y materiales permiten `<model-viewer>` y Sketchfab.

## 3. Modelos de negocio (CE 1d, 1e)

*Qué **patrones** se repiten en las soluciones del apartado 2 (suscripción, *freemium*, comisión por operación, licencia, publicidad, servicio gratuito o público) y por qué. Describe con un **Business Model Canvas** (opcional; el profesor te da el material) **2-3 casos**. Termina con el modelo que seguiría **tu** proyecto, o qué ahorra o mejora si no es un negocio.*

| Patrón | Soluciones que lo usan | Ventaja | Riesgo |
|---|---|---|---|
| [RELLENAR] | | | |

## 4. Herramientas y tecnologías (CE 2a, 2b)

*Para cada decisión técnica importante (lenguaje y *framework*, base de datos, despliegue, autenticación…), compara **2-3 opciones con los mismos criterios**. Marca la que eliges.*

| Decisión | Opción | Madurez | Licencia | Coste | Curva de aprendizaje | Encaje con el ciclo | Elegida |
|---|---|---|---|---|---|---|---|
| [RELLENAR: p. ej. base de datos] | | | | | | | |

*Cada decisión importante se convierte en una decisión registrada en [`decisiones/`](decisiones/0000-plantilla.md).*

## 5. Hueco y diferenciación (CE 1e)

**Qué no cubren las soluciones anteriores.** Los portales de anuncios (coches.net, AutoScout24, Wallapop) reúnen millones de anuncios, pero en las páginas revisadas la decisión de compra se apoya en fotografías planas y en una inspección posterior en el concesionario; no aparece una exploración desde varias vistas ni una personalización antes de contactar (pendiente de comprobar si algún anuncio ofrece vídeo o 360º). El configurador de fabricante estudiado (CUPRA con MHP) sí da una experiencia 3D inmersiva, pero es de una sola marca, orientado a vehículos nuevos y es un sistema cerrado, no un catálogo multimarca. CloudPano y los «spins» a 360º exigen sesiones de captura reales del vehículo y una suscripción desde 27 $/mes. three.js aporta la tecnología de render, pero es una biblioteca: no trae catálogo, filtros, fichas ni servidor. Falta comprobar los concesionarios online de ocasión y los visores 3D embebibles (P6 y P7).

**Propuesta de valor.** Mi proyecto reúne en una sola aplicación dos piezas que hoy se reparten en productos distintos: un catálogo multimarca (nuevos, km 0 y ocasión) con búsqueda, filtros y comparador, y un showroom 3D donde el usuario mira el vehículo de frente, de lado y por arriba, lo gira libremente, lo ve girar sobre una plataforma y, en nuevos y km 0, le cambia el color de la carrocería, todo sin salir de la web y sin coste de licencias de software (three.js es MIT). En los vehículos de ocasión, el showroom se complementa con puntos de información sobre el equipamiento y el estado real, y con fotografías reales. Es una propuesta para que un concesionario pequeño dé a sus vehículos una presentación que hoy está sobre todo al alcance de los configuradores de las grandes marcas.

**Límite honesto.** Para comprar hoy un coche con garantía, historial verificado y servicios como la Protección Mecánica de Wallapop, los grandes portales son mejores que mi proyecto: éste es un encargo simulado, sin transacción, sin verificación de kilometraje y sin catálogo real. Además, un modelo 3D genérico no refleja el estado real de un coche de ocasión concreto, por lo que el showroom ayuda a preseleccionar y no sustituye la revisión física. «Sin coste de licencias» se refiere al software: los modelos 3D tienen su propia licencia y su obtención cuesta tiempo. Su valor está en el proceso de desarrollo y en la experiencia de visualización, no en sustituir a un mercado consolidado.

## 6. Decisiones derivadas (CE 1e, 1f, 2b)

*Qué consecuencias tiene este estudio en tu proyecto.*

- **Tipo de proyecto elegido** (enlaza con el apartado 3 de [`01-analisis.md`](01-analisis.md)): [RELLENAR]
- **Requisitos que salen del estudio** (con su ID del apartado 4 de `01-analisis.md`): [RELLENAR]
- **Decisiones técnicas** (enlace a cada archivo de `decisiones/`): [RELLENAR]

## 7. Fuentes y calidad (CE 2a)

*Al menos **2 fuentes independientes** (no dos páginas de la misma empresa). Datos oficiales o primarios antes que blogs.*

| # | Fuente (enlace) | Tipo | Fecha de acceso | Fiabilidad (alta / media / baja) y por qué |
|---|---|---|---|---|
| F1 | [RELLENAR] | | | |

## 8. Límites

*Qué **no pudiste comprobar** y qué datos son estimaciones. Una lista corta y honesta es mejor que fingir certeza.*

- [RELLENAR]

---

## Criterios de evaluación que alimenta este documento (texto literal)

- **1a)** Se han clasificado las empresas del sector por sus características organizativas y el tipo de producto o servicio que ofrecen.
- **1c)** Se han identificado las necesidades más demandadas a las empresas.
- **1d)** Se han valorado las oportunidades de negocio previsibles en el sector.
- **1e)** Se ha identificado el tipo de proyecto requerido para dar respuesta a las demandas previstas.
- **1f)** Se han determinado las características específicas requeridas al proyecto.
- **2a)** Se ha recopilado información relativa a los aspectos que van a ser tratados en el proyecto.
- **2b)** Se ha realizado el estudio de viabilidad técnica del mismo.

> El SOTA **no añade criterios de evaluación**: reúne en un solo sitio lo que 1a-1f y 2a-2b ya piden. La evaluación sigue las listas de cotejo de H1 y H2.
