# Bracket Brawl Live

Real-time browser tournament game for player, host/admin, and big-screen views.

## Run locally

Open `dist/index.html` directly, or serve the `dist` folder with any static web server:

```powershell
python -m http.server 8000 --directory dist
```

Then open `http://localhost:8000/index.html`.

## Views

- Player: `?view=play&room=room-07`
- Host/admin: `?view=host&room=room-07`
- Big screen: `?view=display&room=room-07`

## Deployment

The project is a static site. Deploy the `dist` folder with Firebase Hosting, Vercel, Netlify, or another static host. Configure the custom domain in the hosting provider after deployment.

## Important production checklist

- Use Firebase Blaze for events with more than 100 simultaneous connections.
- Replace the temporary client-side admin login with Firebase Authentication and protected Realtime Database rules.
- Never commit production passwords or private service-account keys.
- Reset the event room before each tournament and verify the host and display links on real phones.
