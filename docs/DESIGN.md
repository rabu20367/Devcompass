# DevCompass Design Overview

This document outlines the initial architecture, technology stack, and planned features for the **DevCompass** project.

## Vision

DevCompass aims to provide an extensible developer portal that centralizes service documentation, tooling, and lifecycle management for modern software teams.

## Architecture

The project is organized as a web application with a modular backend and a customizable frontend interface. The high‑level components are:

1. **Frontend** – Built with [React](https://react.dev/), offering UI components for the service catalog, search, and documentation.
2. **Backend API** – A REST/GraphQL service implemented with [Node.js](https://nodejs.org/) and [Express](https://expressjs.com/). It exposes APIs for the service catalog, authentication, and integration with third-party systems.
3. **Database** – [PostgreSQL](https://www.postgresql.org/) stores persistent data such as service metadata and user accounts.
4. **Authentication** – Integrates with OAuth providers (e.g., GitHub, Google) for single sign-on.

A simplified diagram:

```text
+----------------------+        +----------------+
|   React Frontend     |  <---> | Node.js API    |
+----------------------+        +----------------+
             |                        |
             v                        v
        Browser Clients          PostgreSQL
```

## Technology Stack

- **Frontend**: React, TypeScript, Webpack or Vite.
- **Backend**: Node.js (TypeScript), Express, GraphQL.
- **Database**: PostgreSQL with an ORM such as Prisma or Sequelize.
- **Deployment**: Docker containers orchestrated via Kubernetes or Docker Compose for local development.

## Key Features

1. **Service Catalog**: Central listing of all internal services with metadata, owners, and links to documentation or repositories.
2. **Documentation Hub**: Ability to author and display technical docs written in Markdown.
3. **Search**: Unified search across the catalog and documentation.
4. **Plugin System**: Extension points to add custom tools or integrations (e.g., CI/CD status, incident management).
5. **Authentication**: OAuth-based login and role-based access control.

## Development Setup

1. Clone the repository and install dependencies:

```bash
git clone <repo-url>
cd Devcompass
npm install
```

2. Start the development servers (frontend and backend):

```bash
npm run start
```

This launches the React app and the Node.js API with hot reload enabled.

## Contributing

- Fork the repository and create a feature branch for your changes.
- Run tests with `npm test` or `pytest` depending on the component.
- Submit pull requests with a clear description of your changes.

## Roadmap

The initial release will focus on:

- Service catalog basics.
- Markdown-based documentation pages.
- OAuth login via GitHub.
- Containerized deployment with Docker Compose.

Future iterations may add Kubernetes support, more integrations, and a plugin marketplace.

