# Docker

Note: This image has no postgresql database configured! It should be easy to add a postgresql container with docker compose for example.

To use this docker image with an existing phoenix installation
  * Run `docker run --rm -v "$PWD":/usr/src/myapp -p 4000:4000 splagemann/elixir-phoenix` in your source directory

To use this docker image with a new phoenix installation
  * Go to your source directory
  * Run `docker run -ti --rm -v "$PWD":/usr/src/myapp splagemann/elixir-phoenix mix phx.new your_app --no-ecto`
  * Run `docker run --rm -v "$PWD/your_app":/usr/src/myapp -p 4000:4000 splagemann/elixir-phoenix`
