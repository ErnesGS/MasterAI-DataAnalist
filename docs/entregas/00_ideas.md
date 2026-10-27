# Ideas de producto para el Master

## Integrantes
- Ernesto Galindo Seijas -- [ErnesGS](https://github.com/ErnesGS)
- Manuel Castellón Reguero -- [manucr99](https://github.com/manucr99)
- José Manuel Pastor Lledó -- [jpastorlledo](https://github.com/jpastorlledo)

**Las ideas que se presentan a continuación están aquí para facilitar el feedback, tambien se podrá encontrar esté documento en docs/entregas/00_ideas.md**

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

### Primera versión o MVP
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

### Primera versión o MVP
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

### Primera versión o MVP
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

### Primera versión o MVP
- **Funciones mínimas:** Superposición estática de prenda 2D sobre silueta con tracking de pose básico (3-4 poses) en tiempo real.
- **Qué mostraríamos funcionando:** Demo con 1 prenda vectorizada, seguimiento básico al moverse levemente, render sobre persona.
- **Qué dejaríamos fuera por ahora:** Ajuste fiel a medidas exactas, drapeado realista, multi-prenda, integración e-commerce completa.

### Viabilidad y dudas
- **Principal dificultad o incertidumbre:** Realismo (ajuste al movimiento) vs complejidad; tracking estable con iluminación variable.
- **Qué necesitaría comprobar:** Calidad suficiente con tracking ligero, aceptación de ambos usuarios (comprador vs sastre - necesidades distintas), latencia.

## Comparativa rápida
| Idea | Claridad problema | Facilidad MVP | Acceso datos | Riesgo principal |
|---|---|---|---|---|
| Gafas adaptativas IA | Alta (seguridad) | Dificil | Media (crítico, fiabilidad) | Seguridad y fiabilidad |
| Aforo con dron | Media | Medio | Media | Normativa drones y privacidad |
| Optimización tráfico | Alta | Media-Alta (analítico) | Dificil (datos restringidos) | Acceso a datos y autorización |
| Probador virtual (*FitMirror*) | Alta | Media-Alta (técnico) | Facil | Realismo |