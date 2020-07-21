# rubymine-rest-client

A series of configuration files for running REST calls through RubyMine (and other JetBrains products).

## Getting Started

1. Clone the repo.
2. Create a new project in RubyMine from the source directory.
3. Create a new file in the top-level directory called ``http-client.private.env.json``. You'll need to
put API secrets in here that match the environments in ``http-client.env.json``, so for example:
```
{
  "subway-uat": {
    "tenant-id": (redacted),
    "client-id": (redacted),
    "client-secret": (redacted)
  }
}
```
You can then open any of the ``*.http`` files and run the individual calls using the correct environment.
RubyMine will grab the 'public' envs like ``base-uri`` as well as the 'private' ones like `client-secret`
and insert them into the API calls where scripted.

## Contributing

*Do not under any circumstances* add a `.private.env.json` file to this repo. It's in the `.gitignore`
for a reason.
