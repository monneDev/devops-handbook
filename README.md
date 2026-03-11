# DevOps Handbook

This repository is a structured DevOps knowledge base designed for humans and AI systems using Retrieval Augmented Generation (RAG).

## Purpose

The goal is to provide concise, practical, and consistently formatted documentation for core DevOps topics.

- Small, focused Markdown files for high retrieval precision.
- Clear headings for predictable chunking and embeddings.
- Practical examples and command workflows for real operations.
- Consistent language and structure across all topics.

## Repository Structure

```text
devops-handbook/
??? docker/
?   ??? docker-basics.md
?   ??? docker-images.md
?   ??? docker-containers.md
?   ??? docker-compose.md
?   ??? docker-networking.md
??? kubernetes/
?   ??? kubernetes-basics.md
?   ??? pods.md
?   ??? deployments.md
?   ??? services.md
?   ??? ingress.md
??? ci-cd/
?   ??? ci-cd-basics.md
?   ??? github-actions.md
?   ??? git-workflows.md
?   ??? automated-testing.md
??? infrastructure/
?   ??? infrastructure-as-code.md
?   ??? terraform-basics.md
?   ??? configuration-management.md
??? cloud/
?   ??? cloud-basics.md
?   ??? aws-basics.md
?   ??? azure-basics.md
?   ??? cloud-networking.md
??? monitoring/
    ??? monitoring-basics.md
    ??? logging.md
    ??? observability.md
```

## RAG Usage

This repository is ready for RAG indexing.

- Each file is scoped to a single topic.
- Sections like `Key Concepts` and `Practical Commands` improve retrieval quality.
- The format supports both file-level and section-level chunking.
- Content is written in clear technical English for strong embedding quality.
