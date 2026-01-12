FROM node:22-alpine
RUN apk add --no-cache git

RUN git config --system --add safe.directory /workspace

WORKDIR /workspace/backend

COPY package*.json ./
RUN npm install && npm cache clean --force
COPY . .

EXPOSE 3000

CMD ["npm", "run", "dev"]