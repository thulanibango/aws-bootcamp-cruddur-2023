FROM node:16.18 AS build
ENV PORT=3000
COPY . /frontend-react-js
WORKDIR /frontend-react-js
RUN npm install

FROM node:16.18 AS run
EXPOSE ${PORT}
CMD ["npm", "start"]