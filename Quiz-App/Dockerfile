FROM node:14-alpine as base

WORKDIR /app
RUN mkdir quizzapp
WORKDIR /app/quizzapp

COPY package*.json ./

RUN npm install
COPY . .

RUN npm run build

FROM node:14-alpine

COPY --from=base /app/quizzapp ./
EXPOSE 3001
ENTRYPOINT ["npm","start"]
