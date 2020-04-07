![Zeew Api](https://i.imgur.com/MP2bABn.png "Lo Mejor de Zeew y del C&P")

# Zeew Eco!

  - Economía Fácil y sencilla
  - Tienda Fácil sin limite


Crea Una economía fácil y sencilla de usar para tu bot.

> Muchos se complican demasiado hacer algo como esto,
> ¿Por qué no ayudarles un poco?.

## Informacion

* **Constructores**
  * [Economía](#economia)
  * [Tienda](#tienda)
  * [Dinero](#dinero)
  * [Inventario](#Inventario)
* **Zeew**
  * [Staff](#staff)
  * [Proyectos](#proyectos)

 
No olvides que si tienes un error o propuestas para mejorar este NPM
Solo tienes que unirte a este servidor de 
[Zeew Discord](https://discord.gg/3K8pdmf).
[KamerrEzz Discord](https://discord.gg/PBDbHGq).

Gracias por Escoger este NPM

>

## instalación

```js
npm i zeew-eco
```
<a name="economia" />

### Economia

```js
const zeco = require('zeew-eco')
const eco = new zeco.economia()
```

| Métodos | Descripción |
| ------ | ------ |
| [mostrar](#Eco-mostrar) | Muestra el dinero del usuario
| [agregar](#Eco-agregar) | Agrega dinero aun usuario|
| [quitar](#Eco-quitar) | Elimina el dinero de un usuario|
| [eliminar](#Eco-eliminar) | Elimina la economia del servidor|
| [comprar](#Eco-comprar) | Comprar En la tienda|

<a name="Eco-mostrar" />

#### Economia: Mostrar

```js
eco.mostrar(clave, id)
```
* clave - ID del servidor
* id - ID del usuario
```js
const eco = new zeco.economia()
eco.mostrar(servidor.id, miembro.id)
```
```js
```
<a name="Eco-agregar" />

#### Economia: Agregar

```js
eco.agregar(clave, id, cantidad)
```
* clave - ID del servidor
* id - ID del usuario
* cantidad - Dinero que quieras agregarle

```js
const eco = new zeco.economia()
eco.agregar(servidor.id, miembro.id, 1500)
```
```js
```
<a name="Eco-quitar" />

#### Economia: Quitar

```js
eco.quitar(clave, id, cantidad)
```
* clave -ID del servidor
* id - ID del usuario
* cantidad - Dinero que quieras quitarle
```js
const eco = new zeco.economia()
eco.quitar(servidor.id, miembro.id, 1500)
```

```js
```

<a name="Eco-eliminar" />

#### Economia: Eliminar

```js
eco.eliminar(clave)
```

* clave -ID del servidor

```js
const eco = new zeco.economia()
eco.eliminar(servidor.id)
```

```js
```

<a name="Eco-comprar" />

#### Economia: Comprar

```js
eco.comprar(clave, id, item)
```
* clave - ID del servidor
* id - ID del usuario
* item - numero de item
```js
const eco = new zeco.economia()
eco.comprar(servidor.id, miembro.id, 1)
```
```js
```
<a name="tienda" />

### Tienda

```js
const zeco = require('zeew-eco')
const td = new zeco.tienda()
```

| Metodos | Descripcion |
| ------ | ------ |
| [Mostrar](#TD-mostrar) | Muestra Items a la tienda|
| [Agregar](#TD-agregar) | Agrega Items a la tienda|
| [Eliminar](#TD-eliminar) | Elimina la tienda del servidor|
| [quitar](#TD-quitar) | Elimina Items de la tienda|

<a name="TD-mostrar" />

#### Tienda: Mostrar

```js
eco.mostrar(clave)
```
* clave - ID del servidor
```js
const td = new zeco.tienda()
eco.mostrar(servidor.id)
```
```js
```
<a name="TD-agregar" />

#### Tienda: Agregar

```js
eco.agregar(clave, nombre, desc, precio)
```
* clave - ID del servidor
* nombre - Nombre del Item
* desc - La descripcion del item
* precio - el precio del item
```js
const td = new zeco.tienda()
td.agregar(servidor.id, "Canal Propio", "un canal privado para ti", 20000)
```
```js
```
<a name="TD-eliminar" />

#### Tienda: eliminar

```js
td.eliminar(clave, item)
```
* clave -ID del servidor
* item - Numero del Item de la tienda
```js
const td = new zeco.tienda()
td.eliminar(servidor.id, 1)
```

```js
```

<a name="TD-quitar" />

#### Tienda: quitar

```js
td.quitar(clave, item)
```
* clave -ID del servidor
* item - Numero del Item de la tienda
```js
const td = new zeco.tienda()
td.quitar(servidor.id, 1)
```

```js
```

<a name="dinero" />

### Dinero

> esta funcion puede ser removida o cambiada en un futuro. Lo que diga la comunidad.
```js
const zeco = require('zeew-eco')
const td = new zeco.dinero()
```
| Metodos | Descripcion |
| ------ | ------ |
| [Robar](#D-robar) | Roba dinero a otro usuario|


<a name="D-robar" />

#### Dinero: robar

```js
td.robar(clave, id1, d2, cantidad)
```
* clave -ID del servidor
* id1 - ID del usuario (robar)
* id2 - ID del usuario (robado)
* cantidad - Cantidad de dinero que le robara al usuario

```js
td.robar(servidor.id, yo.id, usuario.id, 1500)
```

<a name="Inventario" />

### Inventario
```js
const zeco = require('zeew-eco')
const inv = new zeco.inventario()
```
| Metodos | Descripcion |
| ------ | ------ |
| [compras](#V-compras) | Guardar Compras en el inventario|
| [quitarcompras](#V-quitarcompras) | Quitar Alguna compra en el inventario |
| [vercompras](#V-vercompras) | Ver los objetos comprados desde la tienda

<a name="V-compras" />

#### Inventario: compras

```js
inv.compras(clave, id, item, boleano)
```
* clave - ID del servidor
* ID - ID del usuario
* Item - ID del item de la tienda que sera guardado en el inventario
* boleano
    * true - No guardar el mismo Item
    * false - Guardar el mismo Item
> proximas Actualizaciones se quiere hacer que los usuarios puedan vender los items de sus inventarios y tener una economia mas amplia.
```js
const inv = new zeco.inventario()
inv.quitarcompras(servidor.id, usuario.id, 2 , false)
```
```js
```

<a name="V-quitarcompras" />

#### Inventario: quitarcompras

```js
inv.quitarcompras(clave, id, item)
```
* clave - ID del servidor
* ID - ID del usuario
* Item - ID del item de la tienda que sera eliminado en el inventario
```js
const inv = new zeco.inventario()
inv.quitarcompras(servidor.id, usuario.id, 2)
```
```js
```

<a name="V-vercompras" />

#### Inventario: vercompras

```js
inv.vercompras(clave, id)
```
* clave - ID del servidor
* ID - ID del usuario
```js
let inv = new ze.inventario()
inv.vercompras(servidor.id,usuario.id)
```
```js
```

---
## Zeew

<a name="staff" />

#### Staff
 * @KamerrOficial
  ```
    * ROL: Owner
    * ID Discord: 403695999941345280
    * Redes Sociales: @KamerrEzz
    * Portafolio: behance.net/KamerrEzz
  ```
 * @ValerynR  
```
  * ROL: Co-Owner
  * ID Discord: 393603334847856650
```
<a name="proyectos" />

#### Proyectos

| proyecto | descripcion |
| --- | --- |
| [Zeew](https://www.npmjs.com/package/zeew) | Descubre nuestra API Reset de Imágenes y manipulación
#### Donaciones
* [Kamerr Ko-fi](https://ko-fi.com/kamerroficial)
Las Donaciones las uso crear más proyectos y mejorar la calidad,
cierta cantidad está totalmente para **zeew** para su único uso.
