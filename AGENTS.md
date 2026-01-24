# Subagent Coordination Guide

This project uses Cursor 2.4+ subagents for specialized product building. Each agent handles a specific domain and can be invoked explicitly or automatically based on task complexity.

## Available Agents

### 1. UI Designer (`@ui-designer`)
**When to use:**
- Complex layouts and responsive design
- Animations and transitions
- Design system and theming
- Accessibility requirements
- Component styling and polish

**Key patterns:**
- Tailwind CSS utility-first approach
- shadcn/ui component library
- Mobile-first responsive design
- Dark mode support

**Example invocation:**
```
Use @ui-designer to create a responsive dashboard layout with dark mode support
```

---

### 2. Schema Architect (`@schema-architect`)
**When to use:**
- Database schema design
- Multi-tenant architecture
- Complex relationships
- Query optimization
- Database migrations

**Key patterns:**
- Prisma schema with proper indexes
- Referential integrity
- Migration strategy
- Query optimization with includes/selects

**Example invocation:**
```
Use @schema-architect to design a multi-tenant SaaS database with orgs, teams, and permissions
```

---

### 3. API Builder (`@api-builder`)
**When to use:**
- REST API endpoint design
- Request validation (Zod schemas)
- Error handling strategies
- Authentication/authorization
- Rate limiting and security

**Key patterns:**
- Structured API responses (success/error format)
- Zod validation schemas
- Error codes and status codes
- Middleware patterns
- Server actions for forms

**Example invocation:**
```
Use @api-builder to create CRUD endpoints with proper validation and error handling
```

---

### 4. Test Writer (`@test-writer`)
**When to use:**
- Unit test coverage
- Component test coverage
- Integration test coverage
- E2E test coverage
- Test organization and patterns

**Key patterns:**
- Vitest for unit/integration tests
- React Testing Library for components
- Playwright for E2E tests
- Mocking and fixtures
- Test utilities and helpers

**Example invocation:**
```
Use @test-writer to add comprehensive test coverage for the auth flow
```

---

## Implicit Agent Activation

Agents are automatically invoked based on task complexity and requirements:

| Scenario | Agents Involved |
|----------|-----------------|
| Build a simple landing page | UI Designer |
| Build a product with auth, DB, and API | All four agents |
| Add a database feature | Schema Architect + API Builder |
| Complex UI with animations | UI Designer |
| Add test coverage | Test Writer |
| Fix a bug in database logic | Schema Architect + Test Writer |

---

## Workflow: Building a Complete Feature

### 1. Feature Request
```
Build a notes app where users can create, edit, and delete notes organized by tags.
Include auth, real-time collab, and dark mode.
```

### 2. Agents Coordinate

**Schema Architect** designs the database:
- User, Note, Tag models
- Many-to-many relationships
- Indexes for queries

**API Builder** creates endpoints:
- POST /api/notes (create)
- GET /api/notes (list with pagination)
- PATCH /api/notes/[id] (edit)
- DELETE /api/notes/[id] (delete)

**UI Designer** builds components:
- Notes list with filtering by tag
- Note editor with rich text
- Tag selector component
- Dark mode support

**Test Writer** adds coverage:
- API integration tests
- Component tests
- E2E test for create → edit → delete workflow

---

## Best Practices

1. **Be explicit when unclear** - Use `@agent-name` syntax to invoke specific agents
2. **Let coordination happen** - For large features, let agents work in parallel
3. **Reference patterns** - Agents include code patterns; follow them consistently
4. **Test-first when complex** - Use Test Writer for critical flows
5. **Verify output** - Review agent work before integration

---

## Usage Examples

### Simple Feature Request (Implicit)
```
Build a contact form with email validation and Tailwind styling
```
→ UI Designer handles it

### Complex Feature (Explicit)
```
@schema-architect design a collaborative document editing database
@api-builder create the API for real-time updates
@ui-designer build the editor UI
@test-writer add tests for concurrent edits
```

### Fixing a Bug (Explicit)
```
There's a bug where posts don't show for team members. 
@schema-architect review the query pattern
@test-writer add a test case for multi-user access
```

---

## Agent Output Format

Agents follow consistent patterns in their output:

- **Code**: Production-ready, not toy examples
- **Typing**: Full TypeScript with no `any` types
- **Testing**: Critical paths have tests
- **Security**: Input validation, auth checks, error handling
- **Performance**: Proper indexes, query optimization, pagination

---

## Extending the System

To add a new specialized agent:

1. Create `.cursor/agents/my-specialist.md`
2. Define expertise and patterns
3. Add to this coordination guide
4. Reference in feature requests: `@my-specialist`

See `.cursor/rules/imagine-builder.mdc` for the core philosophy.
