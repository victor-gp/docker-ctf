FROM alpine:3.12
WORKDIR /home/
RUN apk add --no-cache git
RUN git clone https://github.com/thedojoseries/react-todo-backend.git

FROM alpine:3.12
RUN apk add --no-cache nodejs npm
COPY --from=0 /home/react-todo-backend /home/react-todo-backend
WORKDIR /home/react-todo-backend
RUN npm install
CMD ["npm", "run", "server-dev"]
