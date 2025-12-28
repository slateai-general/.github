# SlateAI

**Leveraging AI as a tool, not a crutch.**

SlateAI is an evolving project focused on building practical, understandable AI-powered solutions. We believe in using AI intentionally—as a tool to augment human capability, not as something to blindly rely on without understanding.

---

## Philosophy

AI is powerful, but it's not magic. Our approach:

- **Understand what you're building** — Don't use AI just because you can
- **AI as augmentation** — Enhance human decision-making, don't replace it
- **Transparency over black boxes** — Know how and why your tools work
- **Practical over hype** — Solve real problems, skip the buzzwords

---

## Tech Stack

### Core Technologies

| Layer | Technologies |
|-------|-------------|
| **Runtime** | [Bun](https://bun.sh) |
| **Language** | TypeScript |
| **API Framework** | [Hono](https://hono.dev) |
| **Frontend** | [Next.js](https://nextjs.org) |
| **Database** | PostgreSQL via [Supabase](https://supabase.com) |
| **Validation** | [Zod](https://zod.dev) |
| **AI/ML** | [Anthropic](https://www.anthropic.com), [OpenAI](https://openai.com), [LangChain](https://www.langchain.com) |

### Infrastructure

- **Hosting**: Railway (production), Internal (development)
- **CRM**: Attio
- **Project Management**: Linear & Notion
- **Version Control**: GitHub

---

## Packages

All SlateAI packages are published under the `@slateai-general` scope on npm.

| Package | Description |
|---------|-------------|
| `@slateai-general/types` | Common TypeScript type definitions |
| `@slateai-general/constants` | Shared constants throughout |
| `@slateai-general/utils` | Shared utilities |
| `@slateai-general/cache` | Helpers and details for cacheing |
| `@slateai-general/errors` | Error information and builders |
| `@slateai-general/logger` | Consistant logger for projects |
| `@slateai-general/validation` | Validation helpers, information, and common schemas |
| `@slateai-general/hono-middleware` | Commonly used custom middleware throughout Hono APIs |
| `@slateai-general/drizzle-utils` | Utilities for drizzle internally |
| `@slateai-general/cli` | Project scaffolding and management CLI |

---

## Organization Structure

```
slateai-general/           # SlateAI organization housing all repos
├── sai-general/           # '@slateai-general' | All SlateAI packages (internal)
├── slateai-api/           # Backend API (Bun + Hono)
├── slateai-main-siite/    # Main SlateAI web application (Next.js)
├── slateai-cli/           # Project management CLI (internal)
└── templates/             # Project scaffolding templates
```

### Key Projects

**`slateai-api`** — Central API for project management, authentication, and data synchronization. Built with Bun and Hono for performance and simplicity.

**`slateai-cli`** — Command-line tool for scaffolding new projects, managing configurations, and syncing with the central registry. Install globally with `bun add -g @slateai-general/cli`.

**`slateai-templates`** — Collection of project templates for rapid development:
- `nextjs` — Next.js frontend applications
- `api` — Bun + Hono API services
- `general` — General TypeScript projects

---

## Project Configuration

SlateAI projects use a `saiconfig.json` file for centralized management:

```json
{
  "uuid": "generated-uuid",
  "name": "project-name",
  "description": "Project description",
  "version": "0.1.0",
  "type": "client | internal",
  "status": "active | archived | paused",
  "template": {
    "name": "template-name",
    "version": "1.0.0"
  }
}
```

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    SlateAI Ecosystem                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Templates Repository                                       │
│     └─ Project scaffolding and boilerplates                │
│                                                             │
│  CLI Tool (@slateai-general/cli)                           │
│     ├─ Creates projects from templates                     │
│     ├─ Validates & manages configuration                   │
│     ├─ Syncs with central API                              │
│     └─ Auto-commits to git                                 │
│                                                             │
│  SlateAI API (Bun + Hono)                                  │
│     ├─ Authentication middleware                           │
│     ├─ Project management endpoints                        │
│     ├─ Template listing                                    │
│     └─ Validation logic                                    │
│                                                             │
│  PostgreSQL Database                                        │
│     ├─ api_keys                                            │
│     ├─ projects                                            │
│     └─ sync_history                                        │
│                                                             │
│  Web Application (Next.js)                                  │
│     └─ Project overview and management UI                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Development

### Prerequisites

- [Bun](https://bun.sh) v1.0+
- PostgreSQL 15+
- Node.js 20+ (for some tooling)

### Getting Started

```bash
# Clone a repository
git clone https://github.com/slateai-general/<repo-name>

# Install dependencies
bun install

# Set up environment
cp .env.example .env

# Run development server
bun dev
```

### CLI Usage

```bash
# Install the CLI globally
bun add -g @slateai-general/cli

# Create a new project
slateai create nextjs my-project

# Initialize existing project
slateai init

# Sync project with registry
slateai sync

# List all projects
slateai list
```

---

## Design Philosophy

- **Intentional** — Every tool and technology choice has a reason
- **Right-Sized** — Appropriate complexity for the problem at hand
- **Clean Architecture** — Warm minimalism inspired by Supabase, Linear, and Anthropic
- **Developer Experience** — Fast iteration, clear patterns, minimal friction

---

## Contact

- **Email**: [support@slateai.org](mailto:support@slateai.org)
- **Contact**: [www.slateai.org](https://www.slateai.org/contact)
- **GitHub**: [@slateai-general](https://github.com/slateai-general)

---

## Further

- **Website**: [support@slateai.org](mailto:support@slateai.org)
- **API**: [api.slateai.org](https://api.slateai.org)
- **Documentation**: [docs.slateai.org](https://docs.slateai.org)
- **API Reference**: [docs.slateai.org/api](https://docs.slateai.org/api)

---

<sub>© 2024 SlateAI. All rights reserved.</sub>
