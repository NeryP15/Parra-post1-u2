# Checklist Heurístico - Auditoría Nequi

## Tabla de Evaluación General
se tomara en cuenta lo siguiente: Heurística,Cumplimiento,Notas y Severidad (0-4) en ese orden:
H1: Visibilidad del estado | Cumple | El saldo se ve claro al inicio. | 0 |
H2: Lenguaje del mundo real | Cumple | Usa términos como "Saca plata". | 0 |
H3: Control del usuario | No cumple | No permite cancelar envíos rápidos. | 3 |
H4: Consistencia | Cumple | Los colores son los de la marca. | 0 |
H5: Prevención de errores | No cumple | Deja escribir números de cel errados. | 2 |
H6: Reconocimiento | Cumple | Los iconos son estándar. | 0 |
H7: Flexibilidad de uso | Cumple | Tiene accesos rápidos. | 0 |
H8: Estética minimalista | Cumple | Diseño limpio y profesional. | 0 |
H9: Recuperación de errores| Parcial | Los mensajes de error son genéricos. | 2 |
H10: Ayuda | Cumple | Tiene sección de ayuda activa. | 0 |

## Registro de Hallazgos (Mínimo 10)
**ID:** H3-A  
**Heurística:** H3 - Control y libertad del usuario  
**Pantalla:** Confirmación de Envío  
**Descripción:** El botón de "atrás" desaparece en el último paso.  
**Evidencia:** `evidencias/error1.png`  
**Severidad:** 2
