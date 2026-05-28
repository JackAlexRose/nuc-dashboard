# NUC Services Dashboard

Landing page for `nuc.jackrose.website` — links to all self-hosted services running on an Intel NUC.

## What it shows

- Service cards with names, descriptions, and status dots
- Direct links to each hosted app
- Responsive layout (single column on mobile, grid on desktop)

## Stack

- Static HTML + CSS
- nginx on port 80
- Departure Mono font
- Dark terminal aesthetic matching sibling dashboards

## Deploying

```bash
sudo cp index.html DepartureMono-Regular.woff2 /var/www/nuc-dash/
sudo cp nuc-dash.nginx /etc/nginx/sites-available/nuc-dash
sudo ln -sf /etc/nginx/sites-available/nuc-dash /etc/nginx/sites-enabled/
sudo nginx -t && sudo systemctl reload nginx
```

To add a new service, edit `index.html` and add a card to the grid.
