FROM node:16-stretch
LABEL maintainer="jf@perrin.at"

ENV INSTALL_PATH=/calendso 

WORKDIR $INSTALL_PATH
RUN mkdir -p $INSTALL_PATH
RUN git clone https://github.com/calendso/calendso.git $INSTALL_PATH
COPY .env $INSTALL_PATH
RUN npm install prisma -y
RUN npm audit fix

CMD npx prisma db push && yarn dev