FROM node:10.15.1
WORKDIR ~/project/docker
COPY package*.json ./
RUN npm install
COPY privkey.pem /etc/letsencrypt/live/org-plannerapi.symple.co.in/privkey.pem
COPY cert.pem /etc/letsencrypt/live/org-plannerapi.symple.co.in/cert.pem
COPY . .
EXPOSE 8015
CMD [ "npm", "start" ]
