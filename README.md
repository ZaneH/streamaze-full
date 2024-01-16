# Streamaze Full

### 1. Install Requirements

- Elixir
- Docker

### 2. Clone Repository

```bash
$ git clone --recurse-submodules https://github.com/ZaneH/streamaze-full.git
$ cd streamaze-full
```

### 3. Setup Database

```bash
$ docker compose up streamaze-db

# In a new terminal (so that the database is still running)
# run the following commands
$ cd streamaze-full/streamaze-api
$ source .env
$ mix deps.get
$ mix ecto.create
$ mix ecto.migrate
# After this, you should shutdown the database for now by
# pressing Ctrl+C in the terminal running streamaze-db
```

### 4. Run Streamaze

```bash
$ cd ..
$ docker compose up
```

### 5. Open Streamaze + Register

- Open http://localhost:4000/account/register
- Sign up
- Get your Streamaze Key from http://localhost:4000/account/settings
- Open http://localhost:3000/settings and enter your Streamaze Key
- Configure your stream settings on the settings page
- Open the dashboard at http://localhost:3000/dashboard