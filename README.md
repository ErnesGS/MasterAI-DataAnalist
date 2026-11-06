# Ideas de producto para el Master

## Integrantes
- Ernesto Galindo Seijas -- [ErnesGS](https://github.com/ErnesGS)
- Manuel Castellón Reguero -- [manucr99](https://github.com/manucr99)
- José Manuel Pastor Lledó -- [jpastorlledo](https://github.com/jpastorlledo)

**Las ideas que se presentan a continuación están aquí para facilitar el feedback, tambien se podrá encontrar esté documento en [docs/entregas/00_ideas.md](https://github.com/ErnesGS/MasterAI-DataAnalist/blob/main/docs/entregas/00_ideas.md)**

## 1) Gafas con IA enfocada a la adaptabilidad

### Título y descripción
- **Nombre provisional:** *Gafas_de_adaptación_visual*
- **Descripción:** Rediseño del software de unas gafas con inteligencia artificial orientado a mejorar la autonomía de personas con discapacidad visual mediante información contextual adaptada al entorno.

### Problema y usuario
- **Necesidad concreta:** Dificultad para orientarse y detectar cambios peligrosos en el entorno (semáforos, cambios de nivel, obstáculos) sin depender constantemente de terceros.
- **Usuario objetivo:** Personas con discapacidad visual (baja visión o ceguera total) que usan ayudas técnicas (bastón, perro guía).
- **Resolución actual:** Bastón, perro guía, aplicaciones de navegación accesibles, orientación con familiares.

### Uso y valor
- **Situación de uso:** Una persona con ceguera cruza una calle con semáforo peatonal. Al acercarse, las gafas detectan el semáforo y su estado (rojo o verde) y avisan con antelación, advirtiendo también de cambios de nivel (bordillos, escalones) próximos.
- **Lo que recibe:** Alertas auditivas o vibraciones contextualizadas y priorizadas según urgencia.
- **Cómo le ayuda:** Le permite decidir con mayor autonomía, reducir ansiedad y anticiparse a riesgos. Valor: mayor independencia y seguridad.

### Datos
- **Necesarios:** Imágenes del entorno (semáforos peatonales, bordillos, escalones), ubicación GPS, orientación, estado semafórico.
- **Fuentes candidatas:** [OpenStreetMap](https://www.openstreetmap.org/), datasets de semáforos peatonales, imágenes sintéticas, propias. *(Hipótesis: no hay dataset público confirmado para el estado en tiempo real de todos los semáforos.)*
- **Restricciones:** Mayoría hipótesis. Privacidad (procesamiento en movil), imagen, seguridad crítica (falsos negativos peligrosos).

### MVP
- **Funciones mínimas:** Detección de bordillos y cambios de nivel + alerta.
- **Qué mostraríamos funcionando:** Demo con vídeo simulando el acercamiento a un bordillo.
- **Qué dejaríamos fuera por ahora:** Integración completa, sensores de profundidad y avisos más complejos (dificultad elevada, posible descarte).

### Viabilidad y dudas
- **Principal dificultad o incertidumbre:** Fiabilidad crítica (seguridad). La detección de semáforos en tiempo real es compleja y varía por ciudad.
- **Qué necesitaría comprobar:** Precisión en detección de cambios de nivel con hardware ligero, latencia aceptable, aceptabilidad con usuarios reales y qué información puede obtenerse de forma fiable.

## 2) Sistema de aproximación de aforo

### Título y descripción
- **Nombre provisional:** *Calculador_de_Aforo*
- **Descripción:** Sistema basado en dron para estimar el aforo aproximado de lugares o eventos, proporcionando una estimación útil sin necesidad de un conteo manual exhaustivo.

### Problema y usuario
- **Necesidad concreta:** Saber el aforo aproximado para la gestión de espacios,eventos (seguridad, aforo máximo, congestión).
- **Usuario objetivo:** Organizadores de eventos, responsables de seguridad, ayuntamientos o comercios con aglomeraciones.
- **Resolución actual:** Conteo manual, aforos teóricos, estimaciones visuales.

### Uso y valor
- **Situación de uso:** En un evento al aire libre, el organizador quiere recopilar información sobre cuanta gente ha asistido. 
Despliega el dron brevemente y obtiene una estimación de personas por zona.
- **Lo que recibe:** Mapa con aforo aproximado (rango o densidad), con alerta si se acerca a un umbral.
- **Cómo le ayuda:** Toma decisiones de gestión más rápidas y evita aglomeraciones.

### Datos
- **Necesarios:** Imágenes aéreas desde dron, zona de interés, umbrales de aforo.
- **Fuentes candidatas:** Vuelos propios de prueba *(hipótesis)*, datasets de detección de personas en vistas aéreas (ej. [VisDrone](https://github.com/VisDrone/VisDrone-Dataset), [CrowdHuman](https://www.crowdhuman.org/)) *(hipótesis, a consultar)*.
- **Restricciones:** Solo confirmado con pruebas propias. Normativa de drones (espacio aéreo, autorizaciones), privacidad (personas identificables), permisos en zonas públicas.

### MVP
- **Funciones mínimas:** Conteo aproximado por zona con imagen estática (o vídeo corto), mostrando estimación numérica con margen de error.
- **Qué mostraríamos funcionando:** Captura simulada o real en zona controlada.
- **Qué dejaríamos fuera por ahora:** Seguimiento en tiempo real, análisis predictivo, integración con sistemas de control de acceso.

### Viabilidad y dudas
- **Principal dificultad o incertidumbre:** Cumplimiento normativo de drones + fiabilidad en aglomeraciones densas.
- **Qué necesitaría comprobar:** Autorizaciones necesarias, precisión aceptable para toma de decisiones (no requiere conteo exacto), rendimiento con vistas aéreas.

## 3) Sistema de optimización de tráfico

### Título y descripción
- **Nombre provisional:** *Optimización_de_tráfico*
- **Descripción:** Analizar datos de tráfico en zonas con alta congestión (horarios y eventos) para proponer ajustes (tiempos de semáforos, refuerzo policial, logística).

### Problema y usuario
- **Necesidad concreta:** Congestión recurrente que afecta a la movilidad y al tiempo de desplazamiento.
- **Usuario objetivo:** Ayuntamientos (movilidad, tráfico), policías locales, gestores de eventos.
- **Resolución actual:** Ajustes manuales por experiencia, medidas puntuales.

### Uso y valor
- **Situación de uso:** Tras prever un evento, se anticipan zonas con mayor congestión. Con el análisis de patrones, se propone redistribución de tiempos semafóricos o refuerzo en puntos críticos.
- **Lo que recibe:** Informe con puntos críticos, causas probables y propuesta de medidas con impacto esperado.
- **Cómo le ayuda:** Tomar decisiones preventivas en lugar de reactivas, optimizando recursos limitados.

### Datos
- **Necesarios:** Históricos de intensidad de tráfico, semáforos, eventos, incidentes, meteorología, aparcamiento.
- **Fuentes candidatas:** Portales de datos abiertos de ayuntamientos (tráfico), datos de eventos municipales. *(Hipótesis, varían según ciudad.)*
- **Restricciones:** Mayoritariamente hipótesis (acceso a datos en tiempo real frecuentemente restringido). Sensibilidad (infraestructura), licencias de datos, no modificar semáforos directamente sin integración autorizada.

### MVP
- **Funciones mínimas:** Análisis estático de histórico (una intersección + un tipo de evento) mostrando correlación hora-evento/congestión y propuesta sencilla de ajuste.
- **Qué mostraríamos funcionando:** Dashboard con heatmap por hora y recomendación textual (simulada con datos abiertos limitados).
- **Qué dejaríamos fuera por ahora:** Control en tiempo real de semáforos, predicción compleja multi-intersección, integración con agentes de tráfico.

### Viabilidad y dudas
- **Principal dificultad o incertidumbre:** Acceso a datos reales y autoridad para implementar medidas.
- **Qué necesitaría comprobar:** Disponibilidad de dataset histórico abierto usable, validación de la propuesta con un técnico de movilidad, alcance puramente analítico vs actuador.

## 4) Probador virtual (*FitMirror*)

### Título y descripción
- **Nombre provisional:** *FitMirror*
- **Descripción:** Cámara que captura el movimiento de una persona y proyecta una prenda vectorizada sobre ella imitando sus movimientos, orientado a "probar" sin cambiarse. También útil para sastres (previsualización rápida antes de coser).

### Problema y usuario
- **Necesidad concreta:** Probar ropa sin cambiarse físicamente o previsualizar modificaciones antes de la confección.
- **Usuario objetivo:** Compradores online, físicos y sastres (pequeños talleres).
- **Resolución actual:** Probador físico, fotos estáticas, intentos manuales de muestra; para sastres, bocetos o muestras físicas.

### Uso y valor
- **Situación de uso:** Comprador quiere ver cómo queda una prenda antes de comprarla online o sin cola en tienda. Sastre muestra una modificación propuesta al cliente proyectada sobre su silueta para validar antes de cortar la tela.
- **Lo que recibe:** Visualización en tiempo real de la prenda superpuesta adaptada al movimiento.
- **Cómo le ayuda:** Ahorra tiempo o iteraciones costosas (sastrería).

### Datos
- **Necesarios:** Vídeo, modelo vectorial de las prenda, mapeo de cuerpo, texturas.
- **Fuentes candidatas:** Prendas propias vectorizadas para demo, modelos de pose open source: [MediaPipe](https://developers.google.com/mediapipe). *(Acceso confirmado a herramientas OSS; catálogo, prendas, licencias: hipótesis.)*
- **Restricciones:** Privacidad (vídeo en tiempo real), derechos de catálogo, rendimiento en hardware modesto.

### MVP
- **Funciones mínimas:** Superposición estática de prenda 2D sobre silueta con tracking de pose básico (3-4 poses) en tiempo real.
- **Qué mostraríamos funcionando:** Demo con 1 prenda vectorizada, seguimiento básico al moverse levemente, render sobre persona.
- **Qué dejaríamos fuera por ahora:** Ajuste fiel a medidas exactas, drapeado realista, multi-prenda, integración e-commerce completa.

### Viabilidad y dudas
- **Principal dificultad o incertidumbre:** Realismo (ajuste al movimiento) vs complejidad; tracking estable con iluminación variable.
- **Qué necesitaría comprobar:** Calidad suficiente con tracking ligero, aceptación de ambos usuarios (comprador vs sastre - necesidades distintas), latencia.

## 5) Analizador de inflación personalizada (*MiInflación*)

### Título y descripción

- **Nombre provisional:** *MiInflación*
- **Descripción:** Aplicación que permite estimar cómo afecta la inflación al presupuesto de un hogar en función de sus gastos en distintas categorías de consumo, utilizando datos oficiales del Instituto Nacional de Estadística (INE).

### Problema y usuario

- **Necesidad concreta:** La inflación general publicada no refleja necesariamente la pérdida de poder adquisitivo de cada hogar, debido a las diferencias en sus hábitos de consumo.
- **Usuario objetivo:** Hogares, estudiantes y particulares interesados en comprender la evolución de sus gastos y planificar su presupuesto.
- **Resolución actual:** Consulta del IPC general, aplicaciones de presupuestos personales u hojas de cálculo, sin relacionar necesariamente los gastos individuales con la evolución de precios de cada categoría.

### Uso y valor

- **Situación de uso:** Un usuario introduce cuánto destina mensualmente a alimentación, transporte, vivienda y ocio. Selecciona un período de referencia y consulta cuánto habría variado el coste estimado de mantener su cesta de consumo.
- **Lo que recibe:** Estimación de inflación personalizada, evolución del presupuesto y desglose de las categorías que más contribuyen al incremento de costes.
- **Cómo le ayuda:** Permite identificar qué grupos de gasto afectan más a su presupuesto y mejorar la planificación financiera del hogar.

### Datos

- **Necesarios:** Series históricas mensuales del IPC por grupos de consumo, índices de precios, variaciones temporales, fechas y cantidades presupuestadas por el usuario.
- **Fuentes candidatas:** [INE - Índice de Precios de Consumo](https://www.ine.es/), [API JSON del INE](https://www.ine.es/dyngs/DAB/index.htm?cid=1099). *(Acceso público y API documentados; selección y descarga de las series concretas pendientes de comprobar.)*
- **Restricciones:**  Las categorías del IPC son agregadas y no representan necesariamente los precios específicos pagados por cada usuario. Los presupuestos introducidos pueden tratarse localmente para evitar almacenar información personal.

### MVP

- **Funciones mínimas:** Introducción manual del presupuesto mensual por categorías, selección de un período de comparación y cálculo de la variación estimada del coste de mantener la misma cesta utilizando índices oficiales del IPC.
- **Qué mostraríamos funcionando:** Aplicación web sencilla con formulario de gastos, resultado de inflación personalizada y gráfico comparativo de las contribuciones de cada categoría al cambio del presupuesto.
- **Qué dejaríamos fuera por ahora:** Conexión con cuentas bancarias, reconocimiento de tickets, predicciones futuras de inflación, recomendaciones automáticas y seguimiento continuo de gastos.

### Viabilidad y dudas

- **Principal dificultad o incertidumbre:** Correspondencia entre las categorías introducidas por el usuario y las publicadas por el INE, así como la correcta interpretación de una inflación personalizada estimada.
- **Qué necesitaría comprobar:** Disponibilidad y compatibilidad de las series históricas del IPC, cambios de base y clasificación, correspondencia entre categorías y facilidad de uso del formulario. Validar los cálculos con ejemplos reproducibles y comprobar si los usuarios encuentran útil el resultado.

## Comparativa rápida
| Idea | Claridad problema | Facilidad MVP | Acceso datos | Riesgo principal |
|---|---|---|---|---|
| Gafas adaptativas IA | Alta (seguridad) | Dificil | Media (crítico, fiabilidad) | Seguridad y fiabilidad |
| Aforo con dron | Media | Medio | Media | Normativa drones y privacidad |
| Optimización tráfico | Alta | Media-Alta (analítico) | Dificil (datos restringidos) | Acceso a datos y autorización |
| Probador virtual (*FitMirror*) | Alta | Media-Alta (técnico) | Facil | Realismo |
| **MiInflación** | Alta | Alta | Facil | Representatividad del IPC |

## 6) Detección y predicción temprana de incendios forestales

### Título y descripción

- **Título provisional:** Detección y predicción temprana de incendios forestales.
- **Descripción:** Sistema que permite proteger y preservar los entornos forestales para detectar incendios utilizando Inteligencia Artificial. Analizando los datos forestales, se pretende prevenir incendios y en caso de producirse alguno, detectarlo de manera temprana, para contribuir de una manera eficiente en la gestión y sostenibilidad de los bosques.

### Problema y usuario

- **Necesidad concreta:** Disminuir el riesgo de incendio y en caso de producirse, evitar que sea de grandes dimensiones, de manera que se protejan los entornos forestales.
- **Usuario objetivo:** Organizaciones responsables de la protección, vigilancia y gestión de los entornos forestales.
- **Resolución actual:** Actualmente, la protección y vigilancia de los bosques depende de inspecciones presenciales, detecciones de incendios limitadas y de la intervención del ser humano. Esto dificulta la dificulta detectar con rapidez incendios forestales o cambios ambientales.

### Uso y valor

- **Situación de uso:** Desde satélite o vigilancia aérea, se pretende monitorear el terreno forestal, detectando las zonas en las que hay alta probabilidad de incendio o aquellas zonas en las que el incendio ya se ha producido.
- **Lo que recibe:** Se recibe un aviso de incendio o probabilidad de incendio para vigilancia humana.
- **Cómo le ayuda:** Permite detectar zonas con alto riesgo de incendio o incendios ya producidos para que se vigilen dichas zonas.

### Datos

- **Necesarios:** Imágenes aéreas desde satélite de incendios y series históricas de humedad, viento, temperatura, etc...
- **Fuentes candidatas:** [NASA FIRMS – Detección de incendios](https://firms.modaps.eosdis.nasa.gov/content/active_fire/?utm_source=chatgpt.com), [AEMET OpenData – Meteorología](https://www.aemet.es/es/datos_abiertos/AEMET_OpenData?utm_source=chatgpt.com), [Copernicus EFFIS – Riesgo de incendios](https://forest-fire.emergency.copernicus.eu/applications/data-and-services?utm_source=chatgpt.com), [Copernicus Sentinel-2 – Imágenes satelitales](https://dataspace.copernicus.eu/?utm_source=chatgpt.com), [MITECO EGIF – Historial de incendios en España](https://servicio.mapa.gob.es/incendios/Search/Publico?utm_source=chatgpt.com)
- **Restricciones:**  Algunos datos están desactualizados, dificultad para integrar las bases de datos, falta de información, algunas zonas forestales pueden no disponer de toda la información.

### MVP

- **Funciones mínimas:** Detectar un incendio en una imagen dada o detectar la probabilidad de incendio en una zona forestal.
- **Qué mostraríamos funcionando:** Aplicación web sencilla en la que se detecte el incendio o la probabilidad de incendio de una zona.
- **Qué dejaríamos fuera por ahora:** Pruebas en tiempo real en vídeo.

### Viabilidad y dudas

- **Principal dificultad o incertidumbre:** La calidad de los datos así como la información extra para detectar la probabilidad de incendio
- **Qué necesitaría comprobar:** Calidad suficiente de los datos.
