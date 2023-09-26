## Requirements
- Docker Compose

## Deployment
- initialize and update submodules
`git submodule init`
`git submodule update`
- run docker compose `docker-compose up --build -d`

## Add new App
- add submodule of your app
`git submodule add url-to-git-repository name-of-app`
- add your app as service to the docker compose file
- add your locally mounted workspaces directory to `.gitignore` file
- run docker compose `docker-compose up --build -d`

## Update your App
`cd your-app-submodule-directory`
`git pull origin main`
`cd ..`
`git status`
`git add .`
`git commit -m "updated submodule"`
`git push origin main`