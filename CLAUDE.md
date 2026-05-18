# CLAUDE CONNECTIONS

## Figma Integration

When generating or pushing designs to Figma, always read `figma.config.json` for the default target.

### Default Target
- **File**: CLAUDE CONNECTIONS
- **File Key**: `VW53sCUGUKG1lhJQp7zOGK`
- **File URL**: https://www.figma.com/design/VW53sCUGUKG1lhJQp7zOGK
- **Page**: `From Code`
- **Frame naming**: Auto-named by component (e.g., a `Button` component generates a frame named `Button`)

### Workflow for Code → Figma
1. Read `figma.config.json` to get the target file key and page name.
2. Switch to the `From Code` page in Figma before creating any frames.
3. Name each output frame after the component or screen being generated.
4. Position new frames to the right of existing content (never at 0,0 if content exists).
5. Use `use_figma` (Plugin API) for all write operations.

### Rules
- Always push to the `From Code` page unless the user explicitly specifies otherwise.
- Never overwrite existing frames — always create new ones or ask before replacing.
- Return all created node IDs after each `use_figma` call.
