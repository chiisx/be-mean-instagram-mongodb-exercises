
#MongoDB - Aula 02 _ Exercício
autor:Thiago Sousa Santos


1. Crie uma database chamada be-mean-pokemons


mintisx(mongod-2.4.9) be-mean-pokemons> use be-mean-pokemons
switched to db be-mean-pokemons



2. Liste quais databases você possui nesse servidor	

mintisx(mongod-2.4.9) be-mean-pokemons> show dbs
be-mean          ? 0.203GB
be-mean-pokemons ? (empty)
local            ? 0.078GB
pokemon          ? 0.203GB
pokemons         ? 0.203GB
test             ? 0.203GB
teste            ? 0.203GB

3. Liste quais coleções você possui nessa database	

mintisx(mongod-2.4.9) be-mean-pokemons> show collections
pokemons       ? 0.000MB / 0.016MB
system.indexes ? 0.000MB / 0.008MB



4. Insira pelo menos 5 pokemons A SUA ESCOLHA utilizando o mesmo padrão de campos utilizado: name, description, attack, defense e height;

var pokemon = {'name':'metapod','description':'casulo','type': 'verme', attack: 
mintisx(mongod-2.4.9) be-mean-pokemons>
db.pokemon.insert(pokemon)

 var pokemon = {'name':'metapod','description':'casuloa','type': 'verme', attack: 1, height: 0.7 }
db.pokemon.insert(pokemon)



var pokemon = {'name':'weddle','description':'inseto corno ','type': 'inseto', attack: 2, height: 0.3 }
 db.pokemon.insert(pokemon)



var pokemon = {'name':'kakuna','description':'inseto antisocial ','type': 'inseto', attack: 1, height: 0.6 }
 db.pokemon.insert(pokemon)


var pokemon = {'name':'kakuna','description':'inseto antisocial ','type': 'inseto', attack: 1, height: 0.6 }
 db.pokemon.insert(pokemon)


var pokemon = {'name':'bedrill','description':'abelha zika','type': 'abelha venenosa', attack: 4, height: 1.0 }
 db.pokemon.insert(pokemon)



5. Liste os pokemons existentes na sua coleção



mintisx(mongod-2.4.9) be-mean-pokemons> db.pokemon.find()

{
  "_id": ObjectId("56b04ae3a90f84a59e6834b2"),
  "name": "Caterpie",
  "description": "Larva lutadora",
  "type": "inseto",
  "attack": 30,
  "height": 0.3
}

{
  "_id": ObjectId("56b04b2ba90f84a59e6834b3"),
  "name": "Charmander",
  "description": "Esse é o cão chupando manga de fofinho",
  "type": "fogo",
  "attack": 52,
  "height": 0.6
}

{
  "_id": ObjectId("56b04b9ca90f84a59e6834b4"),
  "name": "Charizard",
  "description": "Esse é o cão chupando manga de fofinho",
  "type": "fogo",
  "attack": 52,
  "height": 0.6
}

{
  "_id": ObjectId("56b04ba5a90f84a59e6834b5"),
  "name": "Charmilion",
  "description": "Esse é o cão chupando manga de fofinho",
  "type": "fogo",
  "attack": 52,
  "height": 0.6
}
{
  "_id": ObjectId("56b04bd9a90f84a59e6834b6"),
  "name": "Squirtle",
  "description": "Ejeta água que passarinho não bebe",
  "type": "água",
  "attack": 48,
  "height": 0.5
}

{
  "_id": ObjectId("56b04bffa90f84a59e6834b7"),
  "name": "wartotle",
  "description": "Ejeta água que passarinho não bebe",
  "type": "água",
  "attack": 48,
  "height": 0.5
}
{
  "_id": ObjectId("56b04c12a90f84a59e6834b8"),
  "name": "blastoise",
  "description": "Ejeta água que passarinho não bebe",
  "type": "água",
  "attack": 48,
  "height": 0.5
}

{
  "_id": ObjectId("56b04c39a90f84a59e6834b9"),
  "name": "Bulbassauro",
  "description": "Chicote de trepadeira",
  "type": "grama",
  "attack": 49,
  "height": 0.4
}

{
  "_id": ObjectId("56b04c57a90f84a59e6834ba"),
  "name": "venusaur",
  "description": "Chicote de trepadeira",
  "type": "grama",
  "attack": 49,
  "height": 0.4
}

{
  "_id": ObjectId("56b04c6ca90f84a59e6834bb"),
  "name": "ivysaur",
  "description": "Chicote de trepadeira",
  "type": "grama",
  "attack": 49,
  "height": 0.4
}


6. Busque o pokemons a sua escolha, pelo nome, e armazene-o em uma variável chamada `poke`.

mintisx(mongod-2.4.9) be-mean-pokemons> var query = {name:'venusaur'}
mintisx(mongod-2.4.9) be-mean-pokemons> var poke = db.pokemon.findOne(query)
mintisx(mongod-2.4.9) be-mean-pokemons> poke
{
  "_id": ObjectId("56b04c57a90f84a59e6834ba"),
  "name": "venusaur",
  "description": "Chicote de trepadeira",
  "type": "grama",
  "attack": 49,
  "height": 0.4


mintisx(mongod-2.4.9) be-mean-pokemons> poke
{
  "_id": ObjectId("56b04c57a90f84a59e6834ba"),
  "name": "venusaur",
  "description": "pokemon verde zika da flora floral monstro activia",
  "type": "grama",
  "attack": 49,
  "height": 0.4


7. Modifique sua `description` e salvê-o


mintisx(mongod-2.4.9) be-mean-pokemons> poke.description = 'pokemon verde zika da flora floral monstro activia'
pokemon verde zika da flora floral monstro activia
mintisx(mongod-2.4.9) be-mean-pokemons> db.pokemon.save(poke)
