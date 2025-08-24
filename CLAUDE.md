# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a general workspace that uses the BMAD-METHOD (v5.1.3) for structured project management and development workflows. The repository contains example projects demonstrating different use cases and methodologies.

## BMAD-METHOD Integration

This project has BMAD-METHOD installed and configured for Claude Code IDE integration. The BMAD system provides:

- **Agent-driven workflows**: Structured planning and execution workflows for both greenfield and brownfield projects
- **Document templates**: PRD, architecture, story, and testing templates in `.bmad-core/templates/`
- **Task automation**: Predefined tasks for requirements elicitation, story creation, QA gates, and documentation
- **Agent personas**: Specialized agents (PM, PO, Architect, Dev, QA, UX Expert, Analyst) in `.bmad-core/agents/`

### Key BMAD Commands

The BMAD system is accessible through slash commands prefixed with "BMad":
- Use BMad tasks for structured project planning and execution
- Refer to `.bmad-core/user-guide.md` for complete workflow documentation
- Check `.bmad-core/core-config.yaml` for current configuration

### Document Structure

When working with BMAD projects:
- **PRD files**: Located in `docs/prd/` (sharded) or `docs/prd.md`
- **Architecture docs**: Located in `docs/architecture/` (sharded) or `docs/architecture.md`
- **Stories**: Located in `docs/stories/`
- **Epic patterns**: Follow `epic-{n}*.md` naming convention

## Project Examples

The workspace contains several example projects:

### airbnbPricingAnalysis/
Contains market research and pricing analysis documentation demonstrating business analysis workflows.

### domainExpertForEngineering/
Directory for domain expertise content related to engineering practices.

### learningCaptureAndDocument/
Directory for capturing and documenting learning materials and knowledge.

### reference-guides/
Contains troubleshooting guides and reference materials:
- **npm-claude-code-fix-guide.md** - Solutions for npm ENOTEMPTY errors when installing Claude Code globally

## Configuration

- **Claude Code settings**: Custom permissions configured in `.claude/settings.local.json` with pre-approved access to WebSearch, process management commands, and GitHub domain fetches
- **BMAD configuration**: Core settings in `.bmad-core/core-config.yaml` with document sharding enabled, PRD/architecture versioning (v4), and story location configured

## Development Approach

This workspace emphasizes:
1. Structured planning using BMAD workflows before development
2. Documentation-driven development with PRD and architecture alignment
3. Agent-based task execution for consistent quality
4. Iterative refinement through PO checklists and QA gates

## Working with BMAD

For new projects:
1. Use the planning workflow (Analyst → PM → Architect → PO cycle)
2. Create structured documents using BMAD templates
3. Follow the agent-driven execution workflow
4. Use BMad slash commands for task automation

For existing projects:
- Refer to `.bmad-core/working-in-the-brownfield.md` for brownfield approaches
- Use BMAD tasks to incrementally improve project structure

## Architecture Notes

This workspace follows a documentation-centric approach with no traditional build/test/lint commands. The primary workflow involves:

1. **Planning Phase**: Use BMAD agents and workflows for structured planning
2. **Execution Phase**: Document-driven development with story-based implementation
3. **Quality Assurance**: PO checklists and QA gates for validation

The system includes specialized agent personas (PM, PO, Architect, Dev, QA, UX Expert, Analyst) that can be invoked through BMad slash commands to maintain consistency across planning and execution phases.