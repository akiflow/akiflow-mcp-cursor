# Akiflow for Cursor

Akiflow connects your tasks, calendar, and meeting notes to your AI client. Read a unified schedule across every connected calendar, create and reschedule tasks, time slots and events, and pull summaries and action items from meeting transcripts — all in natural language. Akiflow is the only calendar connector that aggregates multiple calendars into a single connection, so the AI sees your full schedule rather than one account at a time.

This is the official [Cursor](https://cursor.com) plugin for the **Akiflow MCP server**.

## Install

Install from the Cursor Marketplace ("Add to Cursor"), or add the server manually — see below.

## Configuration

The plugin registers a single remote MCP server; there is nothing to configure by hand:

```json
{
  "mcpServers": {
    "akiflow": {
      "url": "https://mcp.akiflow.com/mcp"
    }
  }
}
```

- **Transport:** Streamable HTTP.
- **Auth:** OAuth 2.1 with PKCE (S256), public clients, dynamic client registration. On first use Cursor opens your browser to sign in to Akiflow and grant access — no API keys or tokens to paste.
- **Requirements:** an active Akiflow account with the MCP feature enabled.

## What you can do

Ask in natural language, for example:

- *"What does tomorrow look like? Pull everything across all my calendars plus my planned tasks, and tell me where I have free time."*
- *"Add a task to review the Q3 budget, put it in my Work project, tag it finance, and set it due Friday."*
- *"Go through my inbox and schedule the three most important tasks into open slots this week."*
- *"Block 90 minutes for deep work tomorrow morning and call it PRD writing."*
- *"Set up a 30-minute sync with john@example.com Thursday at 3pm, add a video link, but don't email him yet."*

Under the hood the server exposes 22 tools, with read and write kept separate:

- **Read (11):** `list_tasks`, `get_schedule`, `get_task`, `get_event`, `get_time_slot`, `list_projects`, `list_tags`, `list_calendars`, `list_transcripts`, `get_transcript`, `get_transcript_by_event`.
- **Write (11):** `create_task`, `edit_task`, `complete_task`, `delete_task`, `plan_task`, `move_task_to_inbox`, `create_time_slot`, `edit_time_slot`, `create_event`, `edit_event`, `delete_event`.

## Support & documentation

- Setup guide: https://product.akiflow.com/help/articles/4302815-akiflow-mcp
- Help center: https://product.akiflow.com/help
- Email: support@akiflow.com
- Privacy: [Privacy Policy](https://akiflow.com/privacy-policy) · [AI Features Addendum](https://akiflow.com/privacy-policy-ai-addendum)

## License

[MIT](LICENSE). This wrapper repository is open source; the Akiflow MCP server and product remain proprietary.
