# Crossfire - Marvel Rivals Counter Guide

> The Marvel Rivals Counter Decision Engine by **Dracyan**

A knowledge-first, AI-assisted counter picking guide for Marvel Rivals. Crossfire helps players make better decisions in ranked play by providing hero-specific counter strategies, problem-based solutions, and fundamental counter principles.

![Crossfire](https://img.shields.io/badge/Crossfire-Marvel%20Rivals-blue?style=for-the-badge)
![React](https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-3178C6?style=for-the-badge&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-5.4.19-646CFF?style=for-the-badge&logo=vite)

##  Features

- **Hero Counter Database** - Comprehensive counter information for all Marvel Rivals heroes
- **Problem-Based Search** - Find solutions based on in-game problems ("I keep getting dived" → Solutions)
- **Counter Principles** - Understand WHY counters work with fundamental game mechanics
- **Tier Rankings** - Visual tier system with prominent badges for best/worst heroes
- **AI Coach** - Optional AI assistant powered by OpenRouter (bring your own API key)
- **Beautiful UI** - Dark theme with character background images and smooth animations
- **Quick & Deep Modes** - Toggle between quick summaries and detailed analysis

##  Hero Information

Each hero page includes:

- **Tier Ranking** - S, A, B, C tiers with special "BEST" and "WORST" badges
- **Danger Assessment** - What makes the hero dangerous
- **Core Counter Principle** - The fundamental strategy to counter them
- **Key Abilities & Cooldowns** - Important abilities to track
- **Role-Specific Counters** - How to counter as Vanguard, Duelist, or Strategist
- **Direct Counters** - Specific heroes that counter them and why
- **Common Mistakes** - What not to do
- **Ultimate Counterplay** - How to handle their ultimate

##  Getting Started

### Prerequisites

- Node.js 18+ and npm (or use [nvm](https://github.com/nvm-sh/nvm#installing-and-updating))

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd counter-rivals

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:8080`

### Build for Production

```bash
# Build the project
npm run build

# Preview production build
npm run preview
```

##  Tech Stack

- **Vite** - Build tool and dev server
- **React 18** - UI framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **shadcn-ui** - UI components
- **React Router** - Navigation
- **TanStack Query** - Data fetching
- **OpenRouter API** - AI coach (optional)

##  Project Structure

```
counter-rivals/
├── public/
│   └── Rivals/          # Character images
├── src/
│   ├── components/      # React components
│   │   ├── HeroPage.tsx
│   │   ├── HomeView.tsx
│   │   ├── ProblemSearch.tsx
│   │   ├── PrinciplesView.tsx
│   │   ├── AIPanel.tsx
│   │   └── ui/          # shadcn-ui components
│   ├── data/
│   │   └── heroCounters.ts  # Hero data and counter information
│   ├── pages/
│   │   └── Index.tsx    # Main page component
│   └── index.css        # Global styles
└── package.json
```

##  Usage

### Searching Heroes

- Use the search bar to find heroes by name
- Browse by role (Vanguard, Duelist, Strategist) in the sidebar
- Click any hero to view their detailed counter page

### Problem-Based Search

Navigate to "Search by Problem" to find solutions for common in-game situations:
- "I keep getting dived"
- "This hero won't die"
- "Ult wipes us every fight"
- And more...

### Counter Principles

Learn the fundamental mechanics that govern counters:
- CC Beats Mobility
- Burst Beats Shields
- Range Beats Melee
- And more...

### AI Coach

1. Click the "AI Coach" button in the header
2. Enter your OpenRouter API key (get one free at [openrouter.ai](https://openrouter.ai))
3. Ask questions about counters, strategies, or team compositions
4. The AI is grounded in the knowledge base and won't invent information

##  Customization

### Adding New Heroes

Edit `src/data/heroCounters.ts` and add a new hero object to the `heroCounters` array:

```typescript
{
  id: 'hero-id',
  name: 'Hero Name',
  role: 'vanguard' | 'duelist' | 'strategist',
  tier: 'S' | 'A' | 'B' | 'C',
  isBest?: true,  // Optional: mark as best in role
  isWorst?: true, // Optional: mark as worst in role
  danger: 'Description of what makes them dangerous',
  corePrinciple: 'The core counter strategy',
  // ... other required fields
}
```

### Adding Character Images

Place character images in `public/Rivals/` with the filename matching the hero's image mapping in `HeroPage.tsx`.

##  License

This project is created by Dracyan. All rights reserved.

##  Acknowledgments

- Marvel Rivals community for gameplay insights
- Built with love for the competitive Marvel Rivals scene

##  Contact

Created by **Dracyan**

---

**Note**: This is a fan-made tool and is not affiliated with or endorsed by Marvel or NetEase Games.
