# Alura MongoDB
------------------------------

##### Executando o arquivo MongoDB e arquivo Mongo

```
$ cd /home/milenevlacerda/Projects/Alura/MongoDB/db/mongo/bin
$ ./mongod --dbpath <caminhoDoDiretorioDb>

```



###### Modificando a variável de ambiente no .bash_profile
-------------------------------
```
export PATH=$PATH:<caminhoDoDiretorioDbBin>
```



###### Acessando o cliente mongo
-------------------------------
```
$ mongo
```



###### Criando coleções
-------------------------------
```
db.createCollection( "alunos" );
```



###### Inserindo dados
-------------------------------
```
db.alunos.insert(
    {
        nome: "Milene",
        data_nascimento: new Date( 1996, 10, 14 ),
        curso: {
            nome: "Sistemas para Internet"
        },
        notas: [ 10.0, 9.0, 4.5 ],
        habilidades: [
            {
                nome: "Inglês",
                nível: "Intermediário"
            },
            {
                nome: "Front end",
                nível: "Avançado"
            }
        ]
    }
);
```



###### Encontrando dados
-------------------------------
```
db.alunos.find();
```



###### Removendo determinado dado
-------------------------------

```
db.alunos.remove({
    "_id": ObjectId("586f0ddd10489caadd1fa54e")
});
```
