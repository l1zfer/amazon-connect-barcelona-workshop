# Amazon Q in Connect
## Enable Q in your self-service
- Q&A based on customer history and company knowledge
- Recommend actions, links and inline step-by-step guides

## Deciding on what to automate
- Range of self-service automation:
    - **Highly structured**: bill payment, password resets, prescription refills, booking changes
        - Create structured conversations directly in Connect
    - **Mixed**: returns / refunds, account changes, warranty claims, document submissions
        - Drag-and-drop interface to build omnichannel self-service combining structured conversations with AI agents and orchestrating human-on-the-loop experiences
        - Control and auditability of actions AI agents take
    - **Highly fluid**: outage support, troubleshooting, complaint resolution, recommendations
        - Out-of-the-box, custom AI agents for customer service (take actions, provide answers and make recommendations) powered by Bedrock

## QiC Assistant components
- Flow: Assistant -> AI Agent -> AI Prompt -> Self-service Tools
- Each component builds upon the others to create a complete intelligent interaction system
### Assistant
- Primary container for AI capabilities
- Associates with AI Agents
- Manages KBs
- Handles sessions
### AI Prompts
- Provide LLM instructions (tone, guardrails, behaviors etc) for pre-processing prompts written in **YAML**
- Determines tools selection
- Utilizes session data
### AI Agents
- Configures end-to-end functionality
- Associates AI Prompts
- Overrides KB usage
### Self-service Tools
- Answer questions
- Collect information
- Executes actions
- Defined in AI Prompts

## Tools in QiC
- **Default tools**
    - QUESTION: provides direct answers using KB
    - ESCALATION: transfers to human agent when needed
    - CONVERSATION: handles basic dialogue
    - COMPLETE: concludes resolved interactions
- **Custom tools**
    - Create specialized actions for specific use cases
    - Define input schemas and response formats
    - Interact with Lex bots or step-by-step guides
    - Enabled automated actions

## AI Agents for self-service
- Pre-processing
    - Instructions for the AI Agent (control behavior, personality and responses, define tool usage)
    - Scope and provide examples of use cases
    - Uses MESSAGES
- Answer generation
    - Instructions for how to generate a RAG response