# DbLocal
Está db foi criada com o intuito de melhoração e criatividade para os devs. Você que não sabe usar muito: firebase, mongo ou outra database complicada, venha usar nossa db :)

## O que ela possui?
Nossa db possui algumas funções básicas, como: get, set push entre outros... Caso você não entenda as funções, você pode entrar no grupo do discord e pedir ajuda para nós!

Funções | Paramêtro  
------ | --------
get | (Path)
set | (Path, valor)
push | (Path, valor)
all | () 
remove | (Path, value)
add | (Path, value)
delete | (Path)

## Como usar
```js
  const { Db } = require("more-functions")
  const db = new Db()
  
  db.set("users/count", 10) //Setará users/count como 10
  
  db.get("users/count") // Puxará o users/counts que retornará 10 
  
  db.add("users/count", 1) //Adicionará 1 em users/count (ficando 11)
  
  db.remove("users/count", 3) //Removerá 3 em users/count (ficando 8)
  
  db.push("users/array" "witz") //Irá criar uma array em users/array e Acrescentará witz dentro
  
  db.delete("users/count") //Irá deletar o objeto users/count
  
  db.all() //Puxará tudo dentro de localdb.json
```
