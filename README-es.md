# Brainstorming Planner Agent

[![Ver en GitHub](https://img.shields.io/badge/Ver%20en-GitHub-181717.svg?logo=github)](https://github.com/danifernandezs/brainstorming-agent)
![Licencia](https://img.shields.io/badge/licencia-CC%20BY--SA%204.0-1CA340.svg)
![Versión](https://img.shields.io/badge/versión-1.0.0-1CA340.svg)
![OpenCode](https://img.shields.io/badge/OpenCode-agent-1CA340.svg)

[English](README.md) | [Español](README-es.md)

Agente primario para OpenCode que facilita sesiones de brainstorming estructurado con metodologías 6-3-5 y Rolestorming.

## Características

- **Dos metodologías**: 6-3-5 (Brainwriting) y Rolestorming
- **Loop iterativo**: Continúa hasta que digas "basta"
- **Muchas preguntas**: Recopila todo el contexto necesario
- **Documentación automática**: Genera archivo .md con toda la sesión
- **Priorización**: Ayuda a identificar las mejores ideas
- **Creatividad alta**: Temperature 0.75 para ideas originales

## Instalación

### Global (recomendado)

```bash
mkdir -p ~/.config/opencode/agents
cp brainstorm.md ~/.config/opencode/agents/
```

### Por proyecto

```bash
mkdir -p .opencode/agents
cp brainstorm.md .opencode/agents/
```

## Uso

En OpenCode:

1. Presiona `Tab` para cambiar de agente
2. Selecciona "brainstorm"
3. Escribe tu tema o problema

O invoca directamente:

```
@brainstorm Necesito ideas para mejorar la retención de usuarios
```

## Metodologías

### 6-3-5 (Brainwriting)

Técnica de generación de ideas en rondas:

- Generas 3 ideas iniciales
- Cada ronda construye sobre las anteriores
- Sin límite de tiempo
- Registra decisiones por ronda
- Continúa hasta que quieras parar

Ideal para: Generar muchas ideas rápidamente, explorar variaciones.

### Rolestorming

Técnica de perspectivas múltiples:

- El agente adopta un rol/persona
- Anuncia el rol ANTES de cada ronda
- Genera ideas desde esa perspectiva
- Cambia de rol en cada iteración
- Sintetiza todas las perspectivas al final

Roles típicos: Usuario novato, experto, competidor, inversor, crítico, etc.

Ideal para: Ver problemas desde ángulos inesperados, empatizar con usuarios.

## Flujo de una Sesión

```
1. SETUP
   - Preguntas de contexto
   - Elegir metodología (A o B)

2. EJECUCIÓN
   - Rondas de ideas según metodología
   - Decisiones registradas por ronda

3. SÍNTESIS
   - Consolidar todas las ideas
   - Categorizar
   - Priorizar

4. DOCUMENTACIÓN
   - Crear archivo brainstorm-[tema]-[fecha].md
   - Incluye: contexto, rondas, decisiones, priorización, próximos pasos

5. LOOP
   - Continuar iterando o cerrar sesión
```

## Output

Cada sesion genera un archivo markdown:

```
brainstorm-[tema-slug]-YYYYMMDD.md
```

Contenido:
- Contexto y preguntas
- Todas las rondas con decisiones
- Lista completa de ideas
- Categorización
- Top ideas priorizadas
- Conclusiones
- Próximos pasos accionables

## Ejemplo Rápido

```
USUARIO: @brainstorm Ideas para nombre de app de productividad

AGENTE: Hola! Vamos a encontrar el nombre perfecto.

Preguntas rápidas:
1. Qué hace tu app?
2. Tono: serio o divertido?
3. Idioma preferido?

Metodología?
A) 6-3-5 - Generar muchos nombres
B) Rolestorming - Ver desde perspectivas de usuarios

USUARIO: A, es gestor de tareas, tono minimalista, inglés

AGENTE: Perfecto! 6-3-5 con estilo minimalista.

RONDA 1 - Escribe 3 nombres:
1. ...
2. ...
3. ...
```

## Requisitos

- OpenCode instalado
- Proveedor configurado (Z.AI, Anthropic, etc.)

## Contribuir

Las contribuciones son bienvenidas.

## Licencia

This work is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

Please read the [LICENSE](LICENSE.txt) file for more details.
