# Authentication Endpoints

Simply create a backend server with magic-link authentication.
A user would simply enter an email, and we would email them a link using which they can log in.

**Duration: 1-2 days**

## Techniques you should use

1. Use Poetry, and FastAPI backend framework.

2. PostgreSQL Database and always use async methods wherever possible such as create_async_engine, async_sessionmaker. You can install postgresql locally or use docker container.

3. SQLModel for ORM(not SQLAlchemy).

4. Alembic for Database Migration.

5. SendGrid for mail api. You can sign up to SendGrid and use your free api key for development.

## Endpoints We need

1. ```GET /auth/send-magic-link```

    The user enters emails and requests an email with a link.
    You should save user into database when user request this endpoints.

2. ```GET /auth/verify-magic-link?xyz```
    
    If it is correct, it will generate jwt token that you can use in bearer token.

    Otherwise, return ```404``` error.

3. ```GET /user```

    Return logged in user information.

    JWT token will be added as bearer token here.

## Unit Test

You should write a test for all services, endpoints, utilities, etc.

Test Coverage should be at least 90%.
