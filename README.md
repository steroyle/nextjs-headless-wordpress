## Overview

- **Backend** - Headless WordPress (http://localhost:3000) installed using roots.io and API provided by (http://localhost:9023/wp/graphql)
- **Frontend** - Next.js

## Installation

### Backend (Wordpress)
```
cd backend
composer install
```
Copy `.env.example` to `.env` file and update:

**Database variables**
```
DB_NAME='YOUR_DATABASE_NAME'
DB_USER='YOUR_DATABASE_USER'
DB_PASSWORD='YOUR_DATABASE_PASSWORD'
```
**Site details**
```
WP_ENV='development'
WP_HOME='http://localhost:9023'
WP_SITEURL="${WP_HOME}/wp"
```

Installing theme deps and running locally
```
cd web/app/themes/headless-wordpress-theme
npm install
npm run dev
```
Generate new with salts with roots.io [WordPress salts generator](https://roots.io/salts.html)

- Headless theme is located in `web/app/themes/headless-wordpress-theme`
- Set the document root on your webserver to Bedrock's `web` folder: `/path/to/site/web/`
- Access WordPress admin at `https://localhost:9023/wp/wp-admin/`
