FROM node:14-alpine

ENV NODE_ENV production

WORKDIR /cli

RUN npm -g install @polkadot/api-cli

COPY ./types.json /cli/types.json

CMD ["polkadot-js-api"]