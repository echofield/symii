# Reliable

Commitment platform. Put money on it.

Built on SYMIONE protocol.

## Features

- **Solo** — Challenge yourself with real stakes
- **Duel** — 1v1 challenges with a friend
- **Cell** — Group challenges
- **Templates** — Fork and deploy your own challenge app

## Setup

```bash
# Clone
git clone https://github.com/echofield/symii.git
cd symii

# Install
npm install

# Configure
cp .env.example .env.local
# Edit .env.local with your values

# Run
npm run dev
```

## Deploy

Push to main. Vercel auto-deploys to reliable.app.

## Environment Variables

| Variable | Description |
|----------|-------------|
| `NEXT_PUBLIC_API_URL` | SYMIONE API endpoint (Cloud Run) |
| `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY` | Stripe publishable key |

## Architecture

```
reliable/ (this repo)
    ↓ HTTP
SYMIONE API (Cloud Run)
    ↓
Stripe Connect
```

This is a standalone frontend. All business logic lives in the SYMIONE API.

## License

MIT
