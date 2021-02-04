# Publishing to Heroku

## To Publish a Single Project

### Create app
- Create app here [heroku](https://dashboard.heroku.com/) with app name of your choice
- your website link will be  ```<your-app-name>.herokuapp.com```

### Add remote
- Add remote to your git. 
- run ```git remote add heroku https://git.heroku.com/<your-app-name>.git```

### publish to heroku
- git push heroku master

Thats it your app is published (login if asked)

## To Publish A full Stack Project havng 2 folders

### Create Apps
- create 2 apps one for frontend and one for backend

### Add Remote
- run ```git remote add herokufront https://git.heroku.com/<your-frontend-app-name>.git```
- run ```git remote add herokuback https://git.heroku.com/<your-backend-app-name>.git```

### Publish to heroku
- run ```git subtree push --prefix <your_frontend_path> herokufront master```
- run ```git subtree push --prefix <your_backend_path> herokuback master```
