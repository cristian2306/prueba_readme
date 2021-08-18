# CVDS
Ciclos de Vida y Desarrollo de Software\
**Laboratorio 01**

# Información General
## Datos Personales

* **Nombre**: Diego Alejandro González Gualteros
* **Edad**: 21 años
* **Correo**: *diego.gonzalez-g@mail.escuelaing.edu.co*
* **Semestre Actual**: Séptimo

# Acerca de la carrera
## Plan de estudios
![Image](https://github.com/DiegoGonzalez2807/prueba_readme/blob/main/Resources/Plan_estudios.png) 

## Lenguajes de Programación más interesantes
Los lenguajes que más me gustan son:
1. *Java*
2. *SQL*
3. *Python*

>Esto se debe a que Java está ligado sobre todo a un tema que me parece muy interesante el cuál es la *Programación Orientada a Objetos*

> SQL me parece interesante debido a lo intuitivo que puede llegar a ser el código, y como una buena base de datos puede influir en la organización de una empresa

> Python me parece interesante debido a su capacidad con la inteligencia artificial, así como el manejo de grandes bases de datos con el fin de analizarlos

## Ejemplos en código
### Java
```
/**
     * Hace crecer la serpiente en las unidades especificadas, entiendase hacerla crecer en cuanto a longitud
     * @param unidades - Cantidad en la que crece la serpiente
     */
    public final void crecer(int unidades) {
        for(int i=0;i<unidades;i++){
            Circle miembro = new Circle(colores[1]);
            miembro.setTablero(tablero);
            if(cuerpo.isEmpty() ){
                int[] local = validarSentido(sentido, posicion.getPosicion());
                tablero.setObjeto(miembro, local[0], local[1]);
                miembro.setPosicion(new Posicion(local));
                miembro.setSentido(sentido);
            }
            else{
                Circle cola = cuerpo.get(longitud-2);
                int[] local = validarSentido(sentido,cola.getPosicion().getPosicion());
                tablero.setObjeto(miembro,local[0],local[1]);
                miembro.setSentido(sentido);
                miembro.setPosicion(new Posicion(local[0],local[1]));
            }
            cuerpo.push(miembro);
            longitud+=1;
        }
    }   
```
### SQL
```
/*El numero maximo de piezas que se pueden solicitar es 50*/
CREATE OR REPLACE TRIGGER Maximos_tubos
BEFORE INSERT ON pedido_pieza
FOR EACH ROW
BEGIN
	IF :NEW.cantidad_piezas > 50 THEN
		RAISE_APPLICATION_ERROR(-20001,'El Numero maximo de piezas que se pueden solicitar es 50');
	END IF;
END;
```

### Python
```
from sys import stdin
def MCD(first_element,last_element):
    if last_element == 0:
        return first_element
    else:
        return MCD(last_element,first_element%last_element)

def main():
    numbers = stdin.readline().strip().split()
    a, b = int(numbers[0]), int(numbers[1])
    print(MCD(a,b))
```



