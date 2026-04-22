# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID:** 3.a..e
> **Unidad / Tema:**  Unidad 3
> **Alumno/a:**  Nerea Candón Ramos
> **Fecha:**  30/04/2026

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.

### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
En esta práctica me pareció muy interesante ya que esta unidad se centro en como recopilamos las evidencias e investigar un incidente, hemos utilizado la tabla MITRE para poder entender los pasos que hace un atacante y recopilar toda la información posible y poder contener el incidente. He aprendido hacer una línea temporal de todo un incidente y seguir el ritmo de un ataque

### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
Pienso que lo más útil para mi futuro puesto es saber analizar bien un incidente y realizar un infome que explique de manera clara todo lo que está pasando en el incidente y el proceso. También el indentificar cada fase y las alertas para poder detectar el mínimo cambio.

### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
En las anteriores unidades ya vimos el proceso de como crear un informe, recopilar las evidencias y preservarlas de manera adecuada para no perder la información y lo que es nuevo para mi es el uso de la tabla MITRE para organizar los tipos de ataques que hay y poder tener un control del incidente. También la forma de contener el incidente.

### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
Lo que me ha parecido más interesante es conocer la matriz MITRE ATT&CK, me parece interesante la manera que se creó la tabla y como organizaron todo de manera que se pueda seguir un incidente de manera clara.

### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
No recortaría ninguna parte, ya que todos los conceptos están conectados entre sí y forman parte del proceso completo de gestión de incidentes. Reducir contenido dificultaría la comprensión global.

### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
Me hubiera gustado hacer algun taller o alguna actividad en clase que todos hubieramos participado para hacer un caso real e intentar resolverlo, recrear como sería y analizarlo.

### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
Aplicaría un procedimiento ordenado de aislamiento del sistema afectado y recogida de evidencias, priorizando la preservación de la información antes de cualquier acción que pueda modificar el estado del sistema.

### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
La cadena de custodia me parece una forma fácil de invalidar una prueba de manera legal solo por cometer un error al manipular la evidencia y no seguir el protocolo y me queda en duda si un juez aceptaría una evidencia si no tenemos herramientas gorenses profesionales para certificarlas


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
- Archivo: `evidencias/01_...`
- Qué demuestra:
- Qué he aprendido:

### Evidencia 2
- Archivo: `evidencias/02_...`
- Qué demuestra:
- Qué he aprendido:


## 4) Conclusión (cierre)
- 
