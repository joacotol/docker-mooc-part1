FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY . .

EXPOSE 5000


RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

#RUN apt install update && apt install -y ca-certificates curl gnupg
#RUN curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
#RUN echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list
#RUN sudo apt-get update && sudo apt-get install nodejs -y
RUN npm install
RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
