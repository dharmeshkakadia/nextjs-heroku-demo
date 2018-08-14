nextjs-heroku-demo
==================

1. Start the project `mkdir my-app && cd my-app`
2. Setup next `npm init -y && npm install --save react react-dom next`
3. Git setup `git init && (echo node_modules/ && echo .next/) >> .gitignore`
4. Add code `mkdir pages && touch pages/index.js`
5. Create Heroku app `heroku create`
6. Tell it how to run by adding following in 
    ```
    {
      "scripts": {
        "dev": "next",
        "build": "next build",
        "start": "next start -p $PORT",
        "heroku-postbuild": "npm run build"
      }
    }
    ```
6. Publish 
    ```
    git add .
    git commit -m 'Next.js app on Heroku'
    git push heroku master
    ```