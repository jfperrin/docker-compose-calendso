# docker-compose-calendso

This is a quick project to use calendso in docker-compose with postgres.

## Getting stared 


### Clone the repo

```
git clone https://github.com/jfperrin/docker-compose-calendso.git
```

### Set up the enviroment

in the `docker` directory copy .env.example to .env and replace <user>, <pass>,<pg-admin-email>,<pg-admin-pass>, <pg-admin-port> and <google-api-secret> with their applicable values

### Launch 

```docker-compose up -d```

### Create user

Run the `npx prisma studio` command in the running container (`docker exec -it calendso bash`)

Open a browser to http://localhost:5555 and click on the User model to add a new user record.

Fill out the fields (remembering to encrypt your password with [BCrypt](https://bcrypt-generator.com/)) and click Save 1 Record to create your first user.

### Enjoy

Open a browser to http://localhost:3000 and login with your just created, first user.
