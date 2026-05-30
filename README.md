# WeddingClikz - Admin Console

This is the admin dashboard for managing WeddingClikz.

## GitHub Pages Deployment

1. Create a new GitHub repository (e.g., `weddingclikz-admin`)

2. **Update the Backend URL** in `index.html`:
   - Find the line: `const BACKEND_URL = 'https://your-backend-server.com';`
   - Replace with your actual backend URL (e.g., `https://api.weddingclikz.com`)

3. Push all files to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_ORG/YOUR_REPO.git
   git push -u origin main
   ```

4. Enable GitHub Pages:
   - Go to repository Settings → Pages
   - Source: Deploy from branch
   - Branch: main, / (root)
   - Save

5. Your admin console will be available at:
   - `https://YOUR_ORG.github.io/YOUR_REPO/`
   - Or configure a custom subdomain (e.g., `admin.weddingclikz.com`)

## Custom Subdomain Setup

1. Add a `CNAME` file with your subdomain:
   ```
   admin.weddingclikz.com
   ```

2. Configure DNS:
   - Add a CNAME record for `admin` pointing to `YOUR_ORG.github.io`

## Security Note

- This admin console uses JWT authentication
- Tokens are stored in localStorage
- Always use HTTPS for both frontend and backend
- Consider making this repository private

## Files

- `index.html` - Admin dashboard application
- `logo.png` - WeddingClikz logo  
- `favicon.ico`, `apple-touch-icon.png` - Favicons

## Features

- Dashboard with statistics
- Events management (CRUD)
- Services management with category pricing
- Quotes management with search/filter
- Users management
- Admin users management (superadmin only)
- Notification email settings
