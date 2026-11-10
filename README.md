# MiInflación

## Integrantes
- Ernesto Galindo Seijas -- [ErnesGS](https://github.com/ErnesGS)
- Manuel Castellón Reguero -- [manucr99](https://github.com/manucr99)
- José Manuel Pastor Lledó -- [jpastorlledo](https://github.com/jpastorlledo)

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
Principal dificultad o incertidumbre:** La calidad de los datos así como la información extra para detectar la probabilidad de incendio
- **Qué necesitaría comprobar:** Calidad suficiente de los datos.
