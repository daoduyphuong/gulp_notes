# gulp_notes
Some useful notes about gulp

## Installing Gulp
Install global
```
sudo npm install gulp -g
```
Then install to project 
```
npm install gulp --save-dev
```

## Globing in Node
```
*.scss           // Match any file that have ext .scss in root dir
**/*.scss        // Match any file that have ext .scss in root and any child dir
!not-me.scss     // Not match not-me.scss
*.+(scss|sass)   // Match any file have ext .scss or sass
```
