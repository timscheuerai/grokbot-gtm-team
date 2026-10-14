# Send the work to Claude Code and Codex

Grok Bot is great at running a team: clear jobs, group chats, reliable scheduled tasks. For the work itself (copy, graphics, videos, code) I get better results from Claude Code and Codex with the skills I already built there, and their subscriptions are cheaper than Grok Bot credits. So Grok Bot orchestrates, and Claude Code and Codex do the work.

## The handoff

Any Bot that needs something built hands the Chief of Staff a unit of work with 4 parts:

| Part | Example |
|---|---|
| Outcome | 3 LinkedIn hooks for Thursday's post, in my voice |
| Inputs | The brief from the Head of Content, last week's top post |
| Skill | `linkedin-hook-writer` |
| Limits | Draft only, no publishing, no new proof numbers |

## How the Chief of Staff runs it

1. It starts Claude Code or Codex in a persistent terminal session (tmux or Herdr) inside the right repo, 1 git worktree or branch per task.
2. It picks the subscription with the most weekly limit left.
3. It sends the outcome, inputs, skill and limits as 1 prompt, waits, and reads the result.
4. It brings you the file, branch or pull request to review.

Because the sessions are real terminal sessions, you can attach at any time to watch, interrupt or take over. That is founder mode: when I have something specific to build, I open my terminal and work with Claude Code or Codex directly.

## Where it runs

- **Your Mac** for content and design. That is where the renderers, fonts, browser and logins are. Grok Bot reaches it through local execution, and each command asks for your approval until you allow it in the settings.
- **An always-on dev server over SSH** for product and outbound code. Keep Claude Code and Codex logged in on the server itself, so your subscription tokens never pass through the chat. Never give the Chief of Staff access to production.

## No Claude Code or Codex yet?

The team still works. Delete the "hand it to the Chief of Staff" line from a Bot's instructions and it does the work itself. You can add the handoff later, 1 Bot at a time.
