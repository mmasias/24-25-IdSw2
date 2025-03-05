# Reto 001 - Legibilidad
Teniendo en cuenta los códigos generados en asignaturas de programación anteriores además de proyectos personales se deben identificar los errores que se cometían y exponerlos para saber cómo han evolucionado tus habilidades. El objetivo es analizar los errores más comunes, como malas prácticas, falta de optimización, problemas de seguridad o dificultades en la mantenibilidad del código.

| **Asignatura** | **Código** |
| --- | --- |
| *Programación I* | [RetoCCF](https://github.com/oscarsantasanchez/prg1-22-23/blob/main/retos/entregas/oscarSantamaria/CCCF.java) |
| *Programación I* | [RetoAscii](https://github.com/oscarsantasanchez/prg1-22-23/blob/main/retos/entregas/oscarSantamaria/MicroRetoAscii.java) |
| *Programación I* | [SumaNum](https://github.com/oscarsantasanchez/prg1-22-23/blob/main/retos/entregas/oscarSantamaria/SumaNum.java) |
| *Programación I* | [UnDibujo](https://github.com/oscarsantasanchez/prg1-22-23/blob/main/retos/entregas/oscarSantamaria/UnDibujo.java)|
| *Programación I* | [WhacAMole](https://github.com/oscarsantasanchez/23-24-prg1/blob/main/src/ejercicios/Whacamole/GuacamoleMexicano.java) |
| *EDA I* | [Lista](https://github.com/oscarsantasanchez/23-24-eda1/blob/Reto-007/entregas/santamariaOscar/reto004/List.java) |

## Nombrado

| *Principio* | *Código* | *Error* |
|-|-|-|
| **Elige nombres descriptivos** | [Codigo](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/CCCF.java#L1) | El nombre de la clase no es igual que el del archivo |
| **Nombres Descriptivos** | [Código](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/SumaNum.java#L1) | El nombre de la clase no es igual que el archivo, además son nombres poco descriptivos |


## Comentarios

| *ID* | *Comentario* |
| --- | --- |
| 1 | [Comentario Malo I](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/evaContinua/RetoDiecinueve.java#L3) |
| 2 |[Comentario Malo II](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/evaContinua/RetoDiecisiete.java#L68) |

## Consistencia
| *Código* | *Error* |
| --- | --- |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L13) | Actualmente se ejecuta 16 veces en lugar de 15 |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L13) | Al inicio del bucle no hace poner `turnos=0` ya que [aqui](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L9) ya esta inicializado a cero y no seria necesario volverlo a poner|

## Código Muerto
| *Código* | *Error* |
| --- | --- |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L31) | Esta variable se encuentra varias veces dentro de [este bucle](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L35) pero solo se usa la última vez y se podria optimizar|
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L7) | Este Scanner nunca se llega a cerrar y aunque aqui no genere problemas en práctimas de mayor envergadura podrían generarlos |

## DRY: Don't Repeat Yourself

| *Código* | *Error* |
| --- | --- |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L37) | Se repite en cada iteración, podría simplificarse |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L40) | Tiene condiciones similares, se podría reorganizar de mejor forma|

## YAGNI: You Aren't Gonna Need It
| *Código* | *Error* |
| --- | --- |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L25) | Se pasan como argumentos pero no se usan dentro de la función, se podrían eliminar si no son necesarios |
| [Código](https://github.com/oscarsantasanchez/23-24-prg1/blob/d247b2b4a8f358682fbc614672997ae93bfe8ab6/src/ejercicios/Whacamole/GuacamoleMexicano.java#L31) | Se define antes del bucle pero se reasigna en cada iteración lo cual es innecesario|

## Formato
| *Principio* | *Código* | *Error* |
|-|-|
| Alineado | [Codigo](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/MicroRetoAscii.java#L12) | Las sangrías no estan correctamente alineado |
| Alineado | [Codigo](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/SumaNum.java#L4) | Las sangrías no estan correctamente alineado |
| Alineado | [Codigo](https://github.com/oscarsantasanchez/prg1-22-23/blob/4196931d185cf2e8dd7905c184f07f0ae189244e/retos/entregas/oscarSantamaria/UnDibujo.java#L12) | No se encuentra en concordancia con las demás líneas |

