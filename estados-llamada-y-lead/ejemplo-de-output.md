# Ejemplo de output

> Ejemplo con datos ficticios. Negocio digital que vende mentoría por llamada, CRM en GoHighLevel, 1 setter y 1 closer, sin reservas.

# Estados de llamada y de lead · Mentoría ejemplo

## Lo que hay hoy
Campo único «Etapa» en el pipeline:
| Valor actual | Es de |
|---|---|
| Agendado | Lead |
| No show | Llamada |
| Reagendado | Llamada |
| Seguimiento | Lead |
| Cerrado | Lead |
| No show - perdido | Mezcla |
| Perdido | Lead |

## Los dos campos
**Estado de la llamada** (campo personalizado de la oportunidad, lo carga el closer el mismo día)
| Valor | Criterio | Quién |
|---|---|---|
| Esperando llamada | Hay fecha agendada a futuro | Automático al agendar |
| Asistida | La persona se conectó | Closer |
| No show | No se conectó ni avisó | Closer |
| Cancelada por el lead | Avisó antes de la hora | Closer o setter |
| Reagendada | Hay nueva fecha | Closer o setter |

**Estado del lead** (etapa del pipeline)
| Valor | Criterio | Quién |
|---|---|---|
| Agendado | Tiene una llamada en Esperando | Setter |
| Seguimiento | Hubo llamada u oferta y no decidió | Closer |
| Ganado | Pago acreditado | Closer |
| Perdido | Dijo que no o no responde hace 14 días [SUPUESTO: confirmalo con el founder] | Closer |

## Campos obligatorios según el estado
| Si… | Campo obligatorio | Valores |
|---|---|---|
| La llamada está Asistida | Calificación del closer | Alta · Media · Baja · No califica |
| La llamada está Asistida | ¿Hubo oferta? | Sí · No |
| El lead está en Seguimiento | Fecha del próximo seguimiento | Fecha |
| El lead está Perdido | Motivo | Precio · Tiempo · Socio o pareja · Confianza · No califica · No respondió · Otro |

## Migración
El campo viejo «Etapa» se archiva, no se borra.
| Valor viejo | Estado llamada | Estado lead |
|---|---|---|
| Agendado | Esperando llamada si la fecha es futura · A revisar si ya pasó | Agendado |
| No show | No show | A revisar |
| Reagendado | Reagendada | Agendado |
| Seguimiento | Asistida | Seguimiento |
| Cerrado | Asistida | Ganado |
| No show - perdido | No show | Perdido |
| Perdido | A revisar | Perdido |

## Las tasas que vas a poder medir
Con los datos de octubre ya migrados: asistencia 62 %, no show 20 %, cancelación 12 %, reagendadas 6 %, cierre sobre asistidas 31 %, cierre sobre ofertas 44 %. Antes, el CRM mostraba "cierre 19 %" porque dividía por todas las agendas.

## Cómo se configura en GoHighLevel
1. **Estado del lead:** son las etapas del pipeline. Renombrá las etapas actuales a Agendado · Seguimiento · Ganado · Perdido.
2. **Estado de la llamada:** creá un campo personalizado de la oportunidad, de tipo desplegable, con los cinco valores de arriba.
3. **Campos obligatorios:** creá también como campos de la oportunidad la calificación del closer, «¿Hubo oferta?», la fecha del próximo seguimiento y el motivo de pérdida. El closer los completa al mover la oportunidad; los viernes se revisan los que quedaron vacíos.
4. **Automático al agendar:** un workflow que, cuando se agenda una cita, ponga el Estado de la llamada en Esperando llamada y la oportunidad en Agendado.
5. **Campo viejo:** guardá «Etapa» como un campo de texto de solo lectura con el valor que tenía cada oportunidad antes de migrar.

Si no encontrás alguna opción con ese nombre, buscá «campos personalizados» y «workflows» en la configuración de tu cuenta.

## Para confirmar
- Cuántos días sin respuesta pasan a Perdido.

Las primeras dos semanas, revisá cada viernes que ninguna llamada que ya pasó siga en Esperando llamada. Ese es el error más común.
