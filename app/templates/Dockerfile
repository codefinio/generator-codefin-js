FROM node:8-alpine
WORKDIR /app
ADD package.json /app/package.json
RUN yarn install
ADD src /app/src
ADD .babelrc /app/.babelrc
ADD .eslintrc /app/.eslintrc
RUN yarn run build
CMD ["node", "build/index.js"]
ENTRYPOINT [ "/bin/sh" ]