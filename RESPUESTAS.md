# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID:** 3.a..e
> **Unidad / Tema:**  Unidad 3
> **Alumno/a:**  Nerea Candón Ramos
> **Fecha:**  30/04/2026

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.


### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
La verdad es que esta unidad me ha parecido bastante interesante porque no se centra solo en detectar un ataque, sino en todo el proceso completo: cómo recoger evidencias, analizarlas y actuar sin cometer errores.

Me ha gustado porque te hace darte cuenta de que no vale con reaccionar rápido, sino que hay que hacerlo bien y con orden, ya que una mala decisión puede hacer que pierdas información importante.


### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
Lo más útil para mí ha sido aprender a analizar un incidente y saber explicarlo bien en un informe. Al final, en un trabajo real no solo tienes que entender lo que ha pasado, sino saber comunicarlo de forma clara.

También me parece importante saber detectar las fases de un ataque, porque eso ayuda a reaccionar antes y a evitar que el problema vaya a más.


### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
Ya había visto cosas como la recopilación de evidencias y la importancia de no modificarlas, pero en esta unidad lo he entendido mejor y más aplicado.

Lo nuevo para mí ha sido usar herramientas y métodos como la matriz de MITRE ATT&CK, que ayuda a organizar mejor los ataques y entenderlos paso a paso. También la parte de cómo contener un incidente de forma más estratégica.


### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
Lo que más me ha llamado la atención ha sido la matriz de MITRE ATT&CK, porque me parece una forma muy clara de entender cómo actúa un atacante.

Antes veía los ataques como algo más desordenado, pero esto te ayuda a seguir un patrón y entender mejor todo lo que está pasando.


### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
No recortaría ninguna parte, ya que todos los conceptos están conectados entre sí y forman parte del proceso completo de gestión de incidentes. Reducir contenido dificultaría la comprensión global.


### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
Me hubiera gustado hacer algun taller o alguna actividad en clase que todos hubieramos participado para hacer un caso real e intentar resolverlo, recrear como sería y analizarlo.


### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
Aplicaría sobre todo el orden: primero aislar el sistema afectado, luego recoger evidencias sin tocarlas demasiado y documentar todo lo que haga.

Aunque no tengas muchas herramientas, seguir un proceso claro ya marca bastante la diferencia.


### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
La cadena de custodia me parece una forma fácil de invalidar una prueba de manera legal solo por cometer un error al manipular la evidencia y no seguir el protocolo y me queda en duda si un juez aceptaría una evidencia si no tenemos herramientas forenses profesionales para certificarlas


## 2) Resumen esquematizado (obligatorio)


| SECCIÓN                       | CONCEPTO PRINCIPAL     | DETALLES CLAVE                                                                                                        | EJEMPLOS/FLUJOS                                                                           |
| ----------------------------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 3.1.1 Recopilación Evidencias | RFC 3227               | Pilares: Personas/Procedimientos/HerramientasPrincipios: Recolección>análisis, minimizar cambios                      | Orden Volatilidad:1. RAM/ARP2. Procesos/memoria3. Disco4. Logs5. RedEvitar: Apagar equipo |
|                               | Cadena Custodia        | Quién/Cuándo/Dónde/Cómo                                                                                               | Herramientas: Volatility, Wireshark, dd                                                   |
| 3.1.2 Procedimiento           | 4 Fases                | 1. Preparación (kit forense)2. Escena (aislar/documentar)3. Almacenamiento (cifrado/acceso restringido)4. Disposición | Write-blockers, hashes MD5/SHA256                                                         |
| 3.3.1 MITRE                   | ATT&CK                 | Táctica(para qué)→Técnica(cómo)→Sub-técnica                                                                           | Navigator: capas técnicas observadas                                                      |
|                               | RE&CT                  | Respuesta/DFIR fases                                                                                                  | Navigator: cobertura respuesta                                                            |
|                               | Complementarios        | ATT&CK=ataque / RE&CT=respuesta                                                                                       | Uso conjunto en incidentes                                                                |
| 3.3.2 Investigación           | Tipos Análisis         | Detección→Preliminar→Causa raíz→Intrusión→Atribución                                                                  | IOC: Atómicos/Computacionales/Comportamiento                                              |
|                               | Metodología 10 Fases   | 1.Identif.→2.Recopil.→3.Análisis→4.Correl.Prelim.→5.Normaliz.→6.Desconflic.→7.Línea temp.→8.Marcos→9.Informe          | Hipótesis→Evidencia→Conclusión                                                            |
|                               | Cyber Kill Chain       | 1.Reconocimiento→2.Armamentiz.→3.Entrega→4.Explotación→5.Instalación→6.C2→7.Acciones                                  | Phishing: 3.Entrega(correo)→5.Instalación(payload)                                        |
|                               | Modelo Diamante        | Adversario/Capacidad/Infraestructura/Víctima                                                                          | Phishing: Capacidad(enlace)/Infra(dominio)/Víctima(usuario)                               |
| 3.5.1 Contención              | Objetivos              | Frenar daño/superficie/tiempo/proteger críticos/preservar evidencia                                                   | Daño activo→Aislar YA                                                                     |
|                               | Táctica vs Estratégica | Táctica(min-h): Aislar/bloquearEstratégica(días): Hardening/segmentación                                              | Reset credenciales(táctica)/MFA(estratégica)                                              |
|                               | Por Capas              | Red: ACL egressID: Revocar tokensEndpoint: EDR cuarentenaServicios: WAF temporal                                      | Ransomware: Aislar→Proteger backups                                                       |
|                               | Flujo Decisión         | Daño activo?→Capt.volátil→Táctica→ID comprometida?→Capas→Validar                                                      | Checklist: Evidencia→Aislar→ID→IoC→Backups                                                |
|                               | Errores                | Formatear sin investigarNo cortar IDAislar solo 1 equipo                                                              | Playbooks: Ransomware/Phishing/Web/C2                                                     |


### 2.1) Mapa/índice de la unidad (visión global)

# Gestión de Incidentes
Recopilar → Investigar → Contener → Erradicar → Recuperar

## Recopilación
### Recopilación de evidencias
- Evidencias digitales  
- RFC 3227  
- Orden de volatilidad  
- Cadena de custodia  

### Procedimiento
- 4 fases  
- Uso de herramientas (kits, write-blockers)  
- Cadena de custodia  

## Investigación
### MITRE
- MITRE ATT&CK  
- RE&CT  

### Investigación avanzada
- 10 fases  
- Cyber Kill Chain  
- Modelo Diamante  

## Contención
### Contención del incidente
- Táctica vs estratégica  
- Capas:
  - Identidad  
  - Red  
  - Endpoint  
  - Servicios  
- Flujo:
  - Evaluar daño  
  - Analizar volatilidad  
  - Identificar  
  - Aplicar por capas  
  - Validar  
- Checklist:
  - Preservar evidencias  
  - Aislar sistemas  
  - Realizar backups  


### 2.2) Conceptos clave (lista breve)

**Recopilación evidencias**

- Gestión incidentes: Proceso estructurado respuesta seguridad

- Evidencia digital: Datos para analizar incidente (logs/imágenes)

- RFC 3227: Guía recogida/archivado evidencias

- Orden volatilidad: Prioridad captura: RAM→Procesos→Disco→Red

- Cadena custodia: Quién/cuándo/dónde/cómo manipuló evidencia

**Investigación**

- MITRE ATT&CK: Tácticas/técnicas/subtécnicas atacantes

- RE&CT: Marco respuesta incidentes (DFIR)

- Cyber Kill Chain: 7 fases ataque (Reconocimiento→Acciones)

- Modelo Diamante: Adversario/Capacidad/Infraestructura/Víctima

**Contención**

- Contención: Limitar impacto incidente

- Contención táctica: Respuesta inmediata (minutos)

- Contención estratégica: Medidas largo plazo (días)

- Capas seguridad: Identidad→Red→Endpoint→Servicios

- Erradicación: Eliminar amenaza raíz

- Recuperación: Restaurar servicios normalidad


### 2.3) Procesos / procedimientos (pasos o checklist)

## 1. Detección
- [ ] Identificar que existe un incidente

## 2. Recopilación de evidencias
- [ ] Aplicar RFC 3227 (recoger antes de analizar)
- [ ] Evitar modificar el sistema
- [ ] Capturar por orden de volatilidad:
  - RAM
  - Procesos
  - Disco
  - Red / logs
- [ ] Usar write-blocker si hay discos
- [ ] Registrar cadena de custodia (quién/cuándo/dónde/cómo)

## 3. Investigación
- [ ] Definir hipótesis inicial
- [ ] Recoger evidencias relevantes
- [ ] Analizar información
- [ ] Correlacionar eventos
- [ ] Construir línea temporal
- [ ] Usar modelos (MITRE / Kill Chain / Diamante)
- [ ] Confirmar causa raíz

## 4. Contención
- [ ] Comprobar si el ataque sigue activo
- [ ] Actuar por orden de prioridad:
  - Identidad
  - Red
  - Endpoint
  - Servicios
- [ ] Elegir tipo de contención:
  - Táctica (inmediata)
  - Estratégica (largo plazo)
- [ ] Verificar que el ataque se detuvo

## 5. Erradicación
- [ ] Eliminar la amenaza del sistema
- [ ] Eliminar persistencias

## 6. Recuperación
- [ ] Restaurar sistemas y servicios
- [ ] Validar funcionamiento normal

## 7. Cierre
- [ ] Documentar todo el incidente
- [ ] Guardar evidencias correctamente


### 2.4) Herramientas / técnicas (si aplica)

- FTK Imager: herramienta para crear imágenes forenses de discos y analizar evidencias.
- Volatility: herramienta para análisis forense de memoria RAM.
- Wireshark: analizador de tráfico de red en tiempo real o capturas.
- tcpdump: herramienta de captura de paquetes en línea de comandos.
- Autopsy: software de análisis forense de discos.
- MITRE ATT&CK: base de conocimiento de técnicas y tácticas de ataques.
- RE&CT: framework de respuesta a incidentes basado en DFIR.
- MISP: sistema de intercambio de inteligencia de amenazas.
- SIEM: sistema de correlación y análisis de logs de seguridad.
- Firewall: sistema que controla y filtra el tráfico de red.
- EDR: herramienta de detección y respuesta en endpoints.
- Antivirus / EPP: software para detección y eliminación de malware.

### 2.5) Buenas prácticas y errores típicos

## Buenas prácticas
- Preservar evidencias desde el primer momento
- Aplicar orden de volatilidad correctamente
- Mantener cadena de custodia completa
- Usar herramientas forenses adecuadas
- Documentar cada acción realizada
- Aislar sistemas sin destruir evidencia
- Verificar integridad de las evidencias
- Trabajar siempre de forma reproducible


## Errores típicos
- Formatear el sistema antes de investigar
- No recoger RAM o evidencias volátiles
- Modificar evidencias sin querer
- Romper la cadena de custodia
- No documentar el proceso
- Aislar sistemas sin analizar impacto
- Saltarse el orden de volatilidad
- No validar la causa raíz del incidente


### 2.6) Glosario mínimo (términos y definiciones cortas)

- Incidente: evento de seguridad que afecta sistemas o datos.
- Evidencia digital: información usada para analizar un incidente.
- Logs: registros de actividad en sistemas o redes- Volatilidad: orden en el que se pierden los datos.
- RAM: memoria volátil del sistema- Cadena de custodia: control de quién manipula la evidencia.
- Write-blocker: dispositivo que evita modificar discos.
- RFC 3227: guía para recolección de evidencias digitales.
- MITRE ATT&CK: base de conocimiento de técnicas de ataque
- Kill Chain: fases de un ataque cibernético.
- Diamante: modelo de análisis de ciberataques.
- DFIR: respuesta y análisis forense de incidentes.
- Contención: acción para limitar el daño del incidente.
- Erradicación: eliminación de la amenaza.
- Recuperación: restauración de sistemas a la normalidad.



## 3) (Opcional) Evidencias y recursos usados
Enlaza aquí evidencias (capturas, logs, configuraciones, salidas de comandos, etc.) si forman parte de tu trabajo.

### Evidencia 1
- Archivo: ![Evidencia 1](evidencias/siem.png)
- Qué demuestra: Esta evidencia muestra la infraestructura del laboratorio SIEM desplegada en contenedores, con servicios como Elastic, Kibana, Logstash, Filebeat, Snort, Nginx y una máquina víctima. Demuestra que el entorno está preparado para centralizar logs, monitorizar actividad y simular un escenario real de detección e investigación.

- Qué he aprendido: He aprendido cómo se organiza un entorno de monitorización de seguridad y cómo se relacionan entre sí las distintas piezas de un SIEM. También he entendido la importancia de integrar varias herramientas para poder recoger, correlacionar y analizar eventos de forma eficaz.


### Evidencia 2
- Archivo: ![Evidencia 2](evidencias/investigacion.png)
- Qué demuestra: Esta evidencia refleja el proceso de investigación de un incidente, con una cronología de eventos y una línea temporal de lo que fue ocurriendo. Demuestra la capacidad de ordenar la información, identificar las fases del ataque y relacionar cada acción con su evidencia correspondiente.

- Qué he aprendido: He aprendido a reconstruir un incidente paso a paso a partir de los datos disponibles. También he visto cómo una buena correlación temporal ayuda a entender mejor el comportamiento del atacante y a explicar el impacto del ataque de manera clara.


### Evidencia 3
- Archivo: ![Evidencia 3](evidencias/investigacion-logs.png)
- Qué demuestra: Esta evidencia muestra el análisis de logs y la revisión de registros para encontrar indicios de actividad sospechosa. Demuestra el uso de fuentes como access.log, auth.log o vsftpd.log para detectar accesos, intentos de intrusión y posibles movimientos del atacante.

- Qué he aprendido: He aprendido la utilidad que tienen los logs como fuente principal de evidencias en una investigación forense. También he comprendido que revisar registros de distintos servicios permite detectar patrones de ataque que, por separado, podrían pasar desapercibidos.


### Evidencia 4
- Archivo: ![Evidencia 4](evidencias/investigacion-2.png)
- Qué demuestra: Esta evidencia muestra la parte final del análisis, donde se interpretan las técnicas utilizadas durante el incidente y se relacionan con marcos de intrusión. Demuestra que no solo se observa lo ocurrido, sino que también se clasifica y se contextualiza dentro de una metodología de análisis.

- Qué he aprendido: He aprendido a identificar técnicas de ataque y a vincularlas con etapas concretas de un incidente real. Además, he entendido mejor cómo documentar un caso de forma profesional, clara y ordenada para que otras personas puedan seguir el razonamiento de la investigación.


## 4) Conclusión (cierre)
Esta unidad me ha ayudado a entender que una gestión de incidentes no consiste solo en detectar un ataque, sino en seguir un proceso ordenado para recoger evidencias, analizarlas y responder sin comprometer la investigación. También he reforzado la importancia de la cadena de custodia y de documentar bien cada paso para que el análisis sea útil tanto técnica como legalmente.


