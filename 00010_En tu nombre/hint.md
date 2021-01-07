Recuerda que nos interesan solo los títulos, pero tenemos como dato el nombre del actor.

Te dejamos como ayudita la consulta del ejercicio anterior: :wink: 

> ``` sql 
> SELECT DISTINCT titulo 
> FROM series_peliculas s, personaje_por_contenido pc, personajes p 
> WHERE s.id_serie = pc.id_serie 
> AND pc.id_personaje = p.id_personaje 
> AND p.actriz_actor LIKE "%Jennifer%Lawrence%"; 
> ```

