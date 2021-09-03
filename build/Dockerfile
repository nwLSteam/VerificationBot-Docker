# syntax=docker/dockerfile:1.3

FROM node:16

ENV NODE_ENV=production
WORKDIR '/app'

# install git
RUN ["apt", "install", "-y", "git"]

# clone to /app
RUN ["git", "clone", "-b", "develop", "https://github.com/Visate/VerificationBot", "."]
RUN ["npm", "i"]

# run
CMD ["node", "index.js"]