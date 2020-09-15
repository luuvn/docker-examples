FROM node:12-alpine

RUN ["mkdir", "/app"]
RUN ["mkdir", "/install_node_module"]

WORKDIR /install_node_module
COPY package.json yarn.lock ./
RUN yarn install
ENV PATH /install_node_module/node_modules/.bin:$PATH
ENV NODE_PATH=/install_node_module/node_modules

WORKDIR /app
COPY . .

# CMD yarn run dev