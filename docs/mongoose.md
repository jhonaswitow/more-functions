# Simple-mongoose
Criamos essa classe dentro da nossa npm para simplificar vidas de devs que quer usar uma web db, como a mongoose

# Functions

Função | Parâmetro | Info
----- | ----- | -----
<db>.get | String | Puxa um valor dentro da database
<db>.set | (Array ou String), value | Seta um valor dentro da database
<db>.add | (Array ou String), number | Adiciona um valor na database
<db>.remove | (Array ou String), number | Remove um valor na database
<db>.all | () | Puxa tudo dentro da db
  
# Básico
```js
const { mongoose } = require("more-functions")
const db = new mongoose({
  mongoUrl: 'url',
  schema: {
    schema1: {
    type: String,
    required: true
  },
    schema2: {
    type: Number,
    default: 0
  }
 })
  
function connect() {
  db.login()
}
  
connect()
  ```
  
# Como usar
  ```js
await db.get('schema1').schema2 || 0 
  
await db.set('schema1', '3184147318342137') //Ou: db.set([ 'schema1', 'schema2'], 900)
  
await db.add([
  'schema1',
  'schema2'
    ], 12)
  
await db.remove([
  'schema1',
  'schema2'
    ], 12)
  
await db.all()
 ```
