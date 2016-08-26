# hireable
[![Build Status](https://travis-ci.org/hiendv/hireable.svg?branch=master)](https://travis-ci.org/hiendv/hireable)

Available-for-hire badge built with [Koa framework](https://github.com/koajs/koa)

[![Is hiendv available for hire?](https://hireable.0x1115.org/hiendv)](https://hireable.0x1115.org/p/hiendv)

```
[![Is <username> available for hire?](https://hireable.0x1115.org/<username>)](https://hireable.0x1115.org/p/<username>)
```
*`<username>` is a GitHub username*

Sorry for the long domain, couldn't afford a short one :dollar:

## But why?
Some of my friends want to embed the employment status into their open-source projects.
But it takes too much time and effort to keep these information up-to-date across your projects.  
I thought it would be much cooler to tell people whether you're hireable or not with a badge. Isn't it? :confused:

## The badges
![Hireable](https://cdn.rawgit.com/hiendv/hireable/master/public/hireable-yes.svg)
![Not hireable](https://cdn.rawgit.com/hiendv/hireable/master/public/hireable-no.svg)
![Error](https://cdn.rawgit.com/hiendv/hireable/master/public/hireable-error.svg)

I was too lazy to implement [badges/shields specification](https://github.com/badges/shields/blob/master/spec/SPECIFICATION.md)  
No on-the-fly generated badges for now, I guess. They are all pre-generated. 

- Q: **How do you know when I'm hireable?**  
A: Your [GitHub jobs profile](https://github.com/settings/profile#user_profile_hireable)

- Q: **Cache expiration**  
A: GitHub has their own image proxy: [camo](https://help.github.com/articles/why-do-my-images-have-strange-urls/). Hireable caching is flexible, see [Configurations](#configurations)

## Quickstart Installation
- Download the latest release [here](https://github.com/hiendv/hireable/releases)
```bash
# Unzip
unzip hireable-v*.zip -d hireable && cd hireable

# Dependencies
npm install --production

# Config. See #configurations
vim .env

# Serve
npm run serve

# Or even better with pm2 or forever
```

## Configurations
Configurations are defined in `.env` file.
```
# Application port
APP_PORT=1406

# Cache expiration in ms. Leave it null to disable
APP_CACHE=

# GitHub personal access token. See https://github.com/settings/tokens
GITHUB_TOKEN=PersonalAccessToken
```

## Development
- C'mon, give it a :star:. Thank you :laughing:
```bash
git clone https://github.com/hiendv/hireable.git && cd hireable
npm install
cp .env.example .env && vim .env
npm run dev

# Create a release?
npm run build && cd build
```

## Testing
```bash
npm test
```
e2e test PRs are welcome!
