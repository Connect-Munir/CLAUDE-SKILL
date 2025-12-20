---
name: skill-maker
description: Generate well-structured skills for Claude Code with clear formatting including summary, key terms, questions, and easy-to-read layout. Use when creating new skills that follow best practices.
---

# Skill Maker

## Summary

The **Skill Maker** generates high-quality, consistent skills for Claude Code projects. Every skill created includes:
- Clear **summary** at the top explaining purpose and use cases
- **Key terms** highlighted to improve discoverability
- **Questions** at the end to guide user interactions
- Professional, **easy-to-read formatting** with proper Markdown structure

## When to Use This Skill

Use Skill Maker when you need to:
- Create a new Claude Code skill from scratch
- Ensure consistent skill structure across your project
- Generate skills that follow Claude Code best practices
- Create skills with built-in user guidance and examples

## Key Terms to Understand

- **Skill**: A reusable capability that Claude automatically invokes based on context
- **SKILL.md**: The required file containing YAML frontmatter and Markdown content
- **Allowed-tools**: Optional field restricting which Claude Code tools the skill can use
- **Skill Description**: Critical for discovery—include what it does and when to use it
- **Project Skills**: Stored in `.claude/skills/skill-name/` and shared via git

## Structure Template

Every skill created by Skill Maker follows this structure:

```
skill-name/
├── SKILL.md (required)
├── reference.md (optional: detailed documentation)
├── examples.md (optional: concrete usage examples)
└── scripts/ (optional: helper utilities)
```

## SKILL.md Format

```yaml
---
name: skill-name
description: What this skill does and when to use it (max 1024 chars)
allowed-tools: Tool1, Tool2, Tool3 (optional)
---

# Skill Name

## Summary
Brief 1-2 sentence overview of the skill's purpose.

## Key Terms
- **Term 1**: Definition
- **Term 2**: Definition
- **Term 3**: Definition

## When to Use This Skill
Explain specific scenarios and use cases.

## Instructions
Clear, step-by-step guidance for the skill.

## Examples
Concrete examples showing expected usage.

## Questions for You
- What problem are you trying to solve?
- Have you considered X approach?
- What's your success criteria?
```

## Instructions

To create a new skill:

1. **Define the skill's purpose** - What does it do? When should Claude use it?
2. **Choose a skill name** - Lowercase letters, numbers, hyphens only (max 64 chars)
3. **Write the summary** - 1-2 clear sentences explaining the skill
4. **Identify key terms** - 3-5 important concepts users should understand
5. **Create instructions** - Step-by-step guidance Claude will follow
6. **Add examples** - Show concrete usage patterns
7. **Write ending questions** - 2-3 questions to guide user interaction
8. **Format for readability** - Use Markdown headers, bold, lists, code blocks
9. **Place in .claude/skills/** - Store as `.claude/skills/skill-name/SKILL.md`
10. **Commit to git** - Make the skill available to your team

## Best Practices

✓ **Keep skills focused** - One skill = one specific capability
✓ **Write specific descriptions** - Include trigger words (PDF, Excel, database, etc.)
✓ **Use clear formatting** - Headers, bold terms, bullet points, code blocks
✓ **Provide examples** - Show real-world usage patterns
✓ **Test with your team** - Verify the skill activates when expected
✓ **Document optional tools** - Specify allowed-tools if restricting access

## Examples

### Example 1: PDF Processing Skill
```
Skill Name: pdf-processor
Description: Extract text, fill forms, and merge PDFs. Use for PDF document processing tasks.
Key Terms: PDF, extraction, form-filling, merging
Questions: What PDF operation do you need? What format should output be?
```

### Example 2: Data Analysis Skill
```
Skill Name: data-analyst
Description: Analyze CSV/Excel files and generate insights with charts. Use for data analysis and visualization.
Key Terms: CSV, spreadsheet, analysis, visualization
Questions: What data do you want analyzed? What insights are you looking for?
```

## Questions for You

- **What type of skills** do you want to create with Skill Maker?
- **Who is the audience** for these skills—your team, clients, or personal use?
- **What domains** will your skills cover (documentation, code review, data processing, etc.)?
