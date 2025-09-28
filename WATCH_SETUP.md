# Docker Compose Watch Setup

## Overview
Your Docker Compose is now configured with watch mode for efficient development workflow.

## How to Use

### Start with Watch Mode
```bash
docker compose up --watch
```

### Alternative: Separate Watch Command
```bash
# Start services
docker compose up -d

# Start watch mode separately (useful to separate logs)
docker compose watch
```

## What Happens

### Sync Action
- Changes to files in `./frontend/` are automatically synced to `/app/` inside the container
- The following are ignored:
  - `node_modules/` (for performance and compatibility)
  - `.next/` (build artifacts)
  - `.git/` (version control)
  - `Dockerfile*` (infrastructure files)
  - `README.md` (documentation)

### Rebuild Action
- Changes to `package.json` trigger a complete image rebuild
- This ensures new dependencies are properly installed

## Development Features
- Hot module replacement enabled through Next.js dev server
- Runs in development mode (`NODE_ENV=development`)
- Uses `npm run dev` with Turbopack for faster builds
- Anonymous volume for `node_modules` improves performance

## File Structure
- `Dockerfile.dev`: Development-optimized Docker image
- `Dockerfile`: Production-optimized Docker image (unchanged)
- `docker-compose.yaml`: Updated with proper watch configuration

## Benefits
- No need to rebuild images for code changes
- Fast hot-reload development experience
- Proper handling of Node.js dependencies
- Follows Docker best practices for watch mode