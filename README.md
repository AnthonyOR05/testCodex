# Actividad de GitHub Classroom: Propuesta de Práctica Temática (enfoque en documentación)

## 1) Título de la actividad
**Diseño de Propuesta: Mini Proyecto de Sistemas en Terminal**

> Puedes personalizar el nombre final de tu propuesta con un título temático claro, por ejemplo:
> - “Mini Toolkit en ARM64”
> - “Asistente de Estudio en Terminal”
> - “Reporteador de Información del Sistema”
> - “Organizador de Archivos”
> - “Juego de Aprendizaje en Línea de Comandos”

---

## 2) Descripción general
En esta actividad vas a **diseñar y documentar** la propuesta de una práctica temática pequeña para una materia de arquitectura de computadoras o programación de sistemas.

Tu propuesta debe plantear un proyecto **alcanzable, claro y bien justificado**, priorizando la documentación antes de desarrollar mucho código.

### Lenguaje principal (elige uno)
- ARM64 Assembly
- C
- Python
- Bash

> **Nota importante sobre ARM64 Assembly:** se recomienda únicamente para programas **muy pequeños** (por ejemplo, utilerías básicas, ejercicios de manejo de registros, I/O mínima o flujo de control simple).

### Enfoque obligatorio
La prioridad de esta tarea es:
1. Definir el caso de uso.
2. Justificar el alcance.
3. Diseñar estructura de repositorio.
4. Planear pruebas básicas.
5. Dejar una base clara para implementar después.

### Restricciones de alcance
Para mantener la actividad compatible con herramientas de IA con uso limitado (como planes gratuitos), tu proyecto debe ser pequeño y sin complejidad innecesaria.

**Evita incluir:**
- Proyectos grandes o de múltiples módulos complejos.
- Frameworks pesados.
- APIs pagadas.
- Bases de datos.
- Servicios en la nube.
- Contenedores.
- Dependencias complicadas o difíciles de instalar.

---

## 3) Entregables del estudiante
Tu repositorio debe incluir, como mínimo:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si decides agregar prototipo mínimo):
- `src/`
- `scripts/`
- `tests/`

---

## 4) Estructura recomendada del repositorio
Usa esta estructura base:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

---

## 5) Guía de contenido por archivo

### `README.md`
Incluye:
- Título del proyecto.
- Resumen en 1 párrafo.
- Lenguaje elegido y razón breve.
- Alcance del proyecto (qué sí hará y qué no hará).
- Instrucciones mínimas para ejecutar (si ya existe prototipo).

### `docs/propuesta.md`
Incluye:
- Problema u oportunidad que atiende tu práctica.
- Objetivo general.
- 3 a 5 objetivos específicos.
- Justificación técnica (por qué ese lenguaje y ese enfoque).
- Alcance y límites.
- Estimación de esfuerzo (pequeño, mediano de aula, etc.).

### `docs/caso_de_uso.md`
Incluye:
- Contexto del usuario (quién lo usaría).
- Escenario principal paso a paso.
- Entradas esperadas.
- Salidas esperadas.
- Casos límite básicos.

### `docs/estructura_repositorio.md`
Incluye:
- Árbol del repositorio.
- Descripción de cada carpeta/archivo.
- Convenciones de nombres (archivos, scripts, funciones).
- Estrategia para crecimiento futuro sin romper simplicidad.

### `docs/plan_de_pruebas.md`
Incluye:
- Objetivo de pruebas.
- Lista de pruebas funcionales mínimas (5 a 10).
- Criterios de aceptación por prueba.
- Resultado esperado por prueba.
- Riesgos conocidos y qué no se probará en esta etapa.

---

## 6) Criterios de evaluación sugeridos (rúbrica)

| Criterio | Excelente (100) | Bueno (85) | Suficiente (70) | Insuficiente (<70) |
|---|---|---|---|---|
| Claridad de la propuesta | Problema, objetivo y alcance totalmente claros y coherentes | Claros con ligeras ambigüedades | Entendibles pero incompletos | Confusos o contradictorios |
| Justificación técnica | Lenguaje y enfoque muy bien argumentados | Argumentación adecuada | Argumentación limitada | Sin justificación real |
| Estructura del repositorio | Ordenada, consistente y mantenible | Ordenada con detalles menores | Funcional pero desorganizada | Estructura deficiente |
| Caso de uso | Bien definido, realista y verificable | Definido con pocos huecos | General, poco detallado | Incompleto o irreal |
| Plan de pruebas | Pruebas suficientes y medibles | Pruebas adecuadas | Pruebas mínimas sin detalle | Sin plan verificable |
| Viabilidad del alcance | Proyecto pequeño, realista y ejecutable | Casi realista con ajustes menores | Riesgo de sobrealcance | No viable para el curso |

---

## 7) Instrucciones de entrega
1. Completa todos los documentos solicitados.
2. Verifica que tu propuesta sea consistente entre archivos.
3. Haz commit de tu avance final.
4. Entrega el enlace del repositorio de GitHub Classroom.

---

## 8) Recomendaciones finales del instructor
- Piensa primero en la **calidad de la documentación**, no en escribir mucho código.
- Si eliges ARM64 Assembly, reduce al máximo el alcance.
- Enfócate en un caso de uso sencillo pero bien explicado.
- Entre más clara sea tu planeación, más fácil será implementar en la siguiente etapa.

¡Éxito! La meta aquí es diseñar una propuesta sólida, pequeña y técnicamente bien pensada.
