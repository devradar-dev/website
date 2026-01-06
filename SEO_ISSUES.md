# SEO Issues - GitHub Issue Templates

Copy these contents to create GitHub Issues on https://github.com/devradar-dev/website/issues

Each issue creates a backlink to devradar.dev and gets indexed by Google.

---

## Issue 1: Next.js 15 + Prisma 6 Compatibility

**Title:** `Next.js 15 + Prisma 6 - Full Compatibility Report`

**Labels:** `compatibility`, `nextjs`, `prisma`, `featured`

**Body:**
```markdown
## Next.js 15 + Prisma 6 Compatibility Report

### Status: ✅ Compatible

Next.js 15 works seamlessly with Prisma 6. This is one of the most popular combinations for full-stack TypeScript applications.

### Key Points

- **Server Actions:** Full support in Next.js 15 with Prisma 6
- **App Router:** No issues with Server Components
- **Edge Runtime:** Prisma doesn't support Edge (use Neon or Supabase Edge instead)
- **Type Safety:** Excellent TypeScript integration

### Known Considerations

- Prisma Client requires Node.js runtime (not Edge compatible)
- Use `next/cache` for revalidation strategy
- Consider connection pooling for serverless deployments

### Full Report

Read the complete compatibility analysis with workarounds and examples:
**[devradar.dev/check/nextjs-prisma](https://devradar.dev/check/nextjs-prisma)**

### Related Checks

- [Next.js + MongoDB](https://devradar.dev/check/nextjs-mongodb)
- [Next.js + Supabase](https://devradar.dev/check/nextjs-supabase)
- [Prisma + Vercel](https://devradar.dev/check/prisma-vercel)

---

*Data sourced from official documentation, GitHub issues, and community reports.*
```

---

## Issue 2: Lovable AI - Complete Review

**Title:** `Lovable AI - Full Review & Capabilities`

**Labels:** `ai-tool`, `vibe-coding`, `featured`, `review`

**Body:**
```markdown
## Lovable AI - Complete Tool Review

### Category: Vibe Coding (Prompt-to-App)

**[devradar.dev/tools/lovable](https://devradar.dev/tools/lovable)**

### Overview

Lovable is an AI-powered app builder that transforms natural language prompts into production-ready applications. It's one of the leading tools in the "vibe coding" category.

### Key Features

| Feature | Status |
|---------|--------|
| React Support | ✅ Full |
| Next.js Support | ✅ Full |
| Supabase Integration | ✅ Native |
| Tailwind CSS | ✅ Native |
| Deployment | ✅ One-click |
| GitHub Export | ✅ Available |

### Best For

- Rapid prototyping and MVPs
- Internal tools and dashboards
- Marketing landing pages
- SaaS starters

### Limitations

- Limited customization for complex logic
- Best for standard CRUD applications
- Learning curve for prompt engineering

### Comparison

See how Lovable compares to other AI tools:
- **[Lovable vs Bolt.new](https://devradar.dev/tools)** - Side by side comparison
- **[Lovable vs v0.dev](https://devradar.dev/tools)** - UI generator comparison
- **[Lovable vs Cursor](https://devradar.dev/tools)** - Different approaches

### Full Review

Read the complete analysis with capabilities, pricing, and use cases:
**[devradar.dev/tools/lovable](https://devradar.dev/tools/lovable)**

---

*Last updated: January 2025*
```

---

## Issue 3: Supabase + Vercel Edge Compatibility

**Title:** `Supabase + Vercel Edge Functions - Compatibility Report`

**Labels:** `compatibility`, `supabase`, `vercel`, `edge`, `featured`

**Body:**
```markdown
## Supabase + Vercel Edge Compatibility

### Status: ✅ Compatible (with caveats)

Supabase works with Vercel, but there are important considerations for Edge Functions.

### What Works

| Feature | Edge Runtime | Node Runtime |
|---------|-------------|--------------|
| Auth (JS client) | ❌ Use `@supabase/ssr` | ✅ Yes |
| Database (Direct) | ❌ No | ✅ Yes |
| Database (Edge Function) | ✅ Yes | ✅ Yes |
| Storage | ✅ Yes | ✅ Yes |
| Realtime | ✅ Yes | ✅ Yes |

### Key Recommendations

1. **For Server Components:** Use `@supabase/ssr` package
2. **For Edge Functions:** Create Supabase client per request
3. **For Route Handlers:** Use standard Supabase JS client

### Code Example

```typescript
// Edge Function with Supabase
import { createClient } from '@supabase/supabase-js'

export const config = { runtime: 'edge' }

export default async function handler(req) {
  const supabase = createClient(
    process.env.SUPABASE_URL!,
    process.env.SUPABASE_ANON_KEY!
  )
  // ... your code
}
```

### Full Report

Read the complete compatibility guide:
**[devradar.dev/check/supabase-vercel](https://devradar.dev/check/supabase-vercel)**

### Related

- [Vercel + PostgreSQL](https://devradar.dev/check/vercel-postgresql)
- [Next.js + Supabase](https://devradar.dev/check/nextjs-supabase)
- [Edge Runtime Compatible Databases](https://devradar.dev/check)

---

*Updated for Vercel Edge Runtime 2025*
```

---

## Issue 4: Bolt.new vs Cursor - AI Tool Comparison

**Title:** `Bolt.new vs Cursor - Which AI Tool Should You Choose?`

**Labels:** `ai-tool`, `comparison`, `discussion`

**Body:**
```markdown
## Bolt.new vs Cursor - AI Development Tool Comparison

### Two Different Approaches to AI-Powered Development

| Feature | Bolt.new | Cursor |
|---------|----------|--------|
| Type | Web-based Full-Stack | Desktop IDE |
| Best For | Quick prototypes | Daily development |
| Tech Stack | Any (StackBlitz) | VS Code based |
| AI Model | Claude + Others | Claude + GPT-4 |
| Price | Freemium | Free tier + Pro |

### Bolt.new Strengths

- No setup required, runs in browser
- Full-stack deployment built-in
- Great for learning and prototypes
- Excellent for React/Next.js projects

### Cursor Strengths

- Full IDE experience
- Better for large codebases
- Native Git integration
- Works with any language/framework

### When to Choose Which?

**Choose Bolt.new if:**
- You need to prototype quickly
- Learning a new stack
- Building side projects
- Don't want to install anything

**Choose Cursor if:**
- You're a full-time developer
- Working on production apps
- Need full IDE features
- Collaborating with a team

### Full Comparison

Read detailed reviews and comparisons:
- **[Bolt.new Review](https://devradar.dev/tools/bolt-new)**
- **[Cursor Review](https://devradar.dev/tools/cursor)**
- **[All AI Tools](https://devradar.dev/tools)**

### Discussion

What's your experience with these tools? Share your thoughts below!

---

*Compare 50+ AI tools at [devradar.dev/tools](https://devradar.dev/tools)*
```

---

## Issue 5: Top 10 AI Coding Tools in 2025

**Title:** `Top 10 AI Coding Tools for Developers in 2025`

**Labels:** `ai-tool`, `roundup`, `featured`, `discussion`

**Body:**
```markdown
## Top 10 AI Coding Tools for Developers in 2025

Complete comparison and reviews at **[devradar.dev/tools](https://devradar.dev/tools)**

### 1. Lovable - Prompt-to-App Builder
**[Full Review →](https://devradar.dev/tools/lovable)**
- Best for: Rapid prototyping, MVPs
- Pricing: Freemium ($20/mo Pro)
- Tech Stack: React, Next.js, Supabase

### 2. Bolt.new - Full-Stack AI Developer
**[Full Review →](https://devradar.dev/tools/bolt-new)**
- Best for: Quick prototypes, learning
- Pricing: Freemium
- Tech Stack: Any (StackBlitz powered)

### 3. Cursor - AI-First Code Editor
**[Full Review →](https://devradar.dev/tools/cursor)**
- Best for: Daily development, production apps
- Pricing: Free + $20/mo Pro
- Tech Stack: VS Code based

### 4. Claude Code - CLI AI Assistant
**[Full Review →](https://devradar.dev/tools/claude-code)**
- Best for: Terminal workflows, automation
- Pricing: Usage-based
- Tech Stack: Any (CLI tool)

### 5. v0.dev - AI UI Generator
**[Full Review →](https://devradar.dev/tools/v0)**
- Best for: UI components, landing pages
- Pricing: Free (Vercel)
- Tech Stack: React, Tailwind, Shadcn/ui

### 6. Windsurf - AI Code Editor
**[Full Review →](https://devradar.dev/tools/windsurf)**
- Best for: VS Code users wanting AI
- Pricing: Free + $15/mo Pro
- Tech Stack: Any (Codeium powered)

### 7. Replit Agent - Autonomous Developer
**[Full Review →](https://devradar.dev/tools/replit-agent)**
- Best for: Beginners, full apps
- Pricing: Free + $20/mo
- Tech Stack: Any (Replit ecosystem)

### 8. Aider - CLI Pair Programmer
**[Full Review →](https://devradar.dev/tools/aider)**
- Best for: Local development, Git workflows
- Pricing: Open source (self-hosted)
- Tech Stack: Any (CLI tool)

### 9. GitHub Copilot - AI Autocomplete
**[Full Review →](https://devradar.dev/tools/copilot)**
- Best for: Daily coding, IDE integration
- Pricing: $10-19/mo
- Tech Stack: Any (GitHub)

### 10. Cody - AI Coding Assistant
**[Full Review →](https://devradar.dev/tools/cody)**
- Best for: Code understanding, context
- Pricing: Free + $9/mo
- Tech Stack: Any (Sourcegraph)

### Full Comparison

Compare all 50+ AI tools with detailed reviews:
**[devradar.dev/tools](https://devradar.dev/tools)**

### Categories

- [Vibe Coding Tools](https://devradar.dev/tools) - Prompt-to-app builders
- [AI IDEs](https://devradar.dev/tools) - AI-powered editors
- [CLI Agents](https://devradar.dev/tools) - Terminal AI tools
- [Managed Platforms](https://devradar.dev/tools) - Full-stack hosting

### What's Your Favorite?

Share your experience with AI coding tools in the comments!

---

*Data updated: January 2025 | [devradar.dev](https://devradar.dev)*
```

---

## Instructions

1. Go to: https://github.com/devradar-dev/website/issues
2. Click "New Issue"
3. Choose a template or create from scratch
4. Copy the title and body from above
5. Add labels as specified
6. Submit issue

**Recommendation:** Create 1-2 issues per day to look natural to Google.
