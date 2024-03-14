FROM node:14-alpine

WORKDIR /app
RUN mkdir quizz_app
WORKDIR /app/quizz_app

COPY package*.json ./

RUN npm install
COPY . .

RUN npm run build
EXPOSE 3001
CMD ["npm", "start"]
