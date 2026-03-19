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
ID,Heurística Violada,Pantalla,Descripción del Problema,Evidencia,Severidad
H8-A,H8: Estética y diseño,Inicio,"Exceso de elementos visuales y publicidad en ""Sugeridos"" que saturan la interfaz.",image_436efc.png,1
H9-B,H9: Recuperación de errores,"Mensaje ""No te alcanza""","El error bloquea al usuario; no ofrece mover plata desde ""Bolsillos"" directamente.",image_436c53.png,3
H3-B,H3: Control y libertad,Confirmación Envío,"Tras dar clic en enviar, no existe opción de ""Deshacer"" o cancelar la acción inmediata.",evidencia3.png,4
H4-C,H4: Consistencia,Servicios,Iconografía inconsistente; mezcla de logos comerciales con iconos planos de la app.,evidencia4.png,2
H2-A,H2: Mundo real,Ajustes/Perfil,"Uso de lenguaje técnico bancario como ""Depósito de bajo monto"" en lugar de términos simples.",evidencia5.png,2
H6-B,H6: Reconocimiento,Favoritos,Solo se muestran iniciales; el usuario debe recordar a qué número corresponde cada contacto.,evidencia6.png,2
H7-B,H7: Flexibilidad,Pagos de servicios,"No hay memoria de datos para servicios no frecuentes, obligando a reescribir todo.",evidencia7.png,3
H1-C,H1: Estado del sistema,Pantalla de carga,"El saldo oculto por demora de red no muestra un ""spinner"" o estado de carga claro.",evidencia8.png,2
H5-C,H5: Prevención errores,Recargas,Despliegue de teclado alfanumérico en campos que solo aceptan números.,evidencia9.png,1
H10-B,H10: Ayuda,Asistente Virtual,Ruta compleja para contactar a un asesor humano dentro del flujo de ayuda automática.,evidencia10.png,3
