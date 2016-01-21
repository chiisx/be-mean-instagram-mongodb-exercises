#MongoDB - Aula 01 _ Exercício
	autor:Thiago Sousa Santos


##  Importando os Restaurantes

mongoimport --db be-mean --collection restaurantes --host=127.0.0.1 --drop --file restaurantes.json
connected to: 127.0.0.1
Thu Jan 21 02:49:18.898 dropping: be-mean.restaurantes
Thu Jan 21 02:49:19.639 check 9 25359
Thu Jan 21 02:49:19.777 imported 25359 objects


##Contando os Restaurantes

 db.restaurantes.find({}).count()
   25359
