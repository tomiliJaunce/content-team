5. Initialize Team

Open Claude Code:

    Launch Claude Code application
    File > Open Folder > Select your project folder
    Paste the following into Claude Code chat:

Set up agent team for content production.

TEAM NAME: content-pipeline

AGENTS (all using claude-opus-4-6):
1. Researcher (general-purpose)
2. Content Specialist (general-purpose)
3. Content Writer (general-purpose)
4. Content Reviewer (general-purpose)

WORKFLOW:
- Researcher creates /handoffs/01_researcher_handoff.md
- Content Specialist creates /handoffs/02_specialist_handoff.md
- Writer creates /handoffs/03_writer_handoff.md
- Reviewer creates /handoffs/04_reviewer_handoff.md

Please:
1. Use TeamCreate tool to create "content-pipeline" team
2. Use Task tool to spawn all 4 agents with settings above
3. Each agent should read their ROLE.md from their folder
4. Verify all agents are active

After setup, I'll assign the first content topic.

Claude will create the team and spawn agents. Wait for confirmation that all 4 agents are active.
Usage
Create Your First Article

In Claude Code chat:

Create an article about "AI Coding Tools for Founders"

Target audience: Technical founders with 1-5 person teams
Angle: Practical tools that save time
Length: 1,500-2,000 words

Please:
1. Create Task #1 for Researcher
2. Assign to researcher agent
3. Monitor progress through pipeline
4. Update me when each phase completes

Monitor Progress

Ask Claude:

What's the status of all tasks?

Or check files manually:

# See latest handoff status
ls -lt handoffs/

# Read specific handoff
cat handoffs/01_researcher_handoff.md

Review Completed Work

Ask Claude:

Read the final article: /final-output/[article-name].md

Show me:
- Word count
- Key topics covered
- Any revisions made by reviewer

Request Revisions

If changes needed:

The article looks good, but please:
1. Add section on cost comparison
2. Include more specific examples
3. Expand conclusion

Assign this as revision task to the writer.

Troubleshooting
Team Not Found

Symptom: Claude says content-pipeline team doesn’t exist

Diagnose:

ls ~/.claude/teams/

Fix: If content-pipeline folder missing, run initialization prompt again. Ensure you’re in correct project directory.
Agent Not Responding

Symptom: Agent stuck, no handoff after 30+ minutes

Diagnose: Ask Claude:

Check status of [agent-name]:
- What task is assigned?
- Last activity?
- Any errors?

Fix:

    Restart agent: “Please restart the [agent-name] agent”
    Reassign task: “Please reassign Task #X to [agent-name]”
    Check if previous agent created their handoff file

Handoff File Missing

Symptom: Next agent waiting but previous agent didn’t create handoff

Check:

ls -la handoffs/
ls -la researcher/research.md
ls -la content-specialist/content-brief.md

Fix: Ask Claude:

Please check:
1. Did [previous-agent] complete their work?
2. Is their deliverable in their folder?
3. If yes, manually create the handoff file based on completed work

Quality Issues

Symptom: Articles don’t meet standards

Fix:

    Update ROLE.md with specific requirements

Edit content-reviewer/ROLE.md and add detailed checklist:

## Approval Checklist
- All statistics have sources cited
- No jargon without explanation
- Reading level: Grade 8-10
- At least 3 concrete examples
- Clear next step in conclusion
- Meta description under 160 characters
- Title under 60 characters

    Add example outputs to ROLE.md

Show agents what good output looks like.

    Refine content briefs

Update content-specialist/ROLE.md with more detailed brief requirements.
Performance Issues

Symptom: Pipeline takes 4+ hours per article

Fix:

    Use mixed models for speed:

Edit ~/.claude/teams/content-pipeline/config.json:

    Researcher: "model": "claude-sonnet-4-5-20250929" (faster)
    Content Specialist: "model": "claude-sonnet-4-5-20250929"
    Writer: "model": "claude-opus-4-6" (keep quality)
    Reviewer: "model": "claude-sonnet-4-5-20250929"

Then tell Claude: “Please reload the team configuration”

    Reduce scope:

    Target 1,000-1,500 words instead of 2,000
    Reduce sources from 20-25 to 10-15

Cost Issues

Symptom: API costs higher than expected

Fix:

Use mixed models (see Performance Issues above).

Cost comparison per 1,500-2,000 word article:

    All Opus 4.6: ~$4.75
    Mixed (Sonnet 4.5 + Opus 4.6): ~$2.75

Savings: ~40-50% with minimal quality impact.

Quick Reference
File Structure

    ~/.claude/teams/ - Team configs (auto-created)
    ~/.claude/tasks/ - Task queue (auto-created)
    .claude/settings.local.json - Permissions
    CLAUDE.md - Project instructions
    [agent]/ROLE.md - Agent responsibilities
    /handoffs/ - Agent-to-agent communication
    /final-output/ - Completed work

Key Tools (Claude Code chat)

    TeamCreate - Create new team
    Task - Spawn agent or assign work
    TaskList - View all tasks
    TaskCreate - Create new task
    TaskUpdate - Update task status
    SendMessage - Agent-to-agent communication

Common Commands

Ask Claude:

# Check status
What's the status of all tasks?

# Restart agent
Please restart the [agent-name] agent

# Reload team config
Please reload the team configuration

# Create new task
Create Task #X for [agent-name] to [task description]

Terminal:

# Check handoffs
ls -lt handoffs/

# Read handoff
cat handoffs/01_researcher_handoff.md

# Verify setup
cat .claude/settings.local.json
cat CLAUDE.md
ls */ROLE.md

Concepts Summary

Agent Teams: Coordinated autonomous agents with shared task list and peer-to-peer communication.

Subagents: Quick helpers for one-off tasks that report back to you.

File-based handoffs: Explicit communication between agents via /handoffs/ directory.

Task list: Shared queue at ~/.claude/tasks/[team-name]/ with JSON task definitions.

Quality gates: Each agent reviews previous agent’s work before proceeding.

Persistent state: Team configuration and tasks persist across sessions.