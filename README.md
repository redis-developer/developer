## Getting Started with Docusaurus

Say, you want to host site in your GITHUB repository.
First clone the repostiory where you want to host it as shown below:


```
git clone https://github.com/redis-developer/developer
```

## Installing via npx


```
npx @docusaurus/init@next init redisdoc classic
```

## Building

```
yarn build
```


## Make changes under ```docusaurus.config.js``` file

```
% cat docusaurus.config.js                  
module.exports = {
  title: 'My Site',
  tagline: 'The tagline of my site',
  url: 'https://redis-developer.github.io',
  baseUrl: '/developer/',
  onBrokenLinks: 'throw',
  favicon: 'img/favicon.ico',
  organizationName: 'Redis-Developer', // Usually your GitHub org/user name.
  projectName: 'developer', // Usually your repo name.
  themeConfig: {
    navbar: {
      title: 'Redis Developer Site',
      logo: {
        alt: 'My Site Logo',
        src: 'img/logo.svg',
```

## Creating script to build the site

$ cat publish-gh-pages                      
```
GIT_USER=ajeetraina \
  CURRENT_BRANCH=master \
  USE_SSH=true \
  yarn run publish-gh-pages # or `npm run publish-gh-pages`
ajeetraina@Ajeets-MacBook-Pro redisdoc %
```


## Pushing it to GITHUB repository

```
GIT_USER=ajeetraina USE_SSH=true yarn deploy
```
