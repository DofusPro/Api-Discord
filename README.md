#FireFiles


Tenemos un discord para dudas y actualizaciones : https://discord.gg/6DJxrSZ

FireFiles se dedica a hacer endepoits para los desarolladores de bots de discord

https://firefiles.herokuapp.com/hug

https://firefiles.herokuapp.com/smoke

Y como usarlo aqui un simple ejemplo:

En hadler:

```js
const Discord = require("discord.js"); //Modulo de discord.js
const superagent = require("superagent"); // Modulo para hacer funcionar las imagenes

module.exports.run = async (bot, message, args, prefix) => {

    let { body } = await superagent.get("https://firefiles.herokuapp.com/smoke") // Con el modulo superagent hacemos que mande la imagen
    let link = body.url
    const embed = new Discord.RichEmbed()
      .setAuthor(message.author.username, message.author.avatarURL)
      .setColor("RANDOM")
      .setImage(link)
      .setFooter("Powered by: FireFiles")
     .setTimestamp()
    message.channel.send(embed)


 
}
module.exports.help = {
  name: "smoke"
}
```


En simple :

```js
 const superagent = require("superagent"); // Modulo para hacer funcionar las imagenes
 let { body } = await superagent.get("https://firefiles.herokuapp.com/smoke")// Con el modulo superagent hacemos que mande la imagen
    let link = body.url
    const embed = new Discord.RichEmbed()
      .setAuthor(message.author.username, message.author.avatarURL)
      .setColor("RANDOM")
      .setImage(link)
      .setFooter("Powered by: FireFiles")
     .setTimestamp()
    message.channel.send(embed)
```















