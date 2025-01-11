# Resume Creator Monorepo

This monorepo contains both the frontend and backend services for the Resume Creator application, managed using git submodules.

## Initial Setup

Clone the repository with submodules:
```bash
git clone --recursive https://github.com/condyl/resume-creator.git
cd resume-creator
```

If you already cloned the repository, initialize submodules with:
```bash
git submodule update --init --recursive
```

## Project Structure

- `frontend/`: Next.js application deployed on Vercel
- `backend/`: Node.js backend service deployed on DigitalOcean

## Development

Each project maintains its own dependencies and can be developed independently.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Backend

```bash
cd backend
npm install
npm run dev
```

## Deployment

- Frontend: Automatically deployed through Vercel
- Backend: Deployed to DigitalOcean droplet

## Environment Variables

Make sure to set up appropriate environment variables for both projects:

- Frontend: Configure through Vercel dashboard
- Backend: Configure on your DigitalOcean droplet

## Working with Submodules

### Pulling Updates

To update all submodules to their latest versions:
```bash
git submodule update --remote --merge
```

### Making Changes

1. For frontend changes:
   ```bash
   cd frontend
   # Make your changes
   git add .
   git commit -m "Your commit message"
   git push
   cd ..
   git add frontend  # Update the submodule reference
   git commit -m "Update frontend submodule"
   git push
   ```

2. For backend changes:
   ```bash
   cd backend
   # Make your changes
   git add .
   git commit -m "Your commit message"
   git push
   cd ..
   git add backend  # Update the submodule reference
   git commit -m "Update backend submodule"
   git push
   ```

### Switching Branches in Submodules

If you need to work on a different branch in a submodule:
```bash
cd frontend  # or backend
git checkout your-branch
cd ..
git add frontend  # or backend
git commit -m "Switch frontend to your-branch"
git push
``` 