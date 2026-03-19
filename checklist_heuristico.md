# Checklist Heurístico - Auditoría Nequi

## Tabla de Evaluación General
se tomara en cuenta lo siguiente: Heurística,Cumplimiento,Notas y Severidad (0-4) en ese orden:

H1: Visibilidad del estado 

H2: Lenguaje del mundo real 

H3: Control del usuario

H4: Consistencia 

H5: Prevención de errores

H6: Reconocimiento 

H7: Flexibilidad de uso

H8: Estética minimalista

H9: Recuperación de errores

H10: Ayuda 

## Registro de Hallazgos 
ID,Heurística Violada,Pantalla,Descripción del Problema,Evidencia,Severidad:

**H8**  Estética y diseño,Inicio,"Exceso de elementos visuales y publicidad en ""Sugeridos"" que saturan la interfaz.",image_436efc.png,1

**H9**  Recuperación de errores,"Mensaje ""No te alcanza""","El error bloquea al usuario; no ofrece mover plata desde ""Bolsillos"" directamente.",image_436c53.png,3

**H3** Control y libertad,Confirmación Envío,"Tras dar clic en enviar, no existe opción de ""Deshacer"" o cancelar la acción inmediata.",evidencia3.png,4

**H4** Consistencia,Servicios,Iconografía inconsistente; mezcla de logos comerciales con iconos planos de la app.,evidencia4.png,2

**H2** Mundo real,Ajustes/Perfil,"Uso de lenguaje técnico bancario como ""Depósito de bajo monto"" en lugar de términos simples.",evidencia5.png,2

**H6** Reconocimiento,Favoritos,Solo se muestran iniciales; el usuario debe recordar a qué número corresponde cada contacto.,evidencia6.png,2

**H7** Flexibilidad,Pagos de servicios,"No hay memoria de datos para servicios no frecuentes, obligando a reescribir todo.",evidencia7.png,3

**H1** Estado del sistema,Pantalla de carga,"El saldo oculto por demora de red no muestra un ""spinner"" o estado de carga claro.",evidencia8.png,2

**H5** Prevención errores,Recargas,Despliegue de teclado alfanumérico en campos que solo aceptan números.,evidencia9.png,1

**H10** Ayuda,Asistente Virtual,Ruta compleja para contactar a un asesor humano dentro del flujo de ayuda automática.,evidencia10.png,3

