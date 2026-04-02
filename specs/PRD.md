# mea-wae-ike — Product Requirements Document

## Vision

A knowledge aggregator in the style of the *arr apps (Sonarr, Radarr, etc.) — automated collection, organization, and management of knowledge sources.

## Problem

Knowledge is scattered across many sources (feeds, APIs, documents, databases). There is no unified system for automatically pulling, normalizing, and organizing it — analogous to how *arr apps unify media acquisition.

## Goals

- Aggregate knowledge from multiple configurable sources
- Normalize and store knowledge in a unified format
- Provide visibility into what has been collected and from where
- Be extensible: new source types should be easy to add

## Non-goals (initial scope)

- No user-facing web UI in v1 (API-first)
- No AI/LLM summarization in v1
- Not a general-purpose note-taking app

## Architecture principles

- OTP-native: each source integration runs as a supervised process
- Configuration-driven: sources defined in config, not hardcoded
- Fault-tolerant: a failing source does not affect others

## Key concepts

| Term | Definition |
|---|---|
| **Source** | A configured external system to pull knowledge from |
| **Item** | A single unit of knowledge retrieved from a source |
| **Indexer** | A module that knows how to fetch items from a specific source type |

## Open questions

- Persistence backend (Ecto + PostgreSQL vs SQLite vs embedded?)
- Query/search interface (REST API? GraphQL? CLI only?)
- Scheduling model (polling intervals vs webhooks)
