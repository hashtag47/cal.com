*apps/ --> Interactive with users, provide UI visual operations to display relative modules, executable applications as entry point, (Next.js frontend, REST API, etc.)

*packages/ --> Main logics underneath the application, shared libraries and business modules used by apps
|
 --> packages/prisma/: dealing with different databases, agency to simplify building with data  
|
 --> packages/features/*: vertical slice for different business modules(（booking, availability, notifications...)
|
 --> packages/ui, packages/lib: Shared components, utility functions, hooks, etc.

 *tests/ --> E2E and integration tests (Playwright, Jest, etc.)

 *scripts/ --> Dev/build/seed helper scripts “Maintenance tools”

 *deployes/ --> Docker, Helm, or deployment configs “Blueprints for production”

 *Root configs (turbo.json, packages.json...) --> Define how the monorepo builds and runs “Traffic rules”
  |
   --> packages.json defines workspace-wide dev tooling (TypeScript version, lint, test scripts, etc.)
  |
   --> turbo.json defines the build pipeline for the monorepo. Turborepo decides what to build first, what depends on what, and how to           cache results.
  
