## 15.06.2026
### Tasks Completed:

- Updated the codebase in `website-builder` to stream logs section-by-section via WebSockets to the frontend instead of page-by-page, improving the user experience.
- Tested the WebSocket endpoints and logging flow using Postman.
- Pushed the code changes to the main server and verified that the streaming is working correctly.

### Key Learnings:

- Streaming execution logs section-by-section via WebSockets provides a much more interactive and responsive user experience than waiting for page-by-page updates.
- Testing WebSocket connections and real-time message streams with Postman is an efficient way to validate backend functionality before integrating with the frontend.

## 16.06.2026
### Tasks Completed:

- Attented brainstorming sessions for a new orchestration model at the platform level, including proposing and planning a new architecture.
- Analyzed and learned the current architecture model to identify key flows and limits.
- Designed a sample diagram mapping various user intents and how the current version of Dukanify handles them.

### Key Learnings:

- Mapping user-intent possibilities visually helps clarify system boundaries and simplifies designing orchestration logic at the platform level.
- Reviewing the existing platform architecture provides essential context before introducing structural orchestration changes.

## 17.06.2026
### Tasks Completed:

- Researched and brainstormed viable data structures to store and handle changing business data.
- Proposed a potential PostgreSQL-based data architecture featuring:
  - Relational tables for core structured data.
  - `JSONB` for storing dynamic business states.
  - `pgvector` embeddings for semantic search and retrieval.
  - Relationship graph tables to map connections.

### Key Learnings:

- Using a multi-model PostgreSQL setup (relational + JSONB document + pgvector + relationship tables) offers a flexible and powerful way to handle dynamic, evolving business states within a single database system.

## 18.06.2026
### Tasks Completed:

- Brainstormed ideas for a dynamic architecture.
- Planned the introduction of a unified platform, Dukanify OS, to handle and orchestrate all tasks.

### Key Learnings:

- Designing a unified operating system platform (Dukanify OS) can help centralize workflow execution and improve orchestration reliability across dynamic tasks.

## 19.06.2026
### Tasks Completed:

- Researched Neo4j graph database capabilities for managing relational and dynamic system architecture.
- Presented findings on Neo4j implementation to the team.
- Finalized the overall system architecture.

### Key Learnings:

- Neo4j is highly suited for modeling highly connected dynamic architecture relationships, enabling efficient query performance and data representation compared to standard relational models.
