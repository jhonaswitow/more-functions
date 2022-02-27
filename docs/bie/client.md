# Básico:
```js
const { bie } = require("more-functions")
const client = new bie.Client({
  default: true //Ative isso para poder usar o '&send[]' e os outros...
}) //normal: default: true 
```


### Funções 

Funções | Exemplo
--------| -------
createAppGet() | `<client>.createAppGet({ router: '/', code: '&send[Iu]' })`
setEjsInBie() | `<client>.setEjsInBie()`
createAppListen() | `<client>.createAppListen(8000)`

### Funções dentro do code
```js
//Necessita do default: true
const client = new <bie>.Client({
  default: true 
  })
  ````

Código | Exemplo
-------| ---------
&render[] | `'&render[index]'`
&send[] | `'&send[Este é meu site]'`
&json[] | `'&json[{ name: 'witz' }]'`
&end | `'&end'`
&redirect | `'&redirect[https://google.com]'`

#Exemplos

## Usando sem o default: true

```js
const { bie } = require("more-functions")
const client = new bie.Client({
 default: false
})

client.createAppGet({
  router: '/',
  code: (req, res) => {
  res.send("Olá senhor")
  }
})

function listen() {
client.createAppListen(8000)
console.log("Ligado!")
}

listen()
```

## Usando com o default: true

```js
const { bie } = require("more-functions")
const client = new bie.Client({
 default: true
})

client.createAppGet({
  router: '/',
  code: `&send[Olá senhor]`
})

function listen() {
client.createAppListen(8000)
console.log("Ligado!")
}

listen()
```
