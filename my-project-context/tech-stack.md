# Tech Stack

| Layer | Service | Notes |
|-------|---------|-------|
| Frontend | React & Vite | Core tools used to build the web app and its components |
| Styling | Tailwind CSS | Used to create a clean, professional interface with consistent buttons, typography, and color |
| Backend | Supabase Edge Functions | Server-side logic that acts as the bridge between the app and the AI model |
| Database | PostgreSQL | Stores user profiles, health history, and prior chat conversations |
| Authentication | Supabase Auth | Handles secure email/password login, session management, and protected data access |
| AI Model | Gemini 2.5 Flash | Reads user symptoms and provides educational health information |
| Version Control | GitHub | Tracks code changes and supports team collaboration |
| Hosting | Vercel | Hosts the live web application |
| UI Icons | Lucide Icons | Provides lightweight icons such as send and user icons used throughout the app |

## Architecture Notes
Health Insight AI uses a React and Vite frontend for the user experience, styled with Tailwind CSS. User requests flow through Supabase Edge Functions, which handle application logic and communicate with Gemini 2.5 Flash to generate conversational health guidance. Supabase Auth manages secure login and protected sessions, while PostgreSQL stores persistent application data such as profiles, health history, conversation metadata, and chat records. GitHub and Vercel support collaboration and deployment.
