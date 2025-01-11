# Resume Creator Monorepo

This monorepo contains both the frontend and backend services for the Resume Creator application.

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

## Contributing

When making changes:

1. For frontend-only changes:
   ```bash
   cd frontend
   # Make your changes
   git add .
   git commit -m "Your commit message"
   git push origin master
   ```

2. For backend-only changes:
   ```bash
   cd backend
   # Make your changes
   git add .
   git commit -m "Your commit message"
   git push origin main
   ```

3. For changes affecting both:
   - Make your changes in respective directories
   - Commit and push to both repositories
   - Update the monorepo with:
     ```bash
     git add .
     git commit -m "Update both frontend and backend"
     git push
     ``` 