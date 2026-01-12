FROM node:22-alpine

RUN apk add --no-cache git
RUN git config --system --add safe.directory /workspace

WORKDIR /workspace/frontend

COPY package*.json ./
RUN npm install & npm cache clean --force
COPY . .

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]