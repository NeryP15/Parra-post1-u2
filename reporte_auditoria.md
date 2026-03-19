# Reporte de Auditoría de Usabilidad - Nequi

## 1. Resumen Ejecutivo
Este informe detalla los resultados de una auditoría de usabilidad exhaustiva realizada a la aplicación móvil Nequi (versión actual 2026) sobre la plataforma IOs. El objetivo primordial fue evaluar la calidad de la experiencia del usuario mediante la aplicación de las 10 Heurísticas de Jakob Nielsen, centrándose en los flujos de inicio de sesión, envío de dinero y gestión de servicios financieros.Durante la inspección sistemática, se identificaron 10 hallazgos significativos que afectan diversos niveles de la experiencia. 
El problema más crítico detectado (Severidad 4) se encuentra en el flujo de envío de fondos, donde la carencia de una función de "deshacer" tras la confirmación representa un riesgo elevado de error humano con consecuencias financieras directas para el usuario. Adicionalmente, se observaron deficiencias en la estética minimalista debido a una saturación de elementos comerciales en la interfaz principal. En términos generales, aunque la aplicación posee una base sólida de usabilidad y un lenguaje cercano al mundo real, requiere ajustes urgentes en el control del usuario y la prevención de errores para consolidarse como una herramienta totalmente centrada en el usuario.

## 2. Metodología
Para esta auditoría se utilizó el método de Inspección Heurística, siguiendo el ciclo de Diseño Centrado en el Usuario (DCU). El proceso se dividió en tres fases:

Exploración Libre: Se recorrió la aplicación como un usuario convencional para identificar la arquitectura de información y los flujos principales.

Inspección Sistemática: Cada pantalla de los 3 flujos seleccionados fue analizada minuciosamente contrastándola con las 10 reglas de oro de Nielsen.

Valoración de Severidad: Se asignó un valor de 0 a 4 a cada hallazgo, considerando la frecuencia del error, el impacto en la tarea y la persistencia del problema.

Las herramientas utilizadas incluyeron un dispositivo móvil IOs, la captura de pantalla nativa del sistema y el entorno de documentación en GitHub para asegurar la trazabilidad del proceso.

## 3. Hallazgos por Flujo
**Flujo A**: 

Inicio de Sesión y PerfilH8-A (Estética y diseño): La pantalla de inicio presenta una carga cognitiva elevada debido a la sección de "Sugeridos", que mezcla demasiados colores y marcas de terceros, distrayendo de las funciones de saldo.

H2-A (Mundo real): En la configuración del perfil se emplea terminología técnica como "Depósito de bajo monto", la cual no es intuitiva para el usuario promedio que busca términos más sencillos como "Límites de mi cuenta".

H1-C (Estado del sistema): Al existir latencia en la conexión, el saldo permanece oculto bajo asteriscos sin un indicador visual (spinner) que informe que el sistema está intentando actualizar los datos.

**Flujo B**: 

Envío de DineroH9-B (Recuperación de errores): Al presentarse el mensaje "¡No te alcanza!", el sistema bloquea al usuario obligándolo a retroceder manualmente, en lugar de ofrecer un acceso directo para mover fondos desde los "Bolsillos" de ahorro.

H3-B (Control y libertad): Tras presionar "Enviar", no existe un margen de tiempo ni un botón de cancelación inmediata, dejando al usuario sin control ante un error en el número de destino.

H6-B (Reconocimiento): En la lista de contactos favoritos no se visualizan fotos de perfil, obligando al usuario a reconocer el destino únicamente por iniciales o por el número telefónico memorizado.

H5-C (Prevención de errores): En ciertos campos de entrada de monto, el sistema despliega un teclado alfanumérico innecesario, aumentando la probabilidad de ingresar caracteres inválidos.

**Flujo C**: 

Gestión de ServiciosH4-C (Consistencia): Existe una ruptura visual en la iconografía de servicios; algunos mantienen el diseño de la marca externa mientras que otros usan iconos planos propios de Nequi.

H7-B (Flexibilidad y eficiencia): El sistema no recuerda los números de contrato para servicios públicos no marcados como favoritos, obligando a una entrada de datos repetitiva.

H10-B (Ayuda): El acceso a un asesor humano está profundamente oculto bajo capas de menús en el asistente virtual, dificultando la resolución de problemas complejos que la IA no cubre.

## 4. Tabla de Priorización Consolidada

| Prioridad | ID | Heurística Violada | Severidad Final | Recomendación |
| :--- | :--- | :--- | :---: | :--- |
| **1** | H3-B | Control y libertad | 4 | Implementar un botón de "Deshacer" por 3 segundos tras el envío. |
| **2** | H9-B | Recuperación de errores | 3 | Añadir botón de "Trasladar desde Bolsillos" en el error de saldo. |
| **3** | H10-B | Ayuda y documentación | 3 | Simplificar el acceso al chat humano en el centro de ayuda. |
| **4** | H7-B | Flexibilidad de uso | 3 | Implementar historial de datos para pagos de servicios recurrentes. |
| **5** | H4-C | Consistencia | 2 | Unificar el estilo visual de todos los iconos de servicios. |
| **6** | H1-C | Visibilidad del estado | 2 | Agregar un "spinner" o carga visual mientras se actualiza el saldo. |
| **7** | H2-A | Mundo real | 2 | Cambiar términos bancarios por lenguaje cotidiano y simple. |
| **8** | H6-B | Reconocimiento | 2 | Incluir fotos de perfil en la lista de contactos favoritos. |
| **9** | H8-A | Estética minimalista | 1 | Agrupar la publicidad de terceros en una sección menos invasiva. |
| **10** | H5-C | Prevención de errores | 1 | Configurar el teclado numérico por defecto en campos de monto. |

## 5. Análisis de Patrones
Se identificaron dos patrones recurrentes que afectan la usabilidad de la aplicación:

Priorización Comercial sobre la Simplicidad: La app viola consistentemente la heurística de Estética y Diseño Minimalista (H8). El patrón muestra que se otorga más peso visual a la venta de servicios de terceros que a las acciones principales del usuario, lo que genera ruido visual y distracción en la navegación.

Rigidez en el Manejo de Errores y Control: Existe un patrón de falta de apoyo en momentos críticos. El sistema informa que algo salió mal (H9) o pide confirmar (H3), pero no ofrece una "salida de emergencia" o una solución inmediata. La app tiende a ser punitiva (bloquea el flujo) en lugar de ser facilitadora, especialmente en procesos donde hay dinero involucrado.

## 6. Conclusiones
La auditoría revela que Nequi es una aplicación funcional y robusta, pero que ha comenzado a sufrir de "sobrecarga de funciones", afectando la claridad que la caracterizaba inicialmente. Mientras que la relación con el mundo real es aceptable, el Control y Libertad del Usuario y la Prevención de Errores son las áreas con mayor oportunidad de mejora.

Se concluye que la implementación de mecanismos de reversibilidad en los pagos y una limpieza profunda de la interfaz principal no solo mejorarían los índices de satisfacción, sino que reducirían los errores operativos de los usuarios. La aplicación debe evolucionar de ser un catálogo de servicios a ser una herramienta financiera que acompañe y proteja al usuario en cada paso de su interacción
