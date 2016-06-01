# Basic Flask/Angular template

This is the world's least-featured MVC application, supporting exactly one REST
endpoint and barely any UI. That said, I think it would make a decent starting
point to build out a web app.

Other things it lacks:

- Dependency management: There's zero tooling set up on the frontend; Bootstrap
  and Angular are statically-linked (copied directly into the source tree). The
  backend is slightly better, but it depends on four libraries which you're
  expected to have installed yourself. Mostly because I don't know how
  virtualenv works.
- User management or authentication

# Setup

```
virtualenv env
env/bin/pip install flask glob2 yaml pg8000
```

Then, create a file called `env.yml`:

```
POSTGRES_CONNECTION_TYPE: 'socket'
POSTGRES_DATABASE: 'database_name_here'
POSTGRES_USER: 'username_here'
```

# Running

```
env/bin/python server.py
```

Then, open a web browser to http://localhost:5000


