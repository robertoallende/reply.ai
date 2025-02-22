# reply.ai

An intelligent email management system built on Amazon Q Apps that helps prioritize and respond to emails based on user roles and goals.

## Overview

reply.ai is a powerful email assistant that leverages Amazon Q's generative AI capabilities to help users manage their email workflow more efficiently. The application analyzes incoming emails, prioritizes them based on user-defined criteria, and generates contextually appropriate responses while tracking actions.

## Features

- Email prioritization based on user role and goals
- AI-powered response generation
- Action item extraction and tracking
- Role-based email handling
- Goal-oriented email management

## Architecture

### Current Version (v1.0)

The current version is implemented as a standalone Amazon Q App with the following components:

#### Inputs
- User information
- Role definition
- Goal parameters
- Email data

#### Outputs
- Prioritized email lists
- Generated email responses
- Extracted actions

#### Architecture Diagram

<img width="840" alt="current-architecture" src="https://github.com/user-attachments/assets/3e74e8f3-5e26-4785-a40f-ea2e9c8806bd" />


### Next Version (v2.0)

The upcoming version will enhance the current architecture by incorporating external service integrations through plugins:

#### New Components
- Email Service Plugin: For email fetching and delivery
- Project Management Plugin: For action item tracking
- Action Plugin: For automated workflow triggers

#### Architecture Diagram

<img width="986" alt="next-version-architecture" src="https://github.com/user-attachments/assets/9f19d700-e1aa-41bc-bd60-022ca7ea3341" />


## Getting Started

### Prerequisites

- AWS Account with appropriate permissions
- Access to Amazon Q Business
- Basic understanding of AWS services

For an intrduction on Amazon Q Business, Amazon Q Apps and how to get started, watch 
[Revolutionize Workplace Efficiency with Amazon Q Apps: AI-Powered Task Automation for Every Employee](https://aws.amazon.com/awstv/watch/65709eacee0/)
and
[Simplify Company Policies: Create an Amazon Q App for Instant Document Access](https://aws.amazon.com/awstv/watch/b17f4af1716/).

### Deployment

1. Log into your AWS Console
2. Navigate to Amazon Q Apps
3. Create a new Q App
4. Use the prompt instructions below to configure your app

### Prompt Instructions

```verbatim
reply.ai: Email Priority Assistant
Function: Analyze emails, display them in a priority-sorted list based on priority and generate replies for every email.

Input:
All of them are Text Input Fields:
- Emails Data (content of emails)
- User Name (full name) (default value Michael Scott)
- User Role (position) (default value Scranton Regional Manager)
- User Goal (current priority) (default value Boost Sales)
- Priority Levels (default "Urgent, High, Medium, Low")

Priority Evaluation Factors:
1. Goal alignment
2. Sender hierarchy
3. Urgency markers
4. Required actions
5. Deadlines
6. Sentiment

Email Prioritization Output:
- Use a restructured Text table as format
- One row per email
- Structure: column 1: {priority}, column 2: {date}, column 3: {subject}, column 4: {from}
- Sort order: By priority (highest to lowest), then by date
- No introductory text or rationale
- Only show the prioritized list

Email Writer Assistant Output:
You are an expert email writer assistant. Write one answer per email professional and effective emails.
1. Maintain professional language while adapting to specified goal
   Break long paragraphs into digestible chunks
   Include appropriate greeting and closing
2. Content Structure:
   - Start with a clear purpose statement
   - Present information in logical order
   - End with a clear call to action or next steps
3. Context Awareness:
   - If replying, acknowledge relevant points from previous email
   - Maintain thread context
   - Reference any shared history or previous conversations when available
4. Formatting:
   - Use appropriate paragraph breaks
   - Keep sentences and paragraphs concise
   - Include bullet points only when listing multiple items
5. Tone Guidelines:
   Formal:
   - Use complete sentences
   - Avoid contractions
   - Maintain professional distance
   Casual:
   - Can use contractions
   - More conversational flow
   - Friendly but still professional
   Friendly:
   - Can use warm language
   - More personal touches
   - Still maintaining business appropriateness

RESPONSE FORMAT:
Subject: [Generate appropriate subject if new email]
[Greeting]
[Body Content]
[Closing]
[Signature]

CONSTRAINTS:
- Never include sensitive or confidential information
- Maintain professional language regardless of tone
- Keep responses focused and relevant to the purpose
- Avoid overly complex or technical language unless specified
- Don't use excessive formatting or special characters

Separate every email content by using "----------"

Action List Output:
This is a list of tasks based on the emails responses.
Format: Priority, Email Subject, List of actions using bullet point. One Action per line.
```

### Testing Your Deployment

1. After deployment, test with sample email data
2. Verify prioritization logic
3. Check email response generation
4. Validate action item extraction
5. Test with different user roles and goals

## Authors

- [James Green - Busines Co Founder](https://www.linkedin.com/in/james-w-green/)
- [Roberto Allende - Technical Co Founder](https://www.linkedin.com/in/robertoallende/)

## License

[MIT License](https://github.com/robertoallende/reply.ai/edit/main/README.md).

## Hackathon Winner

This project has been built with Amazon Q Apps in just two hours at the AWS & Ingram Micro GenAI Hackathon in Auckland 2025.

## A Word of Thanks

The development of Reply.ai wouldn't have been possible without the support and guidance of the AWS & Ingram Micro GenAI Hackathon organizers. Special thanks go to Andrei Lizarraga and Vivian Weiwei Luo, whose expertise and dedication helped shape this project and many others during the event.

---
Built with ❤️ using Amazon Q Apps
