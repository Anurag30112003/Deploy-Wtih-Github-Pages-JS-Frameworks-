# Deploy in Github-pages


## Install Github Pages
    npm install -g ghpages

## Create a new branch
    git checkout -b gh-pages

## Run the production build
    npm run build

##  Remove the dist folder from .gitignore file
    dist from .gitignore

## Or Copy the contents of the dist folder into the gh-pages branch
    cp -R dist/* .

## Make sure to make all path to absolute path  
    By adding '.' (dot) in front of the path, it will be converted to absolute path.

## Add following in package.json
    "type": "module"

## Make a new file gh-pages.js and add the following into it.(Make sure to add your own details)
    // var ghpages = require('gh-pages');
    import ghpages from 'gh-pages';

    ghpages.publish(
        'dist', // path to public directory
        {
            branch: 'gh-pages',
            repo: 'https://github.com/username/yourproject.git', // Update to point to your repository  
            user: {
                name: 'Your name', // update to use your name
                email: 'Your Email address' // Update to use your email
            }
        },
        () => {
            console.log('Deploy Complete!')
        }
)

## Add all files
    git add .

## Commit the changes
    git commit -m "Deploy to GitHub Pages"

## Push the branch to the remote
    git push origin gh-pages

## Run the gh-pages file
    node ./gh-pages.js


#### Don't forget to add the following your username ,email and githubrepo in the gh-pages.js file.
