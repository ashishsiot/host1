# Host React + Vite Project on Gitub Pages.

## In the package.json file add these lines in scripts before "build": "vite build"
```json
"predeploy": "npm run build",
"deploy": "gh-pages -d dist",
```

## In the vite.config.js file add this line before plugins: [react()],

```js
base: "/YOUR_REPOSITORY_NAME",
```

## Create repo on GitHub 
### Type in terminal

```git
git init
git add .
git commit -m "Add existing project files to Git"
git remote add origin https://github.com/github_user_name/YOUR_REPOSITORY_NAME.git
git push -u origin main
```

```git
npm run build
git add dist -f
git commit -m "your_massge"
git subtree push --prefix dist origin gh-pages
```
