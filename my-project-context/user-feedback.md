# User Feedback Summary

## Source
User testing conducted with 3 early testers plus implementation observations from security hardening and authentication work.

## What Worked
- Testers were able to log in and use the chat successfully without outside guidance
- The core flow from signup to symptom entry to AI-generated insights worked end to end
- Nearby specialty recommendations and citation hyperlinks were valuable and understandable
- The chat history layout felt organized and useful
- Persistent profile and chat history created a more personalized experience across sessions

## Pain Points
- One tester was unsure how the product was meaningfully different from ChatGPT or other general AI tools
- The logged-out experience is currently too restrictive to demonstrate value before signup
- Some of the product differentiation still needs to be clearer at first glance

## Feature Requests
- A feature-gated guest model so users can try limited functionality before creating an account
- A symptom calendar
- A doctor review system
- More visible product differentiation compared with general AI chatbots

## Bugs & Broken Flows
- No broken links or empty states were identified in the main user flow
- Secure authentication, dashboard access, AI output generation, and data persistence all functioned as expected during testing

## Key Quotes
- "I was not sure how it was different from ChatGPT or another AI platform."
- She enjoyed that conversations were deletable and organized by time periods such as today, yesterday, and earlier.
- The feature-gated model would make the product more competitive with other AI platforms.

## Tester Notes

### Andrew Ingersoll
- Successfully logged in and asked, "Why am I so tired?"
- Received possible explanations and follow-up questions about daily activities and stressors
- Main feedback: the product differentiation versus ChatGPT was not obvious enough
- Change made: citation text was converted into hyperlinks to emphasize credibility, and the team brainstormed additional features

### Angelina Diaz
- Used the chat feature, tested hyperlinks, and explored nearby specialty recommendations
- Responded positively to the chat history organization and deletion controls
- Suggested a feature-gated model to improve competitiveness
- Change made: the team mapped out next-step feature improvements

### Lauryn Barnett
- Used the chat feature, saved profile information, and tested the difference between using the app with and without saved data
- Helped reveal how the AI handled stored conditions and medications in context
- Also supported the idea of a feature-gated model
- Change made: the team planned the next round of improvements

## Security and Trust Signals
- Session persistence was tightened by moving from `localStorage` to `window.sessionStorage`
- Ownership verification was added to protect generated summaries
- The health-chat endpoint now requires authenticated access
- A prompt injection scrubber now blocks known jailbreak attempts before they reach the model
