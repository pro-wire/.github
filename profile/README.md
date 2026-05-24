# ProWire

**A modular application framework for [ProcessWire](https://processwire.com/) — build faster, ship smarter.**

ProWire is a collection of composable modules that sit on top of ProcessWire and give you a production-ready foundation for building modern web applications. Each module is independently usable, but they're designed to work together seamlessly as a full-stack framework.

---

## Why ProWire?

ProcessWire is an exceptionally flexible CMS and framework — but that flexibility means every project often reinvents the same patterns: authentication, routing, multi-tenancy, API layers. ProWire captures those patterns as reusable, well-structured modules so you can focus on your application logic, not the scaffolding.

- **Modular by design** — use one module or the whole stack
- **No lock-in** — each module is its own repository and can be dropped into any ProcessWire project
- **Composable** — modules are built to integrate with each other out of the box when used together
- **Developer-first** — clean APIs, consistent conventions, minimal magic

---

## The Module Ecosystem

### 🔩 [AdminHelper](https://github.com/pro-wire/admin-helper) — Core Framework Engine
The backbone of ProWire. AdminHelper provides the shared conventions, hooks, and utilities that all other ProWire modules build on. Start here.

### 🔐 [Auth](https://github.com/pro-wire/auth) — Headless Authentication
A headless authentication module for ProcessWire. Handles login, registration, sessions, tokens, and access control — decoupled from any frontend so you can pair it with any client.

### 🌐 [ProcessWire JSON API](https://github.com/pro-wire/processwire-json-api) — REST API Layer
Exposes your ProcessWire content and data as a structured JSON API. Configurable, filterable, and built for headless and hybrid setups.

### 🚦 [ApiRouter](https://github.com/pro-wire/api-router) — Request Routing
A clean, expressive router for handling API requests in ProcessWire. Define routes, middleware, and handlers without fighting the core.

### 🏢 [MultiTenant](https://github.com/pro-wire/multi-tenant) — Multi-Tenancy Support
Run multiple isolated tenants from a single ProcessWire installation. Manage per-tenant data, configuration, and access — without the complexity.

### 🧭 [Nautilus](https://github.com/pro-wire/nautilus) — Utilities
A utility belt for ProcessWire development. Helpers, convenience methods, and common patterns used across the ProWire ecosystem (and handy on their own).

---

## How the Modules Fit Together

```
┌─────────────────────────────────────────────────┐
│                  Your Application                │
├──────────────┬──────────────┬────────────────────┤
│  ApiRouter   │  Auth        │  MultiTenant        │
├──────────────┴──────────────┴────────────────────┤
│           ProcessWire JSON API                   │
├──────────────────────────────────────────────────┤
│           AdminHelper (Core Engine)              │
├──────────────────────────────────────────────────┤
│                  ProcessWire                     │
└──────────────────────────────────────────────────┘
              + Nautilus (anywhere)
```

AdminHelper provides the foundation. The API layer, auth, and tenancy modules sit above it. Your application logic sits on top of everything — using as much or as little of the stack as you need.

---

## Getting Started

The recommended starting point is the main **ProWire** project, which wires together the core modules with a sensible default configuration.

```bash
# Clone the main project
git clone https://github.com/pro-wire/prowire
cd prowire

# Follow the setup guide
# docs/getting-started.md
```

Or install individual modules into an existing ProcessWire project by following the README in each module's repository.

---

*Built on top of [ProcessWire CMS/CMF](https://processwire.com/)*
