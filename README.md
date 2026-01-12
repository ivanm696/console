# bolt.new
# [![Bolt Open Source Codebase](./public/social_preview_index.jpg)](https://bolt.new)

> Welcome to the **Bolt** open-source codebase! This repo contains a simple example app using the core components from bolt.new to help you get started building **AI-powered software development tools** powered by StackBlitz’s **WebContainer API**.

### Why Build with Bolt + WebContainer API

By building with the Bolt + WebContainer API you can create browser-based applications that let users **prompt, run, edit, and deploy** full-stack web apps directly in the browser, without the need for virtual machines. With WebContainer API, you can build apps that give AI direct access and full control over a **Node.js server**, **filesystem**, **package manager** and **dev terminal** inside your users browser tab. This powerful combination allows you to create a new class of development tools that support all major JavaScript libraries and Node packages right out of the box, all without remote environments or local installs.

### What’s the Difference Between Bolt (This Repo) and [Bolt.new](https://bolt.new)?

- **Bolt.new**: This is the **commercial product** from StackBlitz—a hosted, browser-based AI development tool that enables users to prompt, run, edit, and deploy full-stack web applications directly in the browser. Built on top of the [Bolt open-source repo](https://github.com/stackblitz/bolt.new) and powered by the StackBlitz **WebContainer API**.

- **Bolt (This Repo)**: This open-source repository provides the core components used to make **Bolt.new**. This repo contains the UI interface for Bolt as well as the server components, built using [Remix Run](https://remix.run/). By leveraging this repo and StackBlitz’s **WebContainer API**, you can create your own AI-powered development tools and full-stack applications that run entirely in the browser.

# Get Started Building with Bolt

Bolt combines the capabilities of AI with sandboxed development environments to create a collaborative experience where code can be developed by the assistant and the programmer together. Bolt combines [WebContainer API](https://webcontainers.io/api) with [Claude Sonnet 3.5](https://www.anthropic.com/news/claude-3-5-sonnet) using [Remix](https://remix.run/) and the [AI SDK](https://sdk.vercel.ai/).

### WebContainer API

Bolt uses [WebContainers](https://webcontainers.io/) to run generated code in the browser. WebContainers provide Bolt with a full-stack sandbox environment using [WebContainer API](https://webcontainers.io/api). WebContainers run full-stack applications directly in the browser without the cost and security concerns of cloud hosted AI agents. WebContainers are interactive and editable, and enables Bolt's AI to run code and understand any changes from the user.

The [WebContainer API](https://webcontainers.io) is free for personal and open source usage. If you're building an application for commercial usage, you can learn more about our [WebContainer API commercial usage pricing here](https://stackblitz.com/pricing#webcontainer-api).

### Remix App

Bolt is built with [Remix](https://remix.run/) and
deployed using [CloudFlare Pages](https://pages.cloudflare.com/) and
[CloudFlare Workers](https://workers.cloudflare.com/).

### AI SDK Integration

Bolt uses the [AI SDK](https://github.com/vercel/ai) to integrate with AI
models. At this time, Bolt supports using Anthropic's Claude Sonnet 3.5.
You can get an API key from the [Anthropic API Console](https://console.anthropic.com/) to use with Bolt.
Take a look at how [Bolt uses the AI SDK](https://github.com/stackblitz/bolt.new/tree/main/app/lib/.server/llm)

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v20.15.1)
- pnpm (v9.4.0)

## Setup

1. Clone the repository (if you haven't already):

```bash
git clone https://github.com/stackblitz/bolt.new.git
```

2. Install dependencies:

```bash
pnpm install
```

3. Create a `.env.local` file in the root directory and add your Anthropic API key:

```
ANTHROPIC_API_KEY=XXX
```

Optionally, you can set the debug level:

```
VITE_LOG_LEVEL=debug
```

**Important**: Never commit your `.env.local` file to version control. It's already included in .gitignore.

## Available Scripts

- `pnpm run dev`: Starts the development server.
- `pnpm run build`: Builds the project.
- `pnpm run start`: Runs the built application locally using Wrangler Pages. This script uses `bindings.sh` to set up necessary bindings so you don't have to duplicate environment variables.
- `pnpm run preview`: Builds the project and then starts it locally, useful for testing the production build. Note, HTTP streaming currently doesn't work as expected with `wrangler pages dev`.
- `pnpm test`: Runs the test suite using Vitest.
- `pnpm run typecheck`: Runs TypeScript type checking.
- `pnpm run typegen`: Generates TypeScript types using Wrangler.
- `pnpm run deploy`: Builds the project and deploys it to Cloudflare Pages.

## Development

To start the development server:

```bash
pnpm run dev
```

This will start the Remix Vite development server.

## Testing

Run the test suite with:

```bash
pnpm test
```

## Deployment

To deploy the application to Cloudflare Pages:

```bash
pnpm run deploy
```

Make sure you have the necessary permissions and Wrangler is correctly configured for your Cloudflare account.
[![Bolt.new: AI-Powered Full-Stack Web Development in the Browser](./public/social_preview_index.jpg)](https://bolt.new)
#
Navigation Menu
bolt.new

Code
Pull requests
8
bolt.new/
yosiwizman
yosiwizman
2 days ago
Cannot retrieve ahead/behind information for this branch.
bolt.new/
Name	Last commit date
.github
2 days ago
.husky
2 years ago
app
2 days ago
functions
2 days ago
icons
2 days ago
public
2 days ago
types
2 years ago
.editorconfig
2 years ago
.gitattributes
2 days ago
.gitignore
2 years ago
.prettierignore
2 years ago
.prettierrc
2 years ago
.tool-versions
2 years ago
CONTRIBUTING.md
2 years ago
LICENSE
2 years ago
README.md
2 days ago
bindings.sh
2 years ago
eslint.config.mjs
2 years ago
load-context.ts
2 years ago
package.json
2 days ago
pnpm-lock.yaml
2 years ago
tsconfig.json
2 years ago
uno.config.ts
2 years ago
vite.config.ts
2 days ago
worker-configuration.d.ts
2 years ago
wrangler.toml
2 days ago
README.md
X Builder
CI

AI-powered full-stack web development in the browser.

Based on Bolt.new - the open-source AI web development agent by StackBlitz.

Production
🚀 Live URL: https://x-builder-staging.pages.dev

Status: Production (Cloudflare Pages)

Note: Custom domain can be added later without downtime.

About
X Builder is a white-label fork of Bolt.new that allows you to prompt, run, edit, and deploy full-stack applications directly from your browser.

Features
Full-Stack in the Browser: Integrates AI models with an in-browser development environment powered by StackBlitz's WebContainers

Install and run npm tools and libraries (Vite, Next.js, etc.)
Run Node.js servers
Interact with third-party APIs
Deploy to production from chat
AI with Environment Control: AI models have complete control over the filesystem, node server, package manager, terminal, and browser console

Tips and Tricks
Be specific about your stack: Mention frameworks/libraries in your initial prompt
Use the enhance prompt icon: Refine your prompt with AI assistance before submitting
Scaffold basics first: Establish the foundation before adding advanced features
Batch simple instructions: Combine multiple simple tasks in one message
Technical Notes
MVP Publish (Cloudflare Pages)
X Builder includes an MVP publish feature that deploys projects directly to Cloudflare Pages.

Components:

app/lib/stores/publish.ts - State management for publish status
app/routes/api.publish.ts - API endpoint for Cloudflare Pages deployment
app/components/workbench/PublishButton.client.tsx - UI button component
Environment Variables (for publish to work at runtime):

CLOUDFLARE_API_TOKEN - API token with Pages permissions
CLOUDFLARE_ACCOUNT_ID - Your Cloudflare account ID
TODO: The Cloudflare Pages Direct Upload API implementation may need adjustment based on actual API requirements for production use.

Cross-Origin Isolation
X Builder requires crossOriginIsolated to be enabled for WebContainers (SharedArrayBuffer). This is achieved via HTTP headers:

Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Embedder-Policy: credentialless
These headers are set in:

public/_headers - Cloudflare Pages static headers
app/entry.server.tsx - Server-side rendering
functions/[[path]].ts - Cloudflare Pages Functions
vite.config.ts - Development server
To verify: Open DevTools console and check self.crossOriginIsolated === true

Development
Prerequisites
Node.js 20.15.1+
pnpm 9.4.0+
Setup
pnpm install
pnpm run dev
Scripts
pnpm run dev - Start development server
pnpm run build - Build for production
pnpm run lint - Run ESLint
pnpm run typecheck - Run TypeScript checks
pnpm test - Run tests
Deployment
Production deploys automatically from main branch via GitHub Actions to Cloudflare Pages.

Required GitHub Secrets:

CLOUDFLARE_API_TOKEN - Cloudflare API token with Pages edit permissions
CLOUDFLARE_ACCOUNT_ID - Your Cloudflare account ID
Release Process
1. Create a Pull Request with your changes
2. CI runs automatically (lint, typecheck, tests)
3. CI must pass before merge is allowed
4. Merge PR to main
5. Auto-deploy to production (Cloudflare Pages)
Safeguards:

Branch protection requires PR reviews
All CI checks must pass
Direct pushes to main are blocked
Linear history enforced
Attribution
This project is based on Bolt.new by StackBlitz, licensed under MIT.

