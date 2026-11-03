# Haystack MCP server

Search live jobs from employers' own careers sites in plain English, from Claude, ChatGPT, Cursor, VS Code or any assistant that supports MCP. Ask which employers reply and how fast, and what their application forms ask, with answers drawn from more than 1.3 million job applications sent through Haystack.

- **Server address:** `https://haystackapp.io/mcp`
- **Transport:** Streamable HTTP
- **Sign-in:** none, no API key
- **Coverage:** the US, UK, Canada, Australia, India and Europe, every field (not only tech), 172,000+ employers with roles listed
- **Docs:** [haystackapp.io/mcp-server](https://haystackapp.io/mcp-server)

## Connect

### Claude

1. On claude.ai or the Claude app, open **Settings › Connectors**.
2. Choose **Add custom connector**, name it Haystack and paste `https://haystackapp.io/mcp`.
3. In a chat, turn Haystack on from the tools menu and ask for jobs.

### ChatGPT

1. Open **Settings › Apps & Connectors › Advanced** and turn on Developer mode.
2. Choose **Create**, name it Haystack, paste `https://haystackapp.io/mcp` and pick **No authentication**.
3. In a chat, add Haystack from the **+** menu and ask for jobs.

### Cursor

Add this to `~/.cursor/mcp.json`, then reload Cursor:

```json
{
  "mcpServers": {
    "haystack": { "url": "https://haystackapp.io/mcp" }
  }
}
```

### VS Code

Add this to `.vscode/mcp.json`, then start the server from the file:

```json
{
  "servers": {
    "haystack": { "type": "http", "url": "https://haystackapp.io/mcp" }
  }
}
```

### Claude Code

```bash
claude mcp add --transport http haystack https://haystackapp.io/mcp
```

## Tools

| Tool | What it does |
|---|---|
| `search_jobs` | Live jobs, newest first. Filter by title words, country, city, remote, and by what the advert says: no experience needed, no degree needed, visa sponsorship offered. Up to 20 jobs, each with its link, and an Auto Apply link when Haystack's AI agent can fill in and submit the employer's form. |
| `get_job` | One job's details: title, employer, location, pay, work mode, skills, the description, and what applying to that employer is like (reply rate, time to reply, form questions) when known. |
| `employer_facts` | An employer's live roles, the share of applications that got a reply, the median time to the first reply and the questions its form asks. With no company, the employers most likely to reply. |
| `application_system_facts` | Facts about an application system such as Greenhouse, Ashby, Workable, Lever or SmartRecruiters: how many fields its forms have, the questions they ask most, and how fast employers on it reply. |

## Things to ask

- "Find remote data analyst jobs in the US posted this week."
- "Which jobs in London say no experience is needed?"
- "Visa sponsorship jobs in the UK for software engineers."
- "Does Monzo reply to applications, and how fast?"
- "What will a Greenhouse application ask me?"
- "Which employers are most likely to reply?"

## Let it apply for you

Connect your own Haystack account at `https://haystackapp.io/mcp/account` (OAuth: your assistant asks you to sign in to Haystack once and press Allow). Your assistant can then list your best matches, and when you name the jobs you want, Haystack's AI agent fills in and submits each employer's form. Replies land in your Haystack inbox, and the assistant can read them, interview invitations included. It never applies to a job you did not pick.

| Tool | What it does |
|---|---|
| `my_account` | Your plan and applications left, setup and CV status, matches waiting, unread replies and your inbox address. |
| `my_matches` | Jobs matched to your CV and preferences, best first. |
| `apply_to_jobs` | Haystack's AI agent applies to up to five jobs you name. |
| `my_applications` | Applications Haystack has sent or is working on, newest first, with each employer's replies. |
| `my_inbox` | Employer emails in your Haystack inbox, newest first: interview invitations, rejections, requests for action. |
| `read_email` | One email in full; marks it read. |

Setup steps for each assistant: [haystackapp.io/mcp-server](https://haystackapp.io/mcp-server). Disconnect any time from **AI assistants** in the Haystack app.

## Privacy

The public server at `/mcp` never asks you to sign in and reads only public job data. Haystack logs which tool was called and a scrambled form of the calling address, to stop abuse. The account server at `/mcp/account` sees your own Haystack account only after you sign in and press Allow.

## Registry

Listed in the Official MCP Registry as `io.haystackapp/jobs` (public) and `io.haystackapp/auto-apply` (signed in). This repository holds documentation only; the server runs at haystackapp.io.

---

[Haystack](https://haystackapp.io) · AI job search for ambitious job seekers.
