¡Espectacular...! Espectacular… espectacular… ¡Espectaculaaar-a-a-a-a!

Ya no importa cómo lo escribamos, porque a todos ellos los vamos a identificar de la misma forma usando solo la PK (el ID numérico) de la que tanto hablamos (o quizás no tanto, pero ahora nos va a importar un poquito más :stuck\_out\_tongue\_winking\_eye:).


<div
  class='mu-erd'
  data-entities='{
    "canciones": {
      "id_cancion": {
        "type": "Integer",
        "pk": true
      },
      "titulo_cancion": {
        "type": "Text"
      },
      "id_artista": {
        "type": "Integer",
        "pk": false,
        "fk": {
          "to": { "entity": "artistas", "column": "id_artista" },
          "type": "many_to_one"
        }
      },
      "album":{
        "type": "Text"
      },
      "anio":{
        "type": "Integer"
      }
    },
    "artistas": {
      "id_artista": {
        "type": "Integer",
        "pk": true
      },
      "nombre_artista": {
        "type": "Text"
      },
      "integrantes": {
        "type": "Text"
      },
      "genero": {
        "type": "Text"
      },
      "nacionalidad": {
        "type": "Text"
      }
    }
  }'>
</div>

Fíjate que la **PK** de una tabla (:key: id\_artista en “artistas”) no es la clave primaria de la otra (:key: id\_canción en “canciones”). 

Pero, como es un campo que asignamos a la canción para referenciar determinado registro de la tabla artista, se lo llama clave foránea, foreign key en inglés, o directamente **FK** (y lo representamos en el DER con la llave plateada).