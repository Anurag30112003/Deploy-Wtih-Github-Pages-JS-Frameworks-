# Deploy in gh-pages
[]: # Language: shell
 
 ## Install GithubPages
    npm install -g ghpages
## Create a new branch
    git checkout -b gh-pages
## Run the production build
    npm run build
##  Remove the dist folder from .gitignore file
    cp -R dist/* .
### Or Copy the contents of the `dist` folder into the `gh-pages` branch

## Make sure to make all path to absolute path
    By adding '.' (dot) in front of the path, it will be converted to absolute path.
## Add following in package.json
    "type": "module"
## Add all files
    git add .
## Commit the changes
    git commit -m "Deploy to GitHub Pages"
## Push the branch to the remote
    git push origin gh-pages
## Run the gh-server file
    node ./gh-pages.js

#### Don't forget to add the following your username ,email and gitrepo in the gh-pages.js file.
