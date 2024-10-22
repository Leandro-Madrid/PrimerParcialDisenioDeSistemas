# Parcial
¡Atención terrícolas! La invasión es inminente. Las Naves Nodrizas se acercan a la tierra. De una Nave Nodriza sabemos su capacidad máxima de albergar naves, ya sea otras Naves Nodrizas, Naves de Ataque, Naves Embajadoras o Naves Mixtas y el daño ofensivo que esta provoca, un número entero que debe ser mayor a 0. Además poseen un Nivel de combustible espacial distinto para toda nave, un nivel de Escudo (que comienza en 100) y una energía (que comienza en 100), estas 3 últimas características son iguales para todos los tipos de Naves. A una Nave Nodriza nos interesa que pueda agregar naves ya fabricadas a su flota, sin pasarse de la capacidad máxima y tomando las consideraciones pertinentes en este caso, poder eliminar una nave dada de la flota (siempre que esté en ella, claro), poder calcular cuánto es el daño total de la misma, considerando además el daño de cada una de las naves que la Nave Nodriza alberga, poder atacar a una Nave Enemiga y poder construir naves. Con este fin, toda nave nodriza tiene a su disposición un Constructor de naves, un recurso tan preciado que es único en todo el sistema, que sabe construir los 3 tipos de nave, considerando cada una de sus particularidades y sin obtener incongruencias: De una Nave de Ataque, nos interesa su daño ofensivo, la cantidad de tripulantes (que nunca puede ser 0), la cantidad de Misiles. El daño de una Nave de ataque está dado por el daño ofensivo multiplicado por la cantidad de tripulantes. De una Nave Embajadora sabemos su cantidad de cónsules. No provoca daño. De una Nave Mixta sabemos su cantidad de daño ofensivo, la cantidad de tripulantes, la cantidad de cónsules y la cantidad de misiles. Puede atacar pero como su fuselaje no es tan resistente como el de una Nave de Ataque, cuando ataca (su daño se calcula de la misma forma que la nave de ataque) un 0.1% del daño lo sufre. Toda Nave debe ser capaz de viajar a otro Planeta, de estos sabemos su nombre y la distancia con respecto a la Tierra, expresada en una cantidad de años luz. Cada año luz consume 1.1 lts de combustible espacial. Si esta nave puede hacer el viaje (es decir le da el combustible) lo hace, si no se debe poder notificar.

Desafio 1:  
A) Toda Nave puede tener dos Modos: AtaquePoderoso que duplica el daño del rival (en el caso de la Nave Embajadora que no provoca daño hace que este sea de 1) AtaqueDefensivo (que aumenta el daño en un 10% pero también al escudo de la nave) Estos se reinician cuandos se ataca 10 veces.  
B) Dar el mecanismo para agregar distintos Modos de pelea en las Naves.

Desafio 2:  
A) Cada vez que una Nave Nodriza recibe una Misión, está la propaga para las Naves nodrizas que conforman su flota. Las misiones pueden ser Bélicas, Diplomáticas o TránsitoHostil. Las Misiones Bélicas son atendidas por Naves de Ataque (atacando al objetivo que la misión le asigna)

Las Misiones Diplomáticas son atendidas por Naves Embajadoras. (Yendo al Planeta que la Misión le proponga) Las Naves Mixtas pueden atender ambos tipos de Misiones (atacando el objetivo pero también yendo al destino que la Misión propone)

Se pide:
- Modelar el hito 1 completo, recordando buenas prácticas (indentación correcta, nombre descriptivos, y principios visto en la Programación Orientada a Objetos (herencia, polimorfismo, generalización, encapsulamiento, etc) tanto como principios vistos en la materia (Tell, Don’t ask, Solid, evitar code smells, etc)
- Elegir uno de los desafíos y moldelarlo.
- Explicar en cada patrón utilizado nombre, tipo y agentes que participan (que clase/s cumple cada rol)
- El ID del proyecto debe ser ar.edu.davinci.parcial
- Tanto el entregable como el proyecto debe responder al formato: Parcial1 - Valenzuela, Horacio E.

## Strategy

Descripción: La interfaz Modo y sus implementaciones (AtaquePoderoso, AtaqueDefensivo) permiten que las naves cambien su comportamiento de ataque. Las naves pueden activar diferentes modos sin modificar su código interno.

## Composición:

La clase NaveNodriza tiene una lista de Nave, lo que permite que las naves contengan otras naves. Esto es un uso de la composición y permite la creación de estructuras jerárquicas de naves.  