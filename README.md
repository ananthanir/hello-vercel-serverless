# Hello Vercel Serverless
A simple NodeJs App for testing out the the [Vercel](https://vercel.com/) [Serverless functions](https://vercel.com/docs/concepts/functions/serverless-functions).

## How to Deploy a simple serverless function

First create a directory, using the command
```
mkdir hello-vercel-serverless
```
Change into the directory
```
cd hello-vercel-serverless
```
Initalsize node project

```
npm init
```
Create a new folder name `api` and create file named `hello.js` inside
```
mkdir api
nano hello.js
```

Paste the following code in `hello.js`
```
module.exports = (req, res) => {
    res.send('Hello World!');
}
```

Now run the command. 
```
vercel dev
```
Note: If you have not installed vercel cli, do y using `npm i -g vercel` 

Now configure it. 

```
hello-vercel-serverless> vercel dev
Vercel CLI 28.19.0
? Set up and develop “C:\worlds\hello-vercel-serverless”? [Y/n] y
? Which scope should contain your project? Ananthan
? Link to existing project? [y/N] n
? What’s your project’s name? hello-vercel-serverless
? In which directory is your code located? ./
Local settings detected in vercel.json:
No framework detected. Default Project Settings:
- Build Command: `npm run vercel-build` or `npm run build`
- Development Command: None
- Install Command: `yarn install`, `pnpm install`, or `npm install`
- Output Directory: `public` if it exists, or `.`
? Want to modify these settings? [y/N] n
🔗  Linked to ananthanir/hello-vercel-serverless (created .vercel)
> Ready! Available at http://localhost:3000
```
Note: Make sure to have a Vercel account as the first thing cli will ask to login.

Now go to http://localhost:3000/api/hello, to see the output. Finally use the following command to deploy it. 
```
vercel deploy
```

```
hello-vercel-serverless> vercel deploy
Vercel CLI 28.19.0
🔍  Inspect: https://vercel.com/ananthanir/hello-vercel-serverless/aTguvEhAiyYCASDFekjb45tDnALP [3s]
✅  Production: https://hello-vercel-serverless.vercel.app [11s]
📝  Deployed to production. Run `vercel --prod` to overwrite later (https://vercel.link/2F).
💡  To change the domain or build command, go to https://vercel.com/ananthanir/hello-vercel-serverless/settings
```