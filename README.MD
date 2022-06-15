## Hosted Project

[Jobs API Heroku URL](https://jobs-api-bulega.herokuapp.com/api-docs/)
#### Setup

```bash
npm install && npm start
```

##### Database Connection and JWT-values
- Setup .env in the root
- Add MONGO_URI,JWT_SECRET and JWT_LIFETIME to the .env with correct values

#### Routers

- auth.js
- jobs.js



#### Register User

- Validate - name, email, password - with Mongoose
- Hash Password (with bcryptjs)
- Save User
- Generate Token
- Send Response with Token

#### Login User

- Validate - email, password - in controller
- If email or password is missing, throw BadRequestError
- Find User
- Compare Passwords
- If no user or password does not match, throw UnauthenticatedError
- If correct, generate Token
- Send Response with Token



#### Security

- helmet
- cors
- xss-clean
- express-rate-limit

Swagger UI

```yaml
/jobs/{id}:
  parameters:
    - in: path
      name: id
      schema:
        type: string
      required: true
      description: the job id
```
