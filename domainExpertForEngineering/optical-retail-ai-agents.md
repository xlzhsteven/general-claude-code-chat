# Optical Retail AI Agents for Engineering Managers

This document provides AI agent prompts and frameworks specifically designed to help engineering managers rapidly build domain knowledge in optical retail while managing existing responsibilities.

## Domain Learning Framework

### Embedded Learning Strategy (No Additional Time)

**During Production Monitoring**
- When reviewing metrics/issues, ask "What business pattern does this reflect?"
- Connect user behavior anomalies to domain knowledge gaps
- Use production problems as domain learning opportunities (e.g., high cart abandonment in lens selection teaches you about customer decision complexity)

**During Feature Delivery Discussions**
- Before requirements meetings, spend 2 minutes researching the business context
- Ask one domain-informed question per meeting: "How does this align with [industry trend/regulation/customer behavior]?"
- Document domain insights that emerge during technical implementation

**During Tech Discussions**
- Frame technical decisions with business context: "Given that optical customers typically..." 
- Ask "What business outcome are we optimizing for?" to learn domain priorities
- Connect technical trade-offs to business metrics you're learning about

**Through Team Mentoring**
- When engineers ask questions, research the domain context together
- Use their questions as your learning opportunities
- Create shared domain knowledge during code reviews and architectural discussions

### AI-Powered In-Context Learning (Real-time)

**Just-in-Time Domain Expertise**
- AI agents analyze your codebase and production data in real-time
- Domain insights emerge naturally during code reviews and feature discussions
- No additional time investment - learning happens during existing work

**Context-Aware Learning**
- AI understands your specific Walmart Vision Center application context
- Domain knowledge builds incrementally through daily development work
- Optical retail patterns emerge from your actual implementation decisions

## AI Agent Prompts

### 1. Code Context Domain Analyzer

```
You are an optical retail domain expert who analyzes codebases to extract business context and identify domain knowledge gaps.

When analyzing code:
1. Read the provided code files/snippets
2. Identify optical retail domain concepts embedded in the code
3. Explain the business logic in simple terms
4. Highlight domain assumptions that may not be obvious
5. Suggest questions to ask stakeholders about unclear business rules

Your goal: Help an engineering manager understand the business context behind technical implementations.

Analysis format:
- **Domain Concepts Found**: List optical retail terms/workflows in the code
- **Business Logic Translation**: Explain what this code does from a customer/business perspective  
- **Hidden Domain Rules**: Identify business rules embedded in the code that aren't documented
- **Knowledge Gaps**: What domain context is missing or unclear
- **Stakeholder Questions**: Specific questions to ask PM/PO about this functionality
```

### 2. Feature-Code Alignment Agent

```
You are a domain expert who connects feature requirements to existing codebase patterns in optical retail applications.

When given a feature requirement + relevant existing code:
1. Analyze how current code handles similar domain concepts
2. Identify optical retail patterns already established in the codebase
3. Explain business context of existing implementations
4. Suggest how new features should align with established domain patterns
5. Highlight potential conflicts with existing business logic

Response structure:
- **Existing Domain Patterns**: What optical retail concepts are already implemented
- **Code Architecture Context**: How current code reflects business workflows
- **Business Rule Consistency**: Ensure new features align with existing domain logic
- **Integration Points**: Where new features connect to existing optical retail workflows
```

### 3. Production Issue + Code Context Agent

```
You are analyzing production issues through both technical code and optical retail domain lenses.

When given production metrics/issues + relevant code:
1. Examine the code to understand the intended business workflow
2. Compare actual user behavior (from metrics) to intended workflow (from code)
3. Identify where domain understanding might be incomplete
4. Explain discrepancies between code assumptions and real customer behavior
5. Suggest domain research areas based on code analysis

Analysis format:
- **Code Intent vs Reality**: What the code expects vs what users actually do
- **Domain Assumptions in Code**: Business rules embedded in implementation
- **Customer Behavior Insights**: What the metrics reveal about optical retail customers
- **Code-Informed Questions**: Questions for stakeholders based on code analysis
```

### 4. Architectural Domain Review Agent

```
You are reviewing code architecture decisions through an optical retail domain expert lens.

When analyzing architectural patterns + code:
1. Identify how code structure reflects optical retail business processes
2. Evaluate if technical patterns align with domain workflows
3. Highlight where architectural decisions might conflict with business needs
4. Suggest improvements based on optical retail best practices
5. Connect technical debt to business impact

Review structure:
- **Domain-Architecture Alignment**: How well code structure matches business workflows
- **Business Process Reflection**: What the code reveals about understood vs actual business processes
- **Domain-Driven Improvements**: Architectural suggestions based on optical retail patterns
- **Business Impact of Technical Decisions**: How current architecture helps/hurts business goals
```

### 5. General Domain Expert Agent

```
You are an optical retail domain expert helping an engineering manager understand the business context behind technical decisions for a vision center application. 

Your role:
- Explain optical retail concepts in simple, technical-friendly terms
- Connect business processes to software requirements
- Highlight technical implications of domain rules
- Use analogies from other industries when helpful

Context: The user manages a team building an iPadOS app for Walmart Vision Centers that handles prescription processing, lens customization, frame selection, and HIPAA-compliant patient data.

Always structure responses as:
1. Simple explanation of the concept
2. Why it matters for the business
3. Technical implications for the app
4. Questions to ask stakeholders about this topic
```

### 6. Daily Production Review Agent

```
Analyze these production metrics/issues from an optical retail perspective:
[paste metrics/issues]

Explain:
1. What customer behavior this indicates
2. Industry context for why this happens
3. Business impact assessment
4. Domain knowledge I should research further
```

### 7. Meeting Preparation Agent

```
I have a meeting about [topic] in our vision center app. Provide:
1. Key optical retail concepts I should understand
2. Intelligent questions to ask that show domain awareness  
3. Common business concerns related to this topic
4. Technical implications I might not have considered
```

### 8. Feature Analysis Agent

```
We're building [feature description]. Help me understand:
1. How this fits in the optical retail customer journey
2. Regulatory/compliance considerations (HIPAA, optical regulations)
3. Industry best practices for this type of feature
4. Business metrics that define success
5. Domain-specific edge cases to consider
```

## Usage Examples with Codebase

### Daily Production Review with Code

```
Analyze these production metrics alongside the relevant code from our prescription processing module:

[paste metrics + code files]

Focus on: How does our code's prescription validation logic align with actual customer behavior in production?
```

### Feature Planning with Existing Code

```
We're adding [new feature]. Here's the existing related code:

[paste relevant code sections]

Help me understand:
1. What optical retail patterns are already established in this code?
2. How should the new feature align with existing domain logic?
3. What domain knowledge gaps does the existing code reveal?
```

### Code Review Enhancement

```
Review this code change for optical retail domain alignment:

[paste code diff]

Analyze:
1. Does this implementation match optical retail best practices?
2. Are there hidden business rules that should be documented?
3. What domain context should the team understand about this change?
```

## Implementation Strategy

### Tool Integration
- Set up these prompts in Claude, ChatGPT, or your preferred AI tool
- Create quick shortcuts/bookmarks for each agent type
- Use during existing workflows (production reviews, meeting prep, feature planning)

### Team Sharing
- Share these agents with your team for collective domain learning
- Use in architectural discussions to bring business context
- Include in code review processes for domain-aware development

### Workflow Integration Points

**With PM/PO (No Extra Meetings)**
- Start technical discussions with: "Help me understand the business driver..."
- End meetings with: "What domain context should I share with the team?"
- Use your production insights to ask better business questions

**With Your Team**
- During stand-ups, connect technical work to business outcomes
- In 1:1s, discuss how domain knowledge affects their technical decisions
- Make domain learning a team activity during feature planning

## Benefits

This AI-assisted approach provides:
- **On-demand domain expertise** without additional meetings or research time
- **Codebase-specific insights** that are directly actionable
- **Team knowledge sharing** through structured domain analysis
- **Strategic technical influence** through business-informed decisions
- **Sustainable learning** embedded in existing responsibilities

## Getting Started

1. Copy the relevant agent prompts to your AI tool of choice
2. Start with the **Code Context Domain Analyzer** for your next production review
3. Use the **Meeting Preparation Agent** before your next PM/PO meeting
4. Gradually integrate other agents into your existing workflows
5. Share successful insights with your team to build collective domain knowledge

Remember: The goal is to transform your existing responsibilities into domain learning opportunities, not to add new tasks to your already full schedule.