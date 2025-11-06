[Copilot Studio](https://copilotstudio.microsoft.com/)

Option 1
1. Create a Copilot (bot) in Copilot Studio
    - Define a topic like “Create Agile User Story”
    - Use trigger phrases like “write a user story” or “new feature request”
2. Use Power Automate to Orchestrate Logic
    - Create a flow that:
        - Collects user inputs (persona, goal, value, etc.)
        - Stores them in variables or a SharePoint list / Dataverse table
        - Calls an AI model (e.g., Azure OpenAI or Copilot connector) with your generateUserStory() prompt
        - Returns the formatted story to the user
3. Add a “Refine” Option
    - Create a second topic or flow for refineUserStory()
    - Let users select a story to improve, then walk them through refinement questions

Option 2: Power Apps + Power Automate
🔹 Use Case
Build a custom form-based app where users input story elements and get AI-generated output.
🛠 How It Works
- Power Apps Frontend
- Create a canvas app with fields:
- Persona
- Goal
- Value
- Acceptance Criteria
- Priority, Tags, etc.
- Add a “Generate Story” button
- Power Automate Backend
- Trigger a flow when the button is clicked
- Compose the prompt using your generateUserStory() logic
- Call Azure OpenAI or a Copilot connector to generate the story
- Return the result to Power Apps for display or storage

🔄 Reusability & Modularity
You can store your prompt modules in:
- Dataverse tables (tagged by type, platform, version)
- Environment variables (for quick updates)
- SharePoint (if collaborating with others)
This lets you build a prompt library that’s:
- Version-controlled
- Editable by non-developers
- Callable across apps and bots

🧠 Bonus: Add Learning Loops
Since you’re building for collaborative learning:
- Let users rate or comment on generated stories
- Store feedback to improve prompts over time
- Use Power BI to visualize usage and quality trends

Would you like a sample Power Automate flow outline or Power Apps screen layout to get started?
