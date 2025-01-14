# Reto UniversityHack 2024
En una empresa industrial de biotecnología donde se producen antígenos para el desarrollo de vacunas, es de vital importancia optimizar el proceso de producción. Se describe a continuación dicho proceso de producción de una forma generalizada y a alto nivel.

Una vacuna consta de un antígeno (que es el componente activo) y otros componentes (estabilizadores, adyuvantes, excipientes, etc). En este caso nos centramos sólo en la producción del antígeno para un proceso microbiano. Para producirlo, se parte de una pequeña cantidad de un microrganismo, que se multiplica utilizando medios de cultivo y luego se procesa para conseguir el antígeno deseado.

Fases del proceso productivo del antígeno:

1. **Preinóculo**: etapa inicial de crecimiento de los microorganismos en un pequeño volumen de medio de cultivo antes de ser transferidos a un volumen mayor. Es un proceso manual y se realiza normalmente en recipientes de pequeño volumen, como frascos de cristal, dónde no se dispone de mediciones en tiempo real.

2. **Inóculo**: el inóculo implica la mezcla de una cantidad determinada del preinóculo con medio de cultivo estéril para lograr la multiplicación de los microorganismos hasta un volumen suficiente para iniciar una producción a escala industrial. Es la última etapa antes de realizar el cultivo de producción y se realiza en biorreactores, tanques agitados de geometría determinada dónde existe, como mínimo, un control básico de algunas variables de proceso (p.ej. temperatura, pH, …).

3. **Cultivo productivo**: es el proceso en el que el inóculo se mezcla de nuevo con medio de cultivo estéril para lograr la amplificación final del microorganismo hasta la cantidad industrial requerida y, a su vez, lograr la producción del producto de interés, normalmente una biomolécula. Este proceso se realiza en biorreactores con un nivel de control e instrumentación habitualmente superior al disponible en la etapa de inóculo. Las variables de proceso más habituales son la temperatura, pH, oxígeno disuelto y agitación; todas ellas se controlan a sus valores óptimos para lograr la mayor productividad.

4. **Centrifugación**: una vez que se ha alcanzado la concentración deseada de antígeno en el cultivo, se lleva a cabo la centrifugación. Este proceso consiste en aplicar fuerza centrífuga para separar los componentes del cultivo en dos fases, una sólida y una líquida. La centrifugación constituye la primera fase de separación del producto de interés del resto de contaminantes, como por ejemplo el medio de cultivo gastado, y constituye habitualmente el primer paso en el tren de purificación.

5. **Purificación adicional**: después de la centrifugación, se pueden realizar procesos de separación adicionales para eliminar cualquier contaminante y obtener un antígeno altamente puro y seguro para su uso en la vacuna.

Cada tipo de antígeno seguirá un proceso distinto y adecuado a su naturaleza. En general, hay una gran diversidad de procesos productivos según el tipo de antígeno que se desea obtener (bacterias, virus, proteína recombinante, mRNA, VLP, …) por lo que es imposible describir resumidamente todos ellos. Esta diversidad afecta tanto a la expansión del vector biológico (bacteria, células de mamífero, …), lo que se conoce como “upstream”, como a las etapas del proceso de purificación o “downstream”. Una vez se obtiene el antígeno purificado, se puede utilizar para formular la vacuna una vez controlada su calidad según unos parámetros preestablecidos.

Esquema ejemplo del escalado de volúmenes en un proceso productivo como el descrito anteriormente:

![fases](https://github.com/user-attachments/assets/bbdc04a8-adce-47c1-90e8-bc4da9548bfa)

Lotes encadenados: si el título del cultivo es suficiente, una parte del cultivo no se centrifuga, se deja en el mismo biorreactor, y se vuelve a introducir medio de cultivo para iniciar un nuevo cultivo. Este segundo cultivo es una nueva OF, donde los datos de las fases anteriores coincidirán con la OF inicial. Se puede repetir el proceso, mantener una parte del cultivo para una tercera OF. No puede haber una cuarta OF.

![02](https://github.com/user-attachments/assets/7946a611-846d-403f-806f-693ad5f25fd6)

## Objetivo

Debido al impacto en la sociedad de optimizar y mejorar el proceso, ya que fruto del mismo se desarrollarán mejores vacunas, se hace necesario disponer de una previsión de la concentración del producto en el antígeno final después de todas las fases.

Dado lo anterior y partiendo de amplios datasets de ensayos históricos, te retamos a crear el mejor modelo de predicción de producción que pueda estimar el valor de concentración en el antígeno final tras la conclusión de todas las fases descritas el apartado anterior, y de esta forma Identificar los parámetros de proceso que tienen más impacto sobre el título del producto fabricado para mejoras futuras en el proceso.
