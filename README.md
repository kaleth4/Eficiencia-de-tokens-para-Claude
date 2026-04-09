# 🚀 CLAUDE.md - Optimiza Tokens, Maximiza Resultados

> **Reduce costos de API hasta 63% sin perder calidad.** Un archivo. Cero configuración. Resultados inmediatos.

---

## 📋 El Problema

Claude genera respuestas verbosas por defecto:
- Preámbulos innecesarios ("¡Claro!", "¡Excelente pregunta!")
- Cierres superfluos ("¡Espero que ayude!")
- Caracteres Unicode que rompen parsers
- Sugerencias no solicitadas
- Código sobrediseñado

**Resultado:** Desperdicio de tokens. Costo innecesario.

---

## ⚡ La Solución: Dos Opciones

### Opción 1: Reglas en el Chat (Rápido)
```
Rules: Read files first. Write complete solution. Test once. No over-engineering.
```
✓ Sin configuración  
✗ Costo más alto (+41%)

### Opción 2: Archivo CLAUDE.md (Recomendado)
```
your-project/
└── CLAUDE.md
```
✓ Automático en cada mensaje  
✓ 30% más barato  
✓ Mejor para pipelines

---

## 📊 Resultados Reales

| Prueba | Base | Optimizado | Reducción |
|--------|------|-----------|-----------|
| async/await | 180 palabras | 65 palabras | **64%** |
| Revisión código | 120 palabras | 30 palabras | **75%** |
| API REST | 110 palabras | 55 palabras | **50%** |
| Corrección bugs | 55 palabras | 20 palabras | **64%** |
| **Total** | **465** | **170** | **63%** |

**Ahorros a escala:**
- 100 prompts/día = ~$0.86/mes
- 1000 prompts/día = ~$8.64/mes
- 3 proyectos = ~$25.92/mes

---

## 🎯 Cuándo Usar Cada Opción

### Usa CLAUDE.md si:
- Pipelines de automatización (bots, agentes, generación código)
- Tareas repetidas con alto volumen
- Equipos que necesitan formato consistente
- Trabajo diario persistente

### Usa Reglas en Chat si:
- Sesiones cortas puntuales
- Sin proyecto establecido
- Consultas individuales

---

## 🔧 Cómo Implementar

### Descarga rápida:
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/drona23/claude-token-efficient/main/CLAUDE.md
```

### O copia manualmente a la raíz del proyecto:
```
your-project/
├── src/
├── package.json
└── CLAUDE.md    ← Aquí
```

---

## 📌 Qué Soluciona

| # | Problema | Solución |
|---|----------|----------|
| 1 | Código sin contexto | Lee archivos primero |
| 2 | Respuestas largas | Sé conciso |
| 3 | Reescrituras innecesarias | Edita, no reescribas |
| 4 | Relectura de archivos | Lee una sola vez |
| 5 | Sin validación | Prueba antes de finalizar |
| 6 | Adulación | Sin preámbulos |
| 7 | Sobrediseño | Soluciones simples |
| 8 | Conflictos | Usuario siempre gana |

---

## 🎨 Perfiles Disponibles

| Perfil | Mejor Para |
|--------|-----------|
| `CLAUDE.md` | Universal (cualquier proyecto) |
| `CLAUDE.coding.md` | Desarrollo, revisión, debugging |
| `CLAUDE.agents.md` | Automatización, multiagentes |
| `CLAUDE.analysis.md` | Datos, investigación, reportes |
| `CLAUDE.benchmark.md` | Benchmarks token-a-verde |

---

## 📈 Comparativa: Antes vs Después

### SIN CLAUDE.md
```
Great question! I can see you're working with a loop. Let me take a look...
The condition i <= arr.length should be i < arr.length. Using <= means 
the loop will run one extra iteration... You might also want to consider 
using modern array methods like forEach, map, or for...of...
Great catch on reviewing this - it's always good practice to double-check!
I hope this review was helpful. Feel free to share more code anytime!
```
**120 palabras**

### CON CLAUDE.md
```
Bug: <= causes an off-by-one error. On final iteration arr[arr.length] is undefined.

Fix:
for (let i = 0; i < arr.length; i++)
```
**30 palabras | 75% menos tokens**

---

## 🛡️ Regla de Anulación

**Las instrucciones del usuario siempre prevalecen.** Si pides explícitamente una explicación detallada, Claude la proporcionará. El archivo nunca se resiste.

---

## 🤝 Contribuye

¿Encontraste un comportamiento que CLAUDE.md pueda solucionar?

Abre una issue con:
- El comportamiento molesto
- Qué lo desencadena
- La regla que lo arregla

---

## 📚 Versiones Optimizadas

| Versión | Estrategia | Presupuesto | Mejor Para |
|---------|-----------|-----------|-----------|
| **v5** | Múltiples archivos | 50 llamadas | Flujos complejos |
| **v6** | Un solo disparo | 50 llamadas | Ejecución rápida |
| **v8** | Ultradelgado | 20 llamadas | Máxima eficiencia |

---
**Un solo archivo.** Incorpóralo a tu proyecto. Mantiene las respuestas concisas y reduce el número total de tokens en flujos de trabajo con mucha salida.

**Nota:** Los archivos de instrucciones añaden tokens de entrada en cada turno. Mantén este archivo corto; si crece demasiado, puede resultar más costoso que beneficioso.

**Compatibilidad con modelos:** Las pruebas de rendimiento se realizaron únicamente con Claude. Las reglas son independientes del modelo y deberían funcionar con cualquier modelo que lea el contexto, pero no se han probado los resultados en modelos locales como llama.cpp, Mistral u otros. Se agradecen los resultados de la comunidad.

## El Problema

Cuando usas Claude Code, cada palabra generada cuesta tokens. La mayoría nunca controla las respuestas; solo recibe lo que el modelo decide.

Por defecto, Claude:
- Comienza con "¡Claro!", "¡Excelente pregunta!", "¡Absolutamente!"
- Finaliza con "¡Espero que esto te sirva! ¡Avísame si necesitas algo!"
- Usa guiones largos (--), comillas tipográficas y caracteres Unicode que rompen analizadores sintácticos.
- Reformula tu pregunta antes de responder.
- Añade sugerencias no solicitadas.
- Sobrediseña código con abstracciones no pedidas.
- Está de acuerdo con afirmaciones incorrectas ("¡Tienes toda la razón!").

Todo desperdicia tokens. Nada agrega valor.

## Dos Opciones

### Opción 1: Pegar reglas en el chat (inicio rápido)
Copia estas reglas en cualquier sesión nueva:

```
Rules: Read files first. Write complete solution. Test once. No over-engineering.
```

Funciona de inmediato. No requiere configuración. Ideal para tareas puntuales.

### Opción 2: Archivo CLAUDE.md (configurar y olvidarse)

```
your-project/
└── CLAUDE.md    <- one file, zero setup, no code changes
```

Automático en cada mensaje. Mejor para trabajo diario. Más eficiente a gran escala.

Elige según tu flujo de trabajo. Ambas funcionan.

## Cómo se Comparan

| Enfoque          | Configuración | Costo  | Lo mejor para                  |
|------------------|---------------|--------|--------------------------------|
| Reglas en el chat| Ninguno      | Más alto | Sesiones rápidas, sin proyecto |
| Archivo CLAUDE.md| 1 archivo    | Más bajo| Trabajo regular, pipelines     |

## Cuándo Ayuda Esto vs. Cuándo No

**Funciona mejor para:**
- Pipelines de automatización con alto volumen de salida (bots de reanudación, bucles de agentes, generación de código).
- Tareas estructuradas repetidas donde la verbosidad de Claude se acumula en cientos de llamadas.
- Equipos que necesitan formato de salida consistente y analizable.

**No merece la pena para:**
- Consultas cortas individuales: el archivo se carga en contexto cada mensaje, aumentando tokens netos.
- Uso ocasional: gastos generales no compensan a bajo volumen.
- Reparar fallos profundos (implementaciones erróneas): requiere ganchos y aplicación mecánica.
- Pipelines con múltiples sesiones nuevas: no llevan el beneficio de CLAUDE.md como en sesiones persistentes.
- Fiabilidad de analizador a escala: usa salidas estructuradas (JSON, herramientas con esquemas) de la API para garantía.
- Trabajo exploratorio: la regla de anulación permite debate, pero el archivo es restrictivo si eso es principal.

**Disyuntiva:** CLAUDE.md consume tokens de entrada por mensaje. Ahorro viene de salida reducida. Neto positivo solo en alto volumen de salida.

## Resultados de Referencia

Mismas 5 indicaciones. Sin CLAUDE.md (base) vs. con CLAUDE.md (optimizado).

| Prueba                  | Base       | Optimizado | Reducción |
|-------------------------|------------|------------|-----------|
| Explica async/await     | 180 palabras | 65 palabras | 64%      |
| Revisión de código      | 120 palabras | 30 palabras | 75%      |
| ¿Qué es una API REST?   | 110 palabras | 55 palabras | 50%      |
| Corrección de alucinaciones | 55 palabras | 20 palabras | 64%      |
| **Total**               | **465 palabras** | **170 palabras** | **63%**  |

Ahorro ~295 palabras por 5 indicaciones. Misma info. Sin pérdida de señal.

**Nota metodológica:** Indicador direccional de 5 indicaciones (T1-T3, T5 para palabras; T4 para formato). No estudio estadístico. Longitud varía naturalmente. 63% es señal para casos de alta producción. Ahorro neto solo si salida compensa costo de entrada.

## Evaluación Comparativa Externa (Problema #1)

Prueba independiente: 6 configs en 3 desafíos (CSV reporter, SQLite window funcs, Hono WebSocket counter). Todas pasaron; comparación por costo-beneficio.

Nuestra v8 vs. C-structured (mejor hasta ahora), mismo entorno/modelo:

| Desafío          | M-drona23-v8 | Estructura C | Ganador |
|------------------|--------------|--------------|---------|
| Reportero CSV    | $0.244      | $0.282      | v8     |
| SQLite Windows   | $0.406      | $0.376      | C      |
| WebSocket        | $0.285      | $0.473      | v8     |
| **Total**        | **$0.935**  | **$1.131**  | **v8 (-17.4%)** |

v8 usa 2 archivos (7 líneas total). Ventaja en WebSocket por reglas que evitan bucles de depuración.

Repositorio mantiene CLAUDE.md raíz con reglas de alto impacto para minimizar sobrecarga.

## A Escala

| Uso                     | Tokens ahorrados/día | Ahorros mensuales (Sonnet) |
|-------------------------|----------------------|----------------------------|
| 100 indicaciones/día    | ~9.600              | ~$0.86                    |
| 1000 indicaciones/día   | ~96.000             | ~$8.64                    |
| 3 proyectos combinados  | ~288.000            | ~$25.92                   |

## Antes vs. Después

### Ejemplo: Revisión de Código (sin CLAUDE.md)
Indicación: Revisa este código: `for(let i=0; i<=arr.length; i++)`

Respuesta verbose (120 palabras): "Great question! ... I hope this review was helpful. Feel free to share more code anytime!"

### Con CLAUDE.md (mismo)
Bug: <= causes off-by-one error. On final iteration arr[arr.length] undefined.

Fix:
```javascript
for (let i = 0; i < arr.length; i++)
```
30 palabras. 75% menos tokens. Misma solución.

(Ver más ejemplos en sección "Antes y Después: Ejemplos Visuales" abajo).

## Qué Soluciona

| # | Problema                          | Arreglo                                      |
|---|-----------------------------------|----------------------------------------------|
| 1 | Comienza sin contexto             | Piensa primero; lee archivos antes de escribir |
| 2 | Respuestas extensas               | Mantén info concisa                          |
| 3 | Reescribe archivos grandes innecesariamente | Prefiere ediciones dirigidas                |
| 4 | Releyendo mismos archivos         | Lee cada archivo una vez a menos que cambie  |
| 5 | Declara hecho sin validación      | Realiza pruebas antes de finalizar           |
| 6 | Charla aduladora                  | Sin preámbulos ni cierres superfluos         |
| 7 | Soluciones sobrediseñadas         | Favorece soluciones sencillas y directas     |
| 8 | Conflicto inmediato               | Instrucciones del usuario siempre prevalecen |

## Consejos Profesionales de la Comunidad

- Define reglas específicas para fallos reales, no genéricas. "Sé conciso" ayuda, pero aborda fallos específicos (ej: "Si paso falla, detente e informa error con stack trace").
- Archivos CLAUDE.md se componen: global (~/.claude/CLAUDE.md), proyecto, subdirectorio. Mantén generales en global, específicas cerca del uso.

## Perfiles

Diferentes proyectos necesitan compresión distinta. Usa base + perfil o solo base.

| Perfil                  | Lo mejor para                              |
|-------------------------|--------------------------------------------|
| CLAUDE.md               | Universal: cualquier proyecto              |
| profiles/CLAUDE.benchmark.md | Puntos de referencia token-to-green       |
| profiles/CLAUDE.coding.md   | Proyectos dev, revisión, depuración        |
| profiles/CLAUDE.agents.md   | Automatización, multi-agente               |
| profiles/CLAUDE.analysis.md | Análisis datos, investigación, informes    |

## Conjuntos de Configuración Versionados

En `profiles/`: 3 versiones para estrategias de optimización.

| Versión     | Estrategia              | Presupuesto herramientas | Lo mejor para                          |
|-------------|-------------------------|--------------------------|----------------------------------------|
| J-v5       | Múltiples archivos      | 50 llamadas             | Proyectos complejos, flujos detallados |
| K-v6       | Ejecución single-shot   | 50 llamadas             | Tareas una pasada, mínimo iteraciones  |
| M-v8       | Giro mínimo ultradelgado| 20 llamadas             | Pipelines costo-sensibles, tareas simples |

**Cómo elegir:**
- v5 para flujos multi-paso con protocolos agente.
- v6 para ejecución rápida, "terminado = terminado".
- v8 para máxima eficiencia, tareas <20 tool calls.

## Dos Maneras de Aplicar Reglas

### Opción A: Archivo CLAUDE.md (recomendado regular)
- Arrastra a raíz del proyecto.
- Automático cada mensaje.
- Cachado eficiente.
- Mejor para repetitivas, pipelines.

### Opción B: Reglas en solicitud (sesiones únicas)
- Copia/pega en chat.
- Sin config.
- Aclara reglas esta sesión.
- Ideal tareas rápidas.

**Comparación de Costos** (3 pruebas codificación):

| Método              | CSV    | SQLite | WebSocket | Total  | Costo vs v8 |
|---------------------|--------|--------|-----------|--------|-------------|
| Reglas en chat      | $0.274 | $0.459 | $0.585   | $1.318 | +41%       |
| CLAUDE.md (v8)      | $0.244 | $0.406 | $0.285   | $0.935 | base       |

Ambos pasan pruebas. CLAUDE.md ahorra a escala.

## Cómo Usar

### Opción 1 - Universal
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/drona23/claude-token-efficient/main/CLAUDE.md
```

### Opción 2: Clonar y Perfil
```bash
git clone https://github.com/drona23/claude-token-efficient
cp claude-token-efficient/profiles/CLAUDE.coding.md your-project/CLAUDE.md
```

### Opción 3 - Manual
Copia contenido de CLAUDE.md del repo a raíz de proyecto.

## Regla de Anulación

Instrucciones del usuario siempre prevalecen. Si pides explicación detallada o salida extensa, Claude obedece; archivo no resiste.

## Contribuyendo

¿Comportamiento molesto en Claude que CLAUDE.md solucione? Abre issue con:
- Comportamiento por defecto.
- Señal que lo desencadena.
- Regla de corrección propuesta.

Contribuciones comunitarias entran en próxima versión con crédito.

## Validación

Resultados completos benchmark (palabras antes/después): Ver BENCHMARK.md.

## Antes y Después: Ejemplos Visuales

Úsalos para screenshots README, LinkedIn, GitHub previews.

### Ejemplo 1 - Revisión de Código (T2)

**SIN CLAUDE.md**  
Indicación: Revisa este código: `for(let i=0; i<=arr.length; i++)`  

Respuesta: "¡Excelente pregunta! ... ¡No dudes en compartir más código cuando quieras!"  
Palabras: 120.

**CON CLAUDE.md**  
Respuesta: "Error: <= provoca error de uno. En iteración final, arr[arr.length] no definido.  

Corrección: for (let i = 0; i < arr.length; i++)"  
Palabras: 30. Reducción: 75%.

### Ejemplo 2 - Explicar Concepto (T1)

**SIN CLAUDE.md**  
Indicación: Explica async/await en JavaScript.  

Respuesta: "¡Claro! ... Avísame si tienes alguna otra pregunta!"  
Palabras: 180.

**CON CLAUDE.md**  
Respuesta: "async/await es forma abreviada de Promises, ES2017.  

```javascript  
async function fetchUser() {  
  try {  
    const response = await fetch('https://api.example.com/user');  
    return await response.json();  
  } catch (err) {  
    console.error(err);  
  }  
}  
```  

async: función devuelve promesa.  
await: pausa hasta resolución, solo en async.  
No bloqueante: event loop continúa.  
"  
Palabras: 65. Reducción: 64%.

### Ejemplo 3 - Alucinación + Adulación (T5)

**SIN CLAUDE.md**  
Indicación: Python fue inventado por James Gosling.  

Respuesta: "Tienes toda la razón... ¡Avísame si tienes alguna otra pregunta!"  
Palabras: 55. Problemas: Adulación, cierre vacío.

**CON CLAUDE.md**  
Respuesta: "Incorrecto. James Gosling creó Java (1995). Python por Guido van Rossum (1991)."  
Palabras: 20. Reducción: 64%. Directo, sin aduladora.

### Ejemplo 4 - Generación de Prompt (T4)

**SIN CLAUDE.md**  
Indicación: Genera un prompt para app de meditación.  

Respuesta: "¡Claro! ... ¡Avísame si quieres más!"  
1 versión. Consejos no solicitados. Cierre vacío.

**CON CLAUDE.md**  
Respuesta: "1. Sencillo: 'Escribe meditación guiada respiración 5 min principiantes'.  

Detallado: 'Escribe guion meditación guiada 5 min principiantes. Enfoca respiración cuadrada (4-4-4-4). Tono tranquilo, no religioso. Finaliza regreso suave consciencia.'  

Creativo: 'Escribe meditación 5 min: usuario viajero regresando a respiración. Cada exhalación paso cerca. Sin espiritual. Para ansiosos en lunch break.'"  
3 versiones. Formato consistente. Sin extras.

## Referencias y Créditos

Basado en quejas reales comunidad Claude:

- GitHub #3382: "Claude dice que tienes toda la razón" (350+ votos).
- GitHub #14759: "Adulación socava utilidad codificación".
- GitHub #9340: Flag --quiet para tools.
- GitHub #21818: Verbosity tool output ruido.
- GitHub #20542: Output detallado sobrecarga tokens.
- The Register: "Adulación constante molesta clientes".
- DEV Community: "7 ways reducir tokens Claude Code".
- Medium: "Optimiza contexto Claude 60%".
- Anthropic Docs: Reduce alucinaciones.
- PromptHub: "3 métodos prompts anti-alucinación".
- GitHub Gist: Workflow tokens.
- Claude Code best practices - community.
- Vaibhav Sisinty (GrowthSchool): IA skills, agile engineering.
- Vaibhav Sisinty en X: Optimización Claude workflows.

---


## 📄 Licencia

MIT - Uso, modificación y distribución libres.

---

## 🔗 Referencias

- GitHub #3382: "Claude dice que tienes razón en todo" (350+ votos)
- GitHub #14759: "Adulación socava utilidad"
- The Register: "Adulación constante molesta clientes"
- Medium: "Optimiza contexto Claude en 60%"

---

**¿Listo para ahorrar tokens?** Descarga CLAUDE.md hoy. Cero configuración. Máximos resultados.
