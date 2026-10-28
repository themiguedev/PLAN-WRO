# Plan de Desarrollo Técnico y Competitivo: LEGO SPIKE Prime
**Enfoque:** Robótica Educativa y World Robot Olympiad (RoboMission)  
**Niveles:** Elementary (8 - 12 años) | Junior (11 - 15 años) | Senior (14 - 19 años)  

---

## 1. Marco General de Fases de Evolución

El progreso técnico de los estudiantes se estructura en cuatro fases continuas:

`
[ Fase 1: Alfabetización ] ──► [ Fase 2: Adaptabilidad ] ──► [ Fase 3: Ingeniería WRO ] ──► [ Fase 4: Optimización ]
  Mecánica y algoritmos           Sensores y lógica libre        Cinemática y robustez         Estrategia y torneo
`

* **Fase 1: Alfabetización Mecánica y Algorítmica (Construcción Guiada y Bloques Base):** Comprensión de vigas, pasadores, ejes, simetría estructural, lectura de instrucciones, engranajes elementales y programación secuencial/condicional básica.
* **Fase 2: Adaptabilidad Creativa e Integración Sensorial:** Modificación libre de modelos existentes, incorporación de sensores (color, distancia, giroscopio), bucles de repetición y resolución de obstáculos sin guía.
* **Fase 3: Ingeniería Competitiva y Cinemática WRO:** Diseño de chasis compactos dentro del cubo de  \times 25 \times 25\text{ cm}$, cálculo de relaciones de transmisión, odometría, movimiento con control giroscópico y seguimiento de líneas.
* **Fase 4: Ejecución Estratégica y Calibración:** Rutinas completas de tapete, protocolos contra fallos mecánicos, tolerancia a variaciones lumínicas, optimización temporal (límite de 2 minutos) y manejo de rondas sorpresa.

---

## 2. Plan Mensual de Nivelación: Noviembre
* **Régimen:** 8 sesiones al mes (Martes y Jueves).
* **Objetivo:** Nivelar fundamentos mecánicos, control motriz y lógica de programación antes de la temporada competitiva.

| Sesión | Nivel Elementary (8 - 12 años) | Nivel Junior (11 - 15 años) | Nivel Senior (14 - 19 años) |
| :--- | :--- | :--- | :--- |
| **Semana 1 - M1**<br>*Chasis y Tracción* | Ensamble guiado del chasis base estándar. Reconocimiento de piezas clave y simetría. Movimiento rectilíneo por rotaciones y grados. | Construcción de chasis rígido con centro de gravedad bajo. Cálculo de avance lineal ($ por rotación en base al diámetro de rueda). | Cinemática diferencial, cálculo de momento de inercia y diseño de chasis para aceleración estable sin derrape de neumáticos. |
| **Semana 1 - J1**<br>*Precisión y Giros* | Giros en un punto (pivote) vs. giros suaves (diferencial). Trazado de trayectorias cuadradas simples con cinta adhesiva. | Giros de 90° calibrados mediante el sensor giroscópico integrado (Yaw angle). Corrección de inercia y uso de freno activo (hold). | Implementación de control proporcional ($) en giros giroscópicos para eliminar subgiros y sobregiros por inercia residual. |
| **Semana 2 - M2**<br>*Sensores de Color & Lógica* | Detección de colores sólidos (semáforo: rojo = parada, verde = avance). Parada inmediata sobre cinta negra. | **Transición Bloques vs Python I:** Calibración de reflectancia $\frac{L_{blanco} + L_{negro}}{2}$ en bloques condicionales vs. su sintaxis equivalente en script Python (color_sensor.reflection()). | Sistema de doble sensor frontal para autoalineación en líneas perpendiculares (*line squaring*) e interpolación continua de lecturas. |
| **Semana 2 - J2**<br>*Sensores de Distancia & Control* | Sensor ultrasónico: detección de barreras fijas y frenado automático a \text{ cm}$ de distancia sin colisión. | **Transición Bloques vs Python II:** Comparativa de bucles: estructuras de espera en bloques frente a ciclos while y condicionales de evasión en código escrito. | Mapeo de zonas ocupadas mediante lecturas de distancia en movimiento, guardando el estado en variables lógicas/booleanas. |
| **Semana 3 - M3**<br>*Módulos Mecánicos I* | Construcción sin manual de una pala fija o parachoques pasivo para empujar bloques entre zonas delimitadas. | **Módulos Mecánicos & Paralelogramos:** Ensambles libres sin manual, mecanismos de paralelogramo deformable (4-bar linkage) y trenes de engranajes para optimizar espacio. | Cajas de engranajes compuestas y mecanismos de cremallera. Optimización de esfuerzo mecánico en motores medianos. |
| **Semana 3 - J3**<br>*Actuadores & Auto-Cero* | Incorporación de un tercer motor para accionar una pinza de 1 grado de libertad (apertura y cierre por rotaciones). | **Actuadores & Parada por Bloqueo:** Diseño de pinzas y cremalleras; cálculo de torque y parada automática por sobreesfuerzo (*stalled condition*) contrastando bloques frente a `run_until_stalled()` en Python. | Sistema modular de acople y desacople rápido (*quick-release*) para intercambiar herramientas en base sin tornillería. |
| **Semana 4 - M4**<br>*Modularidad e Integración* | Desafío integrado: salida de base, detección de objeto por color, transporte a zona segura y retroceso al inicio. | **Modularidad en Bloques vs Funciones Python:** Creación de subprogramas reutilizables en Bloques (*MyBlocks*) frente a la definición de funciones modulares (def) en Python para una rutina completa. | Máquina de estados: seguidor de línea proporcional suave, toma de decisión de clasificación y retorno autónomo contrarreloj. |
| **Semana 4 - J4**<br>*Reto Diagnóstico & Defensa* | "Mini-Rally de Habilidades": resolución en parejas de una pista sorpresa, evaluando colaboración y perseverancia. | **Reto de Innovación y Defensa Técnica:** Ensamble creativo contrarreloj de un mecanismo adaptativo y justificación técnica ante el jurado comparando la lógica de bloques frente al código Python. | Prueba ciega: alteración de la posición de un elemento en el tapete para reconfigurar código y mecánica en menos de 15 minutos. |

---

## 3. Temporada WRO 2027 (Enero a Julio)

`
Ene: Estrategia  ──► Feb: Diseño  ──► Mar: Base y Chasis  ──► Abr: Estrés  ──► May: Rutina  ──► Jun/Jul: Torneo
`

---

### Fase 1: Ideas de Rutina y Estrategia (Enero)
* **Objetivo:** Desglosar el reglamento oficial de la temporada, evaluar riesgos y trazar la ruta de mayor rendimiento por segundo.
* **Proceso de equipo:**
  1. Análisis exhaustivo del reglamento oficial, tapete, zonas de penalización y sistema de puntuación.
  2. Lluvia de ideas y separación de misiones según su viabilidad técnica.
  3. Debate interno para seleccionar la "Ruta Principal" (máximo puntaje) y la "Ruta de Contingencia" (asegurar puntos base).
* **Adaptación por niveles:**
  * **Elementary:** Enfoque en asegurar entre el 40% y 50% del puntaje total con tareas directas de empuje o transporte cercano a la base.
  * **Junior:** Matriz de costo-beneficio (puntos obtenidos / segundos invertidos); rutas combinadas que ejecuten dos acciones por trayecto.
  * **Senior:** Diagrama de flujo dinámico capaz de adaptarse a las variables aleatorias del tapete; ruta planificada para barrido del 100% en menos de 120 s.

---

### Fase 2: Diseño Conceptual y Prototipado (Febrero)
* **Objetivo:** Construir los mecanismos de manipulación y validar que el conjunto respete las dimensiones reglamentarias.
* **Proceso de equipo:**
  1. Verificación del límite de tamaño inicial ( \times 25 \times 25\text{ cm}$) con plantillas o cajas de calibración.
  2. Prototipado rápido de actuadores: garras, brazos de cuatro barras articuladas, tolvas basculantes o empujadores pasivos.
  3. Selección de neumáticos y distancia entre ejes para optimizar el radio de giro.
* **Adaptación por niveles:**
  * **Elementary:** Mecanismos pasivos y guías anguladas en el chasis para encauzar objetos hacia la base sin necesidad de motores adicionales.
  * **Junior:** Brazos de paralelogramo deformable que mantengan la orientación de las piezas en el aire durante la elevación.
  * **Senior:** Estructura en capas: chasis motriz ultracompacto con centro de gravedad bajo y aditamentos modulares accionados por levas o desvíos mecánicos.

---

### Fase 3: Armado Estructural y Programación Base (Marzo)
* **Objetivo:** Ensamblar el chasis definitivo y desarrollar la librería de subrutinas de movilidad confiables.
* **Proceso de equipo:**
  1. Refuerzo de la estructura motriz con vigas cruzadas para evitar torsiones mecánicas repetitivas.
  2. Instalación de dos sensores de color frontales apantallados contra la luz ambiental, fijados a \text{ - }10\text{ mm}$ del tapete.
  3. Programación y parametrización de bloques de movimiento reutilizables (*MyBlocks* o funciones de Python).
* **Adaptación por niveles:**
  * **Elementary:** Creación de bloques parametrizados simples: Avanzar_cm(distancia), Girar_90_Grados() y Soltar_Pieza().
  * **Junior:** Rutinas de autoalineación contra paredes (*bumping*) y contra líneas perpendiculares para reiniciar el error acumulado de odometría.
  * **Senior:** Algoritmos de control Proporcional-Derivativo ($) para seguimiento de línea y avance guiado por giroscopio; arquitectura de código modular en Python o bloques avanzados.

---

### Fase 4: Pruebas de Estrés y Variabilidad de Entorno (Abril)
* **Objetivo:** Someter el robot a perturbaciones reales para garantizar que la rutina no dependa de condiciones ideales de laboratorio.
* **Proceso de equipo:**
  1. **Pruebas de luz:** Operación del robot bajo reflectores directos, sombras del público y variaciones de luz natural.
  2. **Pruebas de superficie:** Corridas en tapetes con pliegues, mesas descalibradas y piezas de juego desgastadas o deformadas.
  3. **Pruebas de batería:** Mapeo del comportamiento de marcha con batería al 100%, 75% y 50% de carga.
* **Adaptación por niveles:**
  * **Elementary:** Refuerzo mecánico de pasadores flojos; entrenamiento de posicionamiento manual exacto en la base de salida.
  * **Junior:** Calibración dinámica: comprobación de umbrales de reflectancia al inicio de cada intento para ajustar las variables de detección.
  * **Senior:** Simulación de errores estocásticos: arrancar el robot con un desvío voluntario de $\pm 3^\circ$ y verificar si los algoritmos corrigen la trayectoria por sensores.

---

### Fase 5: Programación de la Rutina Completa (Mayo)
* **Objetivo:** Integrar la movilidad base con las misiones específicas en una secuencia unificada y fluida.
* **Proceso de equipo:**
  1. Integración secuencial: añadir una misión al código general solo cuando la anterior consiga al menos 5 ejecuciones exitosas consecutivas.
  2. Coordinación de tiempos: sincronizar la detención motriz con la activación de los accesorios de carga.
  3. Establecimiento de protocolos de aborto de misión para evitar atascos que consuman el tiempo total de la ronda.
* **Adaptación por niveles:**
  * **Elementary:** Secuencia lineal respaldada con indicadores gráficos en la pantalla LED del Hub para saber en qué etapa del código se encuentra el robot.
  * **Junior:** Puntos de control (*checkpoints*): si un sensor falla en detectar una pieza, el robot abandona ese intento y se traslada a la siguiente misión sin detener el cronómetro.
  * **Senior:** Lógica condicional compleja para resolver misiones dependientes de la disposición aleatoria inicial; optimización de curvas directas en lugar de giros en el lugar.

---

### Fase 6: Simulacros de Torneo y Calibración Final (Junio - Julio)
* **Objetivo:** Entrenar el rendimiento psicológico y operativo del equipo bajo las condiciones formales de la competencia.
* **Proceso de equipo:**
  1. Cronometraje oficial de 2 minutos por intento, registrando puntajes y penalizaciones en hojas de evaluación estándar.
  2. Protocolo de mantenimiento en boxes (*Pit Stop*): limpieza de neumáticos, ajuste de ejes y rotación de baterías.
  3. Ensayos del tiempo de ensamblaje (si la categoría exige montaje en zona de cuarentena).
* **Adaptación por niveles:**
  * **Elementary:** Asignación clara de roles de salida: un estudiante alinea el robot, otro selecciona el programa y el tercero confirma al juez el inicio. Manejo de la frustración ante fallos en tapete.
  * **Junior:** Pruebas con árbitros invitados ajenos al club para habituarse al rigor reglamentario; bitácora de incidencias mecánicas por ronda.
  * **Senior:** Entrenamiento específico para la "Regla Sorpresa" (*Surprise Rule*): resolución de una modificación de reglamento en 60 a 90 minutos de cuarentena estricta. Registro estadístico con un mínimo de 30 corridas completas antes de viajar.
