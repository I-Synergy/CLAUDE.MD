# GitHub Copilot Instructions

You are assisting with a .NET project following Clean Architecture, CQRS, and DDD patterns.

## Code Standards

**Critical Rules:**
- See `.claude/reference/critical-rules.md` for non-negotiable patterns
- Commands use individual parameters (NOT model objects)
- Use DataContext extension methods (NOT repository interfaces)
- Delete operations: `RemoveItemAsync<TEntity, TKey>()` NOT `DeleteItemByIdAsync`
- Mapster for mapping (NOT AutoMapper)
- Async all the way (NO `.Wait()` or `.Result`)

**Forbidden Technologies:**
- See `.claude/reference/forbidden-tech.md`
- NO MediatR → Use I-Synergy.Framework.CQRS
- NO AutoMapper → Use Mapster
- NO xUnit/NUnit → Use MSTest
- NO FluentValidation → Use DataAnnotations

**Architecture:**
- Domain: `{ApplicationName}.Domain.*` - CQRS, entities
- Application: `{ApplicationName}.Services.*` - API endpoints
- Infrastructure: `{ApplicationName}.Data.*` - Persistence
- Presentation: `{ApplicationName}.UI.*` - Blazor/MAUI

**Patterns:**
- CQRS: `.claude/patterns/cqrs-patterns.md`
- API: `.claude/patterns/api-patterns.md`
- Testing: `.claude/patterns/testing-patterns.md`

**Naming:**
- Commands: `{Action}{Entity}Command` → `CreateBudgetCommand`
- Queries: `Get{Entity}{Criteria}Query` → `GetBudgetByIdQuery`
- Handlers: `{CommandOrQuery}Handler` → `CreateBudgetHandler`

**Templates:**
Refer to `.claude/reference/templates/` for copy-paste patterns:
- `command-handler.cs.txt`
- `query-handler.cs.txt`
- `endpoint.cs.txt`
- `mapping-config.cs.txt`

**Testing:**
- MSTest + Moq + Reqnroll
- Unit tests for handlers
- Integration tests for endpoints
- Gherkin for complex flows

## Token Replacements

Replace throughout codebase:
- `{ApplicationName}` - Your application name
- `{Domain}` - Domain/bounded context
- `{Entity}` - Entity name (PascalCase)

For complete definitions: `.claude/reference/tokens.md`

## Code Generation

When generating code:
1. Follow vertical slice organization
2. Include XML documentation
3. Use proper namespacing
4. Apply SOLID principles
5. Validate inputs with guard clauses
6. Use structured logging
7. Handle errors appropriately
