FROM elixir:1.6

# install hex package manager
RUN mix local.hex --force
RUN mix local.rebar --force

# install the latest phoenix 
RUN mix archive.install https://github.com/phoenixframework/archives/raw/master/phx_new.ez --force

# create app folder
RUN mkdir /app
COPY ./my_app /app
WORKDIR /app

# install dependencies
RUN mix deps.get
