# Amazon Q in Connect
- One application, one seamless experience for customers (omnichannel CX), agents (empowerment and productivity), supervisors and administrators
- Use of generative AI to overcome call-center operation challenges with recommended responses and actions
    - Identify customer concern (ask qualifying questions)
    - Search for solution across disparate sources (KMS, customer-facing FAQs, internal chats with colleagues)
    - Take additional steps to resolve concern (end call without resolution, transferring/escalating)

## Customizing Q
- AI agent (configure end-to-end functionality, associate prompts, KBs and **guardrails**, segment by persona or line of business)
    - Block undesirable topics, filter harmful/inappropriate content and words, redact PII, detect hallucinations in model responses using contextual grounding checks
- AI prompt (customize instructions to the LLM, control answer generation, action recommendation and execution, personalize responses based on contextual and customer information)

## Language support
- **Agent chat assistance**: 65 languages set using Locale in AI Agent, used when agents perform searches, ask questions or conversate with QiC in the workspace
- **Self-service**: 26 languages supporting what Lex supports, set via Custom Prompt (needs updating Self-service processor and Answer Generation)
- **Proactive Recommendations**: 🇬🇧, 🇪🇸, 🇫🇷, 🇵🇹, 🇨🇳 (Mandarin), 🇯🇵, 🇰🇷, used when an intent is triggered based on the transcript of the active conversation

## QiC is built on Amazon Bedrock
- **QiC**: ready-to-deploy application integrated with Connect, tailored to contact center use cases
- **Amazon Bedrock**: Large language models, prompts, KBs and guardrails
    - Does not train the LLM using customer data or conversations (runs locally)
    - Priced per minutes (voice, regardless of IVR or agent interaction) or messages (chat)

## How QiC works (basically KCS)
- **Customer issue**: auto-intent detection ML, or search, based on customer input
- **Relevant personal information**: custom data can be integrated to the interaction
- **Relevant company information**: Amazon Bedrock KBs referrals from customer's repository
- **What Q asks the LLM**: LLM prompts providing response as an agent using 
- **Generative solution**: provided by Amazon Bedrock (default LLM: Claude / Nova)