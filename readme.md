# PokeAPI

Simple demo API with typescript - NodeJs - Mongo

The API is dockerized. To run you must have docker installed on your system.

## Use

Setup:

```
npm i
npm run build
docker-compose up
```

## Request examples

Available endpoints:

### Create pokemon

POST /pokemon

```
curl --request POST \
  --url http://localhost:9001/pokemon \
  --header 'content-type: application/json' \
  --data '{
	"name" : "some name",
	"type": "Water",
    "gender": "Female",
    "height": 0.8,
    "weight": 10.5
}'
```

### Get all pokemon

GET /pokemons

```
curl --request GET \
  --url http://localhost:9001/pokemons
```

### Update pokemon

PUT /pokemon/{pokemon_id}

```
curl --request PUT \
  --url http://localhost:9001/pokemon/5d29c97d72576e4dadfab2fa \
  --header 'content-type: application/json' \
  --data '{
	"name": "updated name"
}'
```

### Delete pokemon

DELETE /pokemon/{pokemon_id}

```
curl --request DELETE \
  --url http://localhost:9001/pokemon/5d29c98e44aa8b4dc15d2f19
```
