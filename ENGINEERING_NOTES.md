# qdrant — engineering notes

Vector retrieval service · Source review: 6 November 2026

## Purpose

A candidate when retrieval needs a dedicated service and explicit payload-based filtering.

## Architecture reviewed

A Rust vector database with payload filters, API specifications, server code, tests and configuration.

Repository areas inspected: `lib, src, openapi, config, tests` (root inventory and linked README documentation).

## Decision and trade-off

A vector match is not an authorization decision. Tenant and document permissions must be enforced with the query and the application.

## Verification to perform

Test cross-tenant denial, filtered queries, deleted documents and a restore on disposable data.

This is a source review and a proposed verification plan. No upstream runtime suite, deployment, provider benchmark or paid API evaluation was run for these notes.

## Attribution and scope

- Original project: [qdrant/qdrant](https://github.com/qdrant/qdrant).
- Original license: Apache-2.0; retained without replacement.
- Original README and source history remain part of the fork.
- This portfolio layer adds documentation; it does not claim authorship of the upstream project or an accepted upstream contribution.
- Dependency licenses, model weights, hosted services and any existing NOTICE files remain subject to their own terms.

## Start from the maintained instructions

Read the [upstream README](https://github.com/qdrant/qdrant/blob/master/README.md) and its contribution guidance for current installation and development commands.
