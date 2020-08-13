## Usage

docker run --rm -it -v "$PWD":/home/lua/projects lua:tag

### Persisting Rocks

- Create a sepearte volume for lua-rocks
- Bind the volume on docker container start
- docker run -it -v lua:/usr/local/lib/luarocks lua:v4
