# HoloPass - Multichain Digital Identity Platform

[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?style=for-the-badge&logo=vercel)](https://vercel.com/hellthere112-1801s-projects/v0-holo-pass-digital-identity)
[![Built with v0](https://img.shields.io/badge/Built%20with-v0.app-black?style=for-the-badge)](https://v0.app/chat/projects/ZeEKjD79VyT)

## 🌟 Overview

HoloPass is a revolutionary multichain digital identity platform that acts as a gamified passport for the Web3 ecosystem. It unlocks exclusive access across real-world events, online communities, and retail experiences through dynamic, upgradeable NFTs.

### 🎯 Core Features

- **🎫 Event & Venue Access** - Scan QR codes via WalletConnect for entry into concerts, meetups, conferences, and private lounges
- **🏛️ Exclusive Communities** - Access token-gated Discord channels, DAO voting, and beta product trials
- **🛍️ Retail & Hospitality Perks** - Partner verification for discounts, special items, and NFT-only deals
- **🎮 Dynamic Gamification** - Earn on-chain stamps for attending events and completing challenges
- **📱 Social Integration** - Showcase achievements on Twitter, Lens, and Farcaster profiles

## 🛠️ Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS v4, Radix UI, shadcn/ui
- **Web3**: Wagmi, Viem, RainbowKit, WalletConnect
- **Blockchain**: Ethereum, Polygon, Optimism, Arbitrum, Base
- **Database**: Supabase (PostgreSQL)
- **Authentication**: Supabase Auth + Web3 Wallet Signatures
- **QR Codes**: @yudiel/react-qr-scanner, qr-code-styling
- **External APIs**: Eventbrite API for live events

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and pnpm
- Supabase account
- WalletConnect Project ID
- (Optional) Eventbrite API token

### Installation

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/hellhack-ui/HoloPass.git
   cd HoloPass
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   pnpm install
   \`\`\`

3. **Set up environment variables**
   \`\`\`bash
   cp .env.local.example .env.local
   \`\`\`

4. **Configure your `.env.local`**
   \`\`\`env
   # Supabase Configuration (Auto-configured in v0)
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key
   
   # Web3 Configuration
   NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=your_walletconnect_project_id
   
   # External APIs (Optional)
   EVENTBRITE_PRIVATE_TOKEN=your_eventbrite_private_token
   \`\`\`

5. **Set up the database**
   \`\`\`bash
   # Run database migrations
   pnpm run db:setup
   \`\`\`

6. **Start the development server**
   \`\`\`bash
   pnpm dev
   \`\`\`

Visit `http://localhost:3000` to see your HoloPass application.

## 🗄️ Database Schema

The application uses the following main tables:

- **`users`** - User profiles and wallet addresses
- **`events`** - Event information and metadata
- **`rsvps`** - Event registrations and attendance tracking
- **`check_ins`** - QR code-based event check-ins
- **`stamps`** - Achievement stamps and rewards
- **`user_stamps`** - User's collected stamps and XP

## 🔌 API Endpoints

### Events Management
- `GET /api/events` - Fetch events with filtering
- `POST /api/events` - Create new events
- `GET /api/events/[id]` - Get specific event
- `PUT /api/events/[id]` - Update event
- `DELETE /api/events/[id]` - Delete event

### User Interactions
- `POST /api/events/[id]/rsvp` - RSVP to events
- `POST /api/events/[id]/checkin` - Check into events via QR

## 🎮 Key Features

### Digital Passport Display
- View your HoloPass NFT with collected stamps
- Track XP progression and achievements
- Display rarity and tier status

### QR Code System
- Generate unique QR codes for events
- Real-time camera scanning for check-ins
- Automatic stamp rewards upon successful scan

### Event Discovery
- Browse live events from Eventbrite API
- Filter by category, location, and date
- RSVP system with capacity management

### Web3 Integration
- Multi-wallet support (MetaMask, WalletConnect, Coinbase)
- Smart contract interactions for NFT management
- Cross-chain compatibility

## 🔧 Configuration

### WalletConnect Setup
1. Visit [WalletConnect Cloud](https://cloud.walletconnect.com/)
2. Create a new project
3. Copy the Project ID to your `.env.local`

### Eventbrite Integration
1. Create an [Eventbrite developer account](https://www.eventbrite.com/platform/api)
2. Generate a private token
3. Add to your environment variables

## 🚀 Deployment

The project is configured for deployment on Vercel:

1. **Connect your repository** to Vercel
2. **Set environment variables** in Vercel dashboard
3. **Deploy** - Vercel will automatically build and deploy

Your live application: **[https://vercel.com/hellthere112-1801s-projects/v0-holo-pass-digital-identity](https://vercel.com/hellthere112-1801s-projects/v0-holo-pass-digital-identity)**

## 📱 Demo

Watch the HoloPass demo: [https://youtu.be/3Exx5KUKmyg](https://youtu.be/3Exx5KUKmyg)

## 🤝 Contributing

This project is built with [v0.app](https://v0.app). Continue development at:
**[https://v0.app/chat/projects/ZeEKjD79VyT](https://v0.app/chat/projects/ZeEKjD79VyT)**

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 Links

- **Live Demo**: [Vercel Deployment](https://vercel.com/hellthere112-1801s-projects/v0-holo-pass-digital-identity)
- **Development**: [v0.app Project](https://v0.app/chat/projects/ZeEKjD79VyT)
- **Demo Video**: [YouTube](https://youtu.be/3Exx5KUKmyg)

---

Built with ❤️ using [v0.app](https://v0.app) - The AI-powered development platform
