# Brainstorming Planner Agent

A primary agent for OpenCode that facilitates structured brainstorming sessions using 6-3-5 and Rolestorming methodologies.

## Features

- **Two methodologies**: 6-3-5 (Brainwriting) and Rolestorming
- **Iterative loop**: Continues until you say "stop"
- **Thorough questioning**: Gathers all necessary context
- **Automatic documentation**: Generates .md file with full session
- **Prioritization**: Helps identify the best ideas
- **High creativity**: Temperature 0.75 for original ideas

## Installation

### Global (recommended)

```bash
mkdir -p ~/.config/opencode/agents
cp brainstorm.md ~/.config/opencode/agents/
```

### Per-project

```bash
mkdir -p .opencode/agents
cp brainstorm.md .opencode/agents/
```

## Usage

In OpenCode:

1. Press `Tab` to switch agents
2. Select "brainstorm"
3. Type your topic or problem

Or invoke directly:

```
@brainstorm I need ideas to improve user retention
```

## Methodologies

### 6-3-5 (Brainwriting)

Idea generation technique in rounds:

- You generate 3 initial ideas
- Each round builds on previous ones
- No time limit
- Records decisions per round
- Continues until you want to stop

Best for: Generating many ideas quickly, exploring variations.

### Rolestorming

Multiple perspectives technique:

- The agent adopts a role/persona
- Announces the role BEFORE each round
- Generates ideas from that perspective
- Changes role in each iteration
- Synthesizes all perspectives at the end

Typical roles: Novice user, expert, competitor, investor, critic, etc.

Best for: Seeing problems from unexpected angles, empathizing with users.

## Session Flow

```
1. SETUP
   - Context questions
   - Choose methodology (A or B)

2. EXECUTION
   - Idea rounds according to methodology
   - Decisions recorded per round

3. SYNTHESIS
   - Consolidate all ideas
   - Categorize
   - Prioritize

4. DOCUMENTATION
   - Create brainstorm-[topic]-[date].md file
   - Includes: context, rounds, decisions, prioritization, next steps

5. LOOP
   - Continue iterating or close session
```

## Output

Each session generates a markdown file:

```
brainstorm-[topic-slug]-YYYYMMDD.md
```

Contents:
- Context and questions
- All rounds with decisions
- Complete list of ideas
- Categorization
- Top prioritized ideas
- Conclusions
- Actionable next steps

## Quick Example

```
USER: @brainstorm Ideas for productivity app name

AGENT: Hi! Let's find the perfect name.

Quick questions:
1. What does your app do?
2. Tone: serious or fun?
3. Preferred language?

Methodology?
A) 6-3-5 - Generate many names
B) Rolestorming - See from user perspectives

USER: A, it's a task manager, minimalist tone, English

AGENT: Perfect! 6-3-5 with minimalist style.

ROUND 1 - Write 3 names:
1. ...
2. ...
3. ...
```

## Requirements

- OpenCode installed
- Configured provider (Z.AI, Anthropic, etc.)

## License

This work is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the [LICENSE](LICENSE.txt) file for more details.
