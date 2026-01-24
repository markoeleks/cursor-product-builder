# Cursor Product Builder

> Turn Cursor into a full-stack AI product builder. Describe what you want, get working code.

Inspired by [imagine.dev](https://imagine.dev) - build real products through conversation, not prototypes.

[![Cursor 2.4+](https://img.shields.io/badge/Cursor-2.4%2B-blue)](https://cursor.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## What This Does

Instead of:
```
User: Build me a dashboard
Cursor: What framework? What features? What styling?
```

You get:
```
User: Build me a dashboard
Cursor: [Generates complete Next.js app with auth, database, API routes, and UI]
```

## Features

- **Ship immediately** - Working code, not explanations
- **Full-stack defaults** - Auth, database, APIs included automatically
- **Parallel subagents** - UI, schema, API, and test specialists (Cursor 2.4)
- **Image generation** - Mockups and assets on demand
- **Modern stack** - Next.js 14, TypeScript, Tailwind, Prisma, shadcn/ui

## Quick Start

```bash
# Clone to your project
git clone https://github.com/oleg-koval/cursor-product-builder.git
cd cursor-product-builder

# Copy to existing project (alternative)
cp -r .cursor/ your-project/.cursor/
cp AGENTS.md your-project/
```

Open in Cursor 2.4+ and start prompting.

## Structure

```
.cursor/
├── rules/
│   └── imagine-builder.mdc    # Core behavior - "build, don't ask"
└── agents/
    ├── ui-designer.md         # Tailwind, shadcn, animations
    ├── schema-architect.md    # Prisma, indexes, relations
    ├── api-builder.md         # Routes, validation, auth
    └── test-writer.md         # Vitest, RTL, Playwright
AGENTS.md                      # Subagent coordination
EXAMPLES.md                    # Ready-to-use prompts
```

## Examples

**SaaS Dashboard**
```
Build a SaaS analytics dashboard with user auth, org management, and charts.
```

**Landing Page**
```
Create a landing page for a fitness app with pricing and email signup.
```

**Internal Tool**
```
Build an inventory system with barcode scanning and low stock alerts.
```

See [EXAMPLES.md](EXAMPLES.md) for more prompts.

## Subagents (Cursor 2.4+)

Specialized agents run in parallel for complex tasks:

| Agent | Triggers On |
|-------|-------------|
| `@ui-designer` | Complex layouts, animations, theming |
| `@schema-architect` | Database design, migrations |
| `@api-builder` | REST endpoints, validation |
| `@test-writer` | Unit, component, E2E tests |

Explicit invocation:
```
Use @schema-architect to design a multi-tenant database
```

## Customization

**Change tech stack** - Edit `.cursor/rules/imagine-builder.mdc`:
```yaml
## Tech Stack Defaults
- **Frontend**: Vue 3 + Nuxt
- **Database**: Drizzle ORM
```

**Add subagents** - Create `.cursor/agents/my-specialist.md`

**Modify patterns** - Edit any agent file to change code patterns

## Default Stack

| Layer | Technology |
|-------|------------|
| Framework | Next.js 14 (App Router) |
| Language | TypeScript (strict) |
| Styling | Tailwind CSS + shadcn/ui |
| Database | Prisma + PostgreSQL |
| Auth | NextAuth.js |
| Validation | Zod |
| State | React Query + Zustand |

## Contributing

PRs welcome:
- New subagent specialists
- Alternative tech stack presets
- Improved patterns

## License

MIT
