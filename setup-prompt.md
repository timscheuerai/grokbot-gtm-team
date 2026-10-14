# Setup prompt

A Grok Bot can create other Bots, group chats and routines from its chat. My Chief of Staff created new Bots and the Content Room for me that way. This prompt uses it to build the whole team in 1 go.

1. In Grok Bot, create a new Bot and call it Chief of Staff.
2. Paste the prompt below into its chat.
3. Answer its questions. It creates the rest and tells you what it couldn't do.

```text
Set up my Grok Bot GTM team from github.com/timscheuerai/grokbot-gtm-team.

1. Read README.md and every file in agents/. The raw files are at
   https://raw.githubusercontent.com/timscheuerai/grokbot-gtm-team/main/agents/<file>.md
2. Ask me these questions in 1 message, then wait for my answers:
   - My company, what we sell and who we sell to (our ICP)
   - Which GTM tools we use for tables, enrichment, sequences and the
     inbox (the files assume the OXYGEN CLI, swap the names if needed)
   - Where my second brain lives (voice, proof, audience), if I have one
   - Where Claude Code and Codex run for me: my Mac, an always-on server
     over SSH, or not set up yet
   - Which Bots I want now (default: all of them)
3. Take on the Chief of Staff instructions from agents/01-chief-of-staff.md.
4. Create each Bot I picked, with its name and the instructions block from
   its file, adapted to my answers. Keep every rule about approvals,
   spend and connectors exactly as strict as written.
5. Create a group chat called Content Room with the Head of Content,
   LinkedIn Writer, X Writer, YouTube Writer, Graphic Designer and you.
6. Create 1 routine: the Outbound Lead, weekdays at 08:20 in my time zone,
   the outbound rollup. No other routines.
7. Show me what you created, and anything you couldn't create, with the
   step I need to do in the app.

During setup, don't connect any tool, send any message or spend credits.
```

After setup, connect your tools in Grok Bot's settings. Each Bot's instructions already say which connectors it may use, because Grok Bot has no per-Bot connector switch.

## Prefer to do it by hand?

Create each Bot in the app and paste the instructions block from its file in [agents/](agents/). Start with the Chief of Staff and the Outbound Lead; the others can wait until you need them.
