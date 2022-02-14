# What's this?
This is a base project for building web apps. Use it as a bootstrap project to get coding quickly and avoid installing and initializing the same stuff all the time.
It uses Strapi as headless cms, SvelteKit for the web app and Postgres as the database. Powered by Docker to easily set up local development.


# How to use it
```
git clone git@github.com:sebastianschnock/web-app-base.git
cd web-app-base
rm -rf .git
git init
docker-compose up -d
```
This will copy the contents of the repo and initialize it as a new git project, ditching all history etc.
