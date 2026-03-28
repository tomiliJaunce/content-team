# Project Instructions for Claude

## Team Usage
ALWAYS use the `content-pipeline` team for all work in this project.

When working on tasks:
1. Check team status
2. Set `team_name: "content-pipeline"` when spawning agents
3. Coordinate via TaskList, TaskCreate, TaskUpdate
4. Communicate via SendMessage

## Team Structure
- team-lead (you) - Coordinates and manages tasks
- researcher - Conducts research and compiles sources
- content-specialist - Transforms research into content briefs
- content-writer - Writes articles based on briefs
- content-reviewer - Reviews content for quality and accuracy

## Workflow
1. Create tasks using TaskCreate
2. Assign tasks to appropriate team members using TaskUpdate
3. Monitor progress via TaskList
4. Coordinate with teammates using SendMessage
5. Use `/handoffs/` directory for work transitions

## Key Rules
- Never work solo - delegate to appropriate specialist
- All work tracked via task list
- All coordination via SendMessage
- Each agent works only in their own folder
- Use `/handoffs/` for transitions between agents
EOF