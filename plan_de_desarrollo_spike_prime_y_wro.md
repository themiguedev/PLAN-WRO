# Plan de Desarrollo TÃ©cnico y Competitivo: LEGO SPIKE Prime
**Enfoque:** RobÃ³tica Educativa y World Robot Olympiad (RoboMission)  
**Niveles:** Elementary (8 - 12 aÃ±os) | Junior (11 - 15 aÃ±os) | Senior (14 - 19 aÃ±os)  

---

## 1. Marco General de Fases de EvoluciÃ³n

El progreso tÃ©cnico de los estudiantes se estructura en cuatro fases continuas:

```
[ Fase 1: AlfabetizaciÃ³n ] â”€â”€â–º [ Fase 2: Adaptabilidad ] â”€â”€â–º [ Fase 3: IngenierÃ­a WRO ] â”€â”€â–º [ Fase 4: OptimizaciÃ³n ]
  MecÃ¡nica y algoritmos           Sensores y lÃ³gica libre        CinemÃ¡tica y robustez         Estrategia y torneo
```

* **Fase 1: AlfabetizaciÃ³n MecÃ¡nica y AlgorÃ­tmica (ConstrucciÃ³n Guiada y Bloques Base):** ComprensiÃ³n de vigas, pasadores, ejes, simetrÃ­a estructural, lectura de instrucciones, engranajes elementales y programaciÃ³n secuencial/condicional bÃ¡sica.
* **Fase 2: Adaptabilidad Creativa e IntegraciÃ³n Sensorial:** ModificaciÃ³n libre de modelos existentes, incorporaciÃ³n de sensores (color, distancia, giroscopio), bucles de repeticiÃ³n y resoluciÃ³n de obstÃ¡culos sin guÃ­a.
* **Fase 3: IngenierÃ­a Competitiva y CinemÃ¡tica WRO:** DiseÃ±o de chasis compactos dentro del cubo de $25 \times 25 \times 25\text{ cm}$, cÃ¡lculo de relaciones de transmisiÃ³n, odometrÃ­a, movimiento con control giroscÃ³pico y seguimiento de lÃ­neas.
* **Fase 4: EjecuciÃ³n EstratÃ©gica y CalibraciÃ³n:** Rutinas completas de tapete, protocolos contra fallos mecÃ¡nicos, tolerancia a variaciones lumÃ­nicas, optimizaciÃ³n temporal (lÃ­mite de 2 minutos) y manejo de rondas sorpresa.

---

## 2. Plan Mensual de Nivelación: Noviembre
* **RÃ©gimen:** 8 sesiones al mes (Martes y Jueves).
* **Objetivo:** Nivelar fundamentos mecÃ¡nicos, control motriz y lÃ³gica de programaciÃ³n antes de la temporada competitiva.

| SesiÃ³n | Nivel Elementary (8 - 12 aÃ±os) | Nivel Junior (11 - 15 aÃ±os) | Nivel Senior (14 - 19 aÃ±os) |
| :--- | :--- | :--- | :--- |
| **Semana 1 - M1**<br>*Chasis y TracciÃ³n* | Ensamble guiado del chasis base estÃ¡ndar. Reconocimiento de piezas clave y simetrÃ­a. Movimiento rectilÃ­neo por rotaciones y grados. | ConstrucciÃ³n de chasis rÃ­gido con centro de gravedad bajo. CÃ¡lculo de avance lineal ($cm$ por rotaciÃ³n en base al diÃ¡metro de rueda). | CinemÃ¡tica diferencial, cÃ¡lculo de momento de inercia y diseÃ±o de chasis para aceleraciÃ³n estable sin derrape de neumÃ¡ticos. |
| **Semana 1 - J1**<br>*PrecisiÃ³n y Giros* | Giros en un punto (pivote) vs. giros suaves (diferencial). Trazado de trayectorias cuadradas simples con cinta adhesiva. | Giros de 90Â° calibrados mediante el sensor giroscÃ³pico integrado (`Yaw angle`). CorrecciÃ³n de inercia y uso de freno activo (`hold`). | ImplementaciÃ³n de control proporcional ($P$) en giros giroscÃ³picos para eliminar subgiros y sobregiros por inercia residual. |
| **Semana 2 - M2**<br>*Sensores de Color* | DetecciÃ³n de colores sÃ³lidos (semÃ¡foro: rojo = parada, verde = avance). Parada inmediata sobre cinta negra. | Lectura de porcentaje de luz reflejada. CalibraciÃ³n bÃ¡sica de umbral blanco/negro mediante la fÃ³rmula: $\frac{L_{blanco} + L_{negro}}{2}$. | Sistema de doble sensor frontal para autoalineaciÃ³n en lÃ­neas perpendiculares (*line squaring*) e interpolaciÃ³n continua de lecturas. |
| **Semana 2 - J2**<br>*Sensores de Distancia* | Sensor ultrasÃ³nico: detecciÃ³n de barreras fijas y frenado automÃ¡tico a $10\text{ cm}$ de distancia sin colisiÃ³n. | EvasiÃ³n activa: desaceleraciÃ³n proporcional segÃºn proximidad y desvÃ­os laterales en bucle condicional continuo. | Mapeo de zonas ocupadas mediante lecturas de distancia en movimiento, guardando el estado en variables lÃ³gicas/booleanas. |
| **Semana 3 - M3**<br>*MecÃ¡nica de Carga* | ConstrucciÃ³n sin manual de una pala fija o parachoques pasivo para empujar bloques entre zonas delimitadas. | Trenes de engranajes: anÃ¡lisis experimental de torque frente a velocidad angular. SelecciÃ³n de relaciÃ³n para brazos mecÃ¡nicos. | Cajas de engranajes compuestas y mecanismos de cremallera. OptimizaciÃ³n de esfuerzo mecÃ¡nico en motores medianos. |
| **Semana 3 - J3**<br>*Actuadores Activos* | IncorporaciÃ³n de un tercer motor para accionar una pinza de 1 grado de libertad (apertura y cierre por rotaciones). | Garra articulada con retorno a cero automÃ¡tico aprovechando la detecciÃ³n de bloqueo del motor (*stalled condition*). | Sistema modular de acople y desacople rÃ¡pido (*quick-release*) para intercambiar herramientas en base sin tornillerÃ­a. |
| **Semana 4 - M4**<br>*IntegraciÃ³n LÃ³gica* | DesafÃ­o integrado: salida de base, detecciÃ³n de objeto por color, transporte a zona segura y retroceso al inicio. | Subrutina completa: seguimiento de lÃ­nea bÃ¡sico (2 estados), detecciÃ³n de marca en tapete, sujeciÃ³n y depÃ³sito. | MÃ¡quina de estados: seguidor de lÃ­nea proporcional suave, toma de decisiÃ³n de clasificaciÃ³n y retorno autÃ³nomo contrarreloj. |
| **Semana 4 - J4**<br>*Reto DiagnÃ³stico* | "Mini-Rally de Habilidades": resoluciÃ³n en parejas de una pista sorpresa, evaluando colaboraciÃ³n y perseverancia. | PresentaciÃ³n y defensa tÃ©cnica: ejecuciÃ³n de misiÃ³n completa explicando la estructura de los subprogramas (*MyBlocks*). | Prueba ciega: alteraciÃ³n de la posiciÃ³n de un elemento en el tapete para reconfigurar cÃ³digo y mecÃ¡nica en menos de 15 minutos. |

---


---

## 3. Plan Mensual de Especialización y Pre-Temporada: Noviembre
* **Régimen:** 8 sesiones al mes (Martes y Jueves).
* **Objetivo:** Dominio de odometría fina, transición a Python (Senior), control Proporcional/Derivativo de línea, multiplexación de puertos y simulacro en la Copa Pre-WRO de Club.

| Sesión | Nivel Elementary (8 - 12 años) | Nivel Junior (11 - 15 años) | Nivel Senior (14 - 19 años) |
| :--- | :--- | :--- | :--- |
| **Semana 1 - M1**<br>*Odometría y Calibración Fina* | Medición de trayectorias con cinta métrica y cálculo de compensación por arrastre de neumáticos en superficie vinílica. | Odometría con encoders internos de motor; estimación de error angular acumulado en secuencias de traslación combinada. | Introducción y estructuración modular en **MicroPython oficial de SPIKE Prime**: clases para tracción diferencial y lectura continua del sensor inercial. |
| **Semana 1 - J1**<br>*Subprogramas y Parámetros* | Creación de *MyBlocks* con parámetros de entrada (distancia_cm, elocidad) para evitar código repetitivo en cascada. | Uso de variables globales y matrices unidimensionales para registrar el orden de recogida de bloques en pista. | Funciones en Python con retorno de valores booleanos para comprobación asíncrona de fin de trayectoria y detección de colisión. |
| **Semana 2 - M2**<br>*Seguimiento de Línea Proporcional* | Seguidor de dos sensores con ajuste diferenciado de potencia para trazado suave de curvas cerradas sin desenganche. | Algoritmo de seguidor proporcional (P): cálculo de error = luz - setpoint, ajuste continuo de steering con ganancia Kp. | Controlador Proporcional-Derivativo (PD) en Python: amortiguación de oscilaciones parásitas a alta velocidad y filtrado de ruido. |
| **Semana 2 - J2**<br>*Navegación de Intersecciones* | Detección confiable de líneas transversales de cruce en 'T' y parada con doble sensor frontal simultáneo. | Algoritmo de conteo de intersecciones para localización relativa sin depender exclusivamente de rotaciones de motor. | Cruce de intersecciones ciegas y maniobra de recuperación autónoma si el robot pierde la línea de guía por inercia excesiva. |
| **Semana 3 - M3**<br>*Mecanismos Quick-Release* | Diseño de guías y pestillos de encastre deslizante sin pasadores para recambio de palas en menos de 5 segundos. | Multiplexación mecánica: acople de trinquete para que un motor ejecute dos tareas distintas según el sentido de rotación (horario / antihorario). | Sistemas modulares con autoalineación cinemática y compensación de holguras para no superar el límite de 6 puertos del Hub. |
| **Semana 3 - J3**<br>*Gestión de Energía y Masa* | Balance de peso sobre el eje motriz para evitar descompensación de tracción al transportar piezas pesadas. | Rutinas de testeo y mapeo de degradación de velocidad angular según caída de voltaje de la batería en tandas de 10 minutos. | Optimización de curvas de aceleración y deceleración polinomial en Python para prevenir derrapes con el robot a plena carga. |
| **Semana 4 - M4**<br>*Copa Pre-WRO: Rondas Clasificatorias* | Reto cronometrado de 3 misiones combinadas en tapete escolar, registro de tiempos y evaluación de espíritu de equipo. | Mini-torneo con cambio sorpresa de zonas de depósito a mitad de la sesión para entrenar la flexibilidad del algoritmo. | Simulación estricta con pesaje en cubo de 25x25x25 cm, cronometraje reglamentario de 120s y 3 intentos oficiales en boxes. |
| **Semana 4 - J4**<br>*Auditoría y Bitácora Técnica* | Revisión de estado de piezas, desmontaje selectivo, orden de gavetas y presentación oral de aprendizajes. | Evaluación y defensa de la bitácora técnica de ingeniería: bocetos, registro de fallos mecánicos y justificación de engranajes. | Defensa técnica ante jurado de mentores: análisis del código en Python, plan de contingencia ante fallos y selección de alineaciones oficiales. |

## 4. Macro-Ciclo Competitivo WRO (Enero a Julio)

```
Ene: Estrategia  â”€â”€â–º Feb: DiseÃ±o  â”€â”€â–º Mar: Base y Chasis  â”€â”€â–º Abr: EstrÃ©s  â”€â”€â–º May: Rutina  â”€â”€â–º Jun/Jul: Torneo
```

---

### Fase 1: Ideas de Rutina y Estrategia (Enero)
* **Objetivo:** Desglosar el reglamento oficial de la temporada, evaluar riesgos y trazar la ruta de mayor rendimiento por segundo.
* **Proceso de equipo:**
  1. AnÃ¡lisis exhaustivo del reglamento oficial, tapete, zonas de penalizaciÃ³n y sistema de puntuaciÃ³n.
  2. Lluvia de ideas y separaciÃ³n de misiones segÃºn su viabilidad tÃ©cnica.
  3. Debate interno para seleccionar la "Ruta Principal" (mÃ¡ximo puntaje) y la "Ruta de Contingencia" (asegurar puntos base).
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** Enfoque en asegurar entre el 40% y 50% del puntaje total con tareas directas de empuje o transporte cercano a la base.
  * **Junior:** Matriz de costo-beneficio (puntos obtenidos / segundos invertidos); rutas combinadas que ejecuten dos acciones por trayecto.
  * **Senior:** Diagrama de flujo dinÃ¡mico capaz de adaptarse a las variables aleatorias del tapete; ruta planificada para barrido del 100% en menos de 120 s.

---

### Fase 2: DiseÃ±o Conceptual y Prototipado (Febrero)
* **Objetivo:** Construir los mecanismos de manipulaciÃ³n y validar que el conjunto respete las dimensiones reglamentarias.
* **Proceso de equipo:**
  1. VerificaciÃ³n del lÃ­mite de tamaÃ±o inicial ($25 \times 25 \times 25\text{ cm}$) con plantillas o cajas de calibraciÃ³n.
  2. Prototipado rÃ¡pido de actuadores: garras, brazos de cuatro barras articuladas, tolvas basculantes o empujadores pasivos.
  3. SelecciÃ³n de neumÃ¡ticos y distancia entre ejes para optimizar el radio de giro.
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** Mecanismos pasivos y guÃ­as anguladas en el chasis para encauzar objetos hacia la base sin necesidad de motores adicionales.
  * **Junior:** Brazos de paralelogramo deformable que mantengan la orientaciÃ³n de las piezas en el aire durante la elevaciÃ³n.
  * **Senior:** Estructura en capas: chasis motriz ultracompacto con centro de gravedad bajo y aditamentos modulares accionados por levas o desvÃ­os mecÃ¡nicos.

---

### Fase 3: Armado Estructural y ProgramaciÃ³n Base (Marzo)
* **Objetivo:** Ensamblar el chasis definitivo y desarrollar la librerÃ­a de subrutinas de movilidad confiables.
* **Proceso de equipo:**
  1. Refuerzo de la estructura motriz con vigas cruzadas para evitar torsiones mecÃ¡nicas repetitivas.
  2. InstalaciÃ³n de dos sensores de color frontales apantallados contra la luz ambiental, fijados a $8\text{ - }10\text{ mm}$ del tapete.
  3. ProgramaciÃ³n y parametrizaciÃ³n de bloques de movimiento reutilizables (*MyBlocks* o funciones de Python).
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** CreaciÃ³n de bloques parametrizados simples: `Avanzar_cm(distancia)`, `Girar_90_Grados()` y `Soltar_Pieza()`.
  * **Junior:** Rutinas de autoalineaciÃ³n contra paredes (*bumping*) y contra lÃ­neas perpendiculares para reiniciar el error acumulado de odometrÃ­a.
  * **Senior:** Algoritmos de control Proporcional-Derivativo ($PD$) para seguimiento de lÃ­nea y avance guiado por giroscopio; arquitectura de cÃ³digo modular en Python o bloques avanzados.

---

### Fase 4: Pruebas de EstrÃ©s y Variabilidad de Entorno (Abril)
* **Objetivo:** Someter el robot a perturbaciones reales para garantizar que la rutina no dependa de condiciones ideales de laboratorio.
* **Proceso de equipo:**
  1. **Pruebas de luz:** OperaciÃ³n del robot bajo reflectores directos, sombras del pÃºblico y variaciones de luz natural.
  2. **Pruebas de superficie:** Corridas en tapetes con pliegues, mesas descalibradas y piezas de juego desgastadas o deformadas.
  3. **Pruebas de baterÃ­a:** Mapeo del comportamiento de marcha con baterÃ­a al 100%, 75% y 50% de carga.
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** Refuerzo mecÃ¡nico de pasadores flojos; entrenamiento de posicionamiento manual exacto en la base de salida.
  * **Junior:** CalibraciÃ³n dinÃ¡mica: comprobaciÃ³n de umbrales de reflectancia al inicio de cada intento para ajustar las variables de detecciÃ³n.
  * **Senior:** SimulaciÃ³n de errores estocÃ¡sticos: arrancar el robot con un desvÃ­o voluntario de $\pm 3^\circ$ y verificar si los algoritmos corrigen la trayectoria por sensores.

---

### Fase 5: ProgramaciÃ³n de la Rutina Completa (Mayo)
* **Objetivo:** Integrar la movilidad base con las misiones especÃ­ficas en una secuencia unificada y fluida.
* **Proceso de equipo:**
  1. IntegraciÃ³n secuencial: aÃ±adir una misiÃ³n al cÃ³digo general solo cuando la anterior consiga al menos 5 ejecuciones exitosas consecutivas.
  2. CoordinaciÃ³n de tiempos: sincronizar la detenciÃ³n motriz con la activaciÃ³n de los accesorios de carga.
  3. Establecimiento de protocolos de aborto de misiÃ³n para evitar atascos que consuman el tiempo total de la ronda.
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** Secuencia lineal respaldada con indicadores grÃ¡ficos en la pantalla LED del Hub para saber en quÃ© etapa del cÃ³digo se encuentra el robot.
  * **Junior:** Puntos de control (*checkpoints*): si un sensor falla en detectar una pieza, el robot abandona ese intento y se traslada a la siguiente misiÃ³n sin detener el cronÃ³metro.
  * **Senior:** LÃ³gica condicional compleja para resolver misiones dependientes de la disposiciÃ³n aleatoria inicial; optimizaciÃ³n de curvas directas en lugar de giros en el lugar.

---

### Fase 6: Simulacros de Torneo y CalibraciÃ³n Final (Junio - Julio)
* **Objetivo:** Entrenar el rendimiento psicolÃ³gico y operativo del equipo bajo las condiciones formales de la competencia.
* **Proceso de equipo:**
  1. Cronometraje oficial de 2 minutos por intento, registrando puntajes y penalizaciones en hojas de evaluaciÃ³n estÃ¡ndar.
  2. Protocolo de mantenimiento en boxes (*Pit Stop*): limpieza de neumÃ¡ticos con toallitas de alcohol isopropÃ­lico, ajuste de ejes y rotaciÃ³n de baterÃ­as.
  3. Ensayos del tiempo de ensamblaje (si la categorÃ­a exige montaje en zona de cuarentena).
* **AdaptaciÃ³n por niveles:**
  * **Elementary:** AsignaciÃ³n clara de roles de salida: un estudiante alinea el robot, otro selecciona el programa y el tercero confirma al juez el inicio. Manejo de la frustraciÃ³n ante fallos en tapete.
  * **Junior:** Pruebas con Ã¡rbitros invitados ajenos al club para habituarse al rigor reglamentario; bitÃ¡cora de incidencias mecÃ¡nicas por ronda.
  * **Senior:** Entrenamiento especÃ­fico para la "Regla Sorpresa" (*Surprise Rule*): resoluciÃ³n de una modificaciÃ³n de reglamento en 60 a 90 minutos de cuarentena estricta. Registro estadÃ­stico con un mÃ­nimo de 30 corridas completas antes de viajar.