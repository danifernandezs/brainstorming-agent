# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-07-17

### Added
- **Brainstorming Planner Agent** with two structured methodologies
  - 6-3-5 (Brainwriting): Iterative rounds building on previous ideas
  - Rolestorming: Multi-perspective idea generation through role adoption
- Complete workflow with 5 phases: Setup, Execution, Synthesis, Documentation, Iterative Loop
- Automatic session documentation in markdown format
- Built-in prioritization methods (voting, impact/effort matrix, custom criteria)
- Context-aware questioning system
- Iterative refinement loop until user decides to stop
- CC BY-SA 4.0 license
- Badges for license, version, OpenCode, and GitHub repository link
- Cross-language navigation between English and Spanish documentation
- Contributing section in both languages

### Changed
- Migrated deprecated `tools:` field to `permission:` per OpenCode docs best practices
- Fixed `edit` permission from `deny` to `ask` to allow documentation file creation
- Updated repository metadata: description, topics, and HTTPS homepage URL

### Documentation
- `README.md` - Full documentation in US English
- `README-es.md` - Spanish documentation preserved
- `brainstorm.md` - Agent configuration in US English

### Features
- Temperature: 0.75 for creative, original ideas
- Permission-based tool access: read, glob, grep, question, edit (ask), bash (ask), webfetch (ask), task (allow)
- Safe permissions: destructive bash commands require approval, file edits require approval
- Color theme: #1CA340

[1.0.0]: https://github.com/danifernandezs/brainstorming-agent/releases/tag/v1.0.0
