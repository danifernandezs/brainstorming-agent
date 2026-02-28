# Brainstorming Planner Agent

Agente primario para OpenCode que facilita sesiones de brainstorming estructurado con metodologias 6-3-5 y Rolestorming.

## Caracteristicas

- **Dos metodologias**: 6-3-5 (Brainwriting) y Rolestorming
- **Loop iterativo**: Continua hasta que digas "basta"
- **Muchas preguntas**: Recopila todo el contexto necesario
- **Documentacion automatica**: Genera archivo .md con toda la sesion
- **Priorizacion**: Ayuda a identificar las mejores ideas
- **Creatividad alta**: Temperature 0.75 para ideas originales

## Instalacion

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
@brainstorm Necesito ideas para mejorar la retencion de usuarios
```

## Metodologias

### 6-3-5 (Brainwriting)

Tecnica de generacion de ideas en rondas:

- Generas 3 ideas iniciales
- Cada ronda construye sobre las anteriores
- Sin limite de tiempo
- Registra decisiones por ronda
- Continua hasta que quieras parar

Ideal para: Generar muchas ideas rapidamente, explorar variaciones.

### Rolestorming

Tecnica de perspectivas multiples:

- El agente adopta un rol/persona
- Anuncia el rol ANTES de cada ronda
- Genera ideas desde esa perspectiva
- Cambia de rol en cada iteracion
- Sintetiza todas las perspectivas al final

Roles tipicos: Usuario novato, experto, competidor, inversor, critico, etc.

Ideal para: Ver problemas desde angulos inesperados, empatizar con usuarios.

## Flujo de una Sesion

```
1. SETUP
   - Preguntas de contexto
   - Elegir metodologia (A o B)

2. EJECUCION
   - Rondas de ideas segun metodologia
   - Decisiones registradas por ronda

3. SINTESIS
   - Consolidar todas las ideas
   - Categorizar
   - Priorizar

4. DOCUMENTACION
   - Crear archivo brainstorm-[tema]-[fecha].md
   - Incluye: contexto, rondas, decisiones, priorizacion, proximos pasos

5. LOOP
   - Continuar iterando o cerrar sesion
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
- Categorizacion
- Top ideas priorizadas
- Conclusiones
- Proximos pasos accionables

## Ejemplo Rapido

```
USUARIO: @brainstorm Ideas para nombre de app de productividad

AGENTE: Hola! Vamos a encontrar el nombre perfecto.

Preguntas rapidas:
1. Que hace tu app?
2. Tono: serio o divertido?
3. Idioma preferido?

Metodologia?
A) 6-3-5 - Generar muchos nombres
B) Rolestorming - Ver desde perspectivas de usuarios

USUARIO: A, es gestor de tareas, tono minimalista, ingles

AGENTE: Perfecto! 6-3-5 con estilo minimalista.

RONDA 1 - Escribe 3 nombres:
1. ...
2. ...
3. ...
```

## Requisitos

- OpenCode instalado
- Proveedor configurado (Z.AI, Anthropic, etc.)

## Licencia

This work is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the [LICENSE](LICENSE.txt) file for more details.
