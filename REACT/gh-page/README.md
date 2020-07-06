# GITHUB PAGES FOR REACT
You can directly host github as a static page from github pages
## starting

- add ```"homepage": "https://<your/organisation_github_id>.github.io/<your_repo_name>",```  in package.json

- add
```
"predeploy": "npm run build",
"deploy": "gh-pages -d build",
```
in "scripts" of package.json
- run
```
npm install gh-pages --save-dev 
```
from project folder 

-nice you have completed set up
- push to git as you do every time
- deploy when needed

## deployment
- run ```npm run deploy``` from project folder
- run this every time you pushed
