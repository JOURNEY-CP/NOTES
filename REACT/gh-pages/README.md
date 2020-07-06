# GITHUB PAGES FOR REACT
You can directly host github as a static page from github pages
## starting

#### full procedure
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

- nice you have completed set up
- push to git as you do every time
- deploy when needed
#### code
run this code to do all the above points at once 🙂🙂🙂

!!!!!!!!note: works fine for default readme file which is generated at first of create-react-app 

!!!!!!!!so be cautious to use this code directly
```
sed -i '5i\  "homepage": "http://gitname.github.io/react-gh-pages",' ./package.json
sed -i '15i\    "predeploy": "npm run build",' ./package.json
sed -i '16i\    "deploy": "gh-pages -d build",' ./package.json
npm install gh-pages --save-dev
```

## deployment
- run ```npm run deploy``` from project folder
- run this every time you pushed
