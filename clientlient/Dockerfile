FROM node:18-alpine
RUN apk add --no-cache \
      python3 \
      make \
      g++ \
      cairo-dev \
      pango-dev \
      giflib-dev

RUN ln -sf /usr/bin/python3 /usr/bin/python

ENV PYTHON=/usr/bin/python3

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install --only=production

COPY . .

EXPOSE 3000

CMD ["node", "app.js"]

