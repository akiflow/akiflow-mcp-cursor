# Changelog

All notable changes to the Akiflow Cursor plugin are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-06-18

### Added

- Initial release: registers the hosted Akiflow MCP server (`https://mcp.akiflow.com/mcp`) as a remote, URL-based MCP entry.
- One-click connect with OAuth 2.1 + PKCE — Cursor auto-discovers the authorization server and completes the flow in the browser; no API keys or manual configuration.
- Tools for tasks, schedule, time slots, calendar events, and meeting transcripts, with read and write split into separate tools.
