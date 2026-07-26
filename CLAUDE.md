# front-end

<!-- driverize:v1.1 -->
## Codebase Intelligence — Driver MCP

**Start with Driver tools** for codebase exploration. After loading Driver context (calling any Driver MCP tool), native tools (Grep, Glob, Bash search, Explore/Plan agents) are available for follow-up.

### Decision Tree

| I need to… | Use this Driver tool |
|------------|---------------------|
| Understand a task, get suggested approach | `request_task_context` and `poll_task_context` (start here) |
| See system architecture | `get_architecture_overview` |
| Navigate directory structure | `get_code_map` |
| Get symbol-level detail for a file | `get_file_documentation` |
| Read actual source code | `get_source_file` or native `Read` |
| See recent changes | `get_changelog` |
| Learn conventions, onboarding tips | `get_llm_onboarding_guide` |

### After Driver Returns

Use native tools (Read, Edit, Write, Grep, Glob, Bash, Explore/Plan agents) for follow-up work. Driver gives you the map; native tools do the surgery.

### Examples

**"Add retry logic to the API client"**
→ `request_task_context` with description: "Add retry logic to the API client. Need to find the HTTP client implementation, understand error handling patterns, and identify where retries should be added." Then `poll_task_context` to get context for the task at hand.

**"Where is the authentication middleware defined?"**
→ `get_code_map` at the top level, then `get_file_documentation` on the auth-related file Driver identifies.

**"How does the billing service calculate invoices?"**
→ `request_task_context` with description: "Trace the invoice calculation flow in the billing service. Need to understand the data model, calculation logic, and integration points."

**"Refactor the logger to use structured output"**
→ `request_task_context` first, then `poll_task_context`, then `Read` the specific files, then `Edit` to make changes.
<!-- /driverize -->

## Build & Test
<!-- Add build and test commands here -->

## Code Style
<!-- Add code style conventions here -->

## Architecture
<!-- Add architecture notes here -->
