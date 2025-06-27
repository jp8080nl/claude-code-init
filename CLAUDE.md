# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository documents and implements the Anthropic-recommended Test-Driven Development (TDD) workflow for agentic coding.

## Development Workflow

### Github flow and Test-Driven Development (TDD) Approach

This codebase follows a strict Git (GitHub) and TDD and workflow that leverages iterative development:

#### Initialize feature
- Claude code slash command /1-feature-init.md
We use this claude code command to 'Create a feature branch', 'Write Tests First' and 'Commit Tests'

#### Implement or update Feature
- Claude code slash command /2-feature-implement.md
We use this claude code command to 'Implement Code and update documentation', 'run Puppeteer test when UI changes', 'Run Linting and Formatting', 'Check code coverage' and 'Commit and push'

#### Git pull request flow
- Claude code slash command /3-feature-pr-flow.md
We use this claude code command to 'Create a pull request' and 'Check automated tests and do PR review'

## Development Setup

GitHub is not setup. Create repo and enable repo checks for running test.
1. run through setups and check if everything is setup correctly 

No build, test, or development tools are currently configured. When implementing features:
1. Choose appropriate language and framework based on requirements
2. Set up necessary configuration files following the TDD workflow
3. Establish project structure that supports test-first development

## Notes

- The repository is not yet initialized as a git repository
- Follow the TDD workflow strictly for all new functionality