# Conductor Plugin for Claude Code

**Measure twice, code once.**

Conductor turns Claude Code into a proactive project manager using **Context-Driven Development**. It ensures every feature follows a consistent lifecycle: **Context → Spec & Plan → Implement**.

## 🚀 Quick Start

```bash
# Add the marketplace
claude plugin marketplace add unvoidf/claude-code-conductor

# Install the plugin
claude plugin install conductor@conductor-marketplace

# Update the plugin
claude plugin update conductor@conductor-marketplace
```

## Workflow

Conductor manages the entire lifecycle of your tasks:

### 1. Setup (Run Once)
Defines your product goals, tech stack, and workflow preferences.
```bash
/conductor:setup
```

### 2. New Track
Starts a feature or bug fix. Generates a strict **Spec** and **Plan** before writing code.
```bash
/conductor:newTrack "Add generic dark mode toggle"
```

### 3. Implement
Executes the plan step-by-step, verifying each task.
```bash
/conductor:implement
```

## 📚 Command Reference

| Command | Description | Artifacts |
| :--- | :--- | :--- |
| `/conductor:setup` | Initialize project context & guidelines. | `conductor/product.md`, `tech-stack.md`, `workflow.md` |
| `/conductor:newTrack` | Create a new Spec & Plan. | `conductor/tracks/<id>/spec.md` & `plan.md` |
| `/conductor:implement` | Execute the current plan. | Updates `plan.md` & `tracks.md` |
| `/conductor:status` | Check project progress. | Reads `conductor/tracks.md` |
| `/conductor:revert` | Smart revert for tracks/phases. | Reverts git history |
| `/conductor:review` | Review work against guidelines. | Reads `product-guidelines.md` |

## License
Apache License 2.0
