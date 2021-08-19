# CVDS  
_Ciclos de Vida y Desarrollo_  
_Lab01_
# INFORMACION GENERAL
> - __Nombre__: Cristian Andres
> - __Apellido__: Castellanos Fino
> - __Edad__: 21
## Estudio
> - __Universidad__: [Escuela Colombiana de Ingenieria Julio Garavito](https://www.escuelaing.edu.co/es/)
> - __Correo__: cristian.castellanos@mail.escuelaing.edu.co
> - __Carrera__: Ingenieria de Sistemas
> - __Semestre__: Septimo semestre
## Plan de estudio
![Plan de estudio][1]

[1]:https://github.com/DiegoGonzalez2807/prueba_readme/blob/main/Resources/Plan_estudios.png "Plan de estudio"

### Proyecto realizados
1. SnOOpe
  - La experiencia que tuve al realizar este proyecto fue bastante, puesto que era poco lo que sabia del lenguaje como tal, aprendi bastante el trabajo en pareja, fue arduo el trabajo y exigente sin embargo se logro un exelente proyecto, lastimosamente no terminado.  
  El proyecto consistía en crear un modelos de el juego Snake, pero con nuestra propia personalización. Se busco que el usuario tuviera una experiencia agradable, permitiendole elegir la serpiente, ademas de agregarle habilidades a la serpiente, y lograr un modo multijugador.
  ```
    /**
     * function created to add a box
     * in a given row and column
     * 
     * @param row  --> the number of the row
     * @param column --> the number of the column
     */
    public void store(int row, int column){
        if(row < 1 && column < 1 || row >=1 && column < 1 || row <1 && column >= 1){
            JOptionPane.showMessageDialog(null, "No puedes meter cajas en esta posición", "Cuidado", JOptionPane.WARNING_MESSAGE);
        }
        else{
            int newRow = row - 1;
            int newColumn = column - 1;
            stockValues[newRow][newColumn] += 1;
            //add one to the height variable, and for each stock array, add a new rectangle
            setStockValues(stockValues);
        }
    } 
  ```

2. Calculadora de números complejos
  - LA calculadora de números complejos es un proyecto interesante, bastante de hecho, permite al usuario entrar a el tema de los números complejos y la computacion cuantica, claro esta la base, el proyecto permite al usuario realizar cualquier operacion con los números complejos, ademas explica de forma muy sencilla el tema.
    ```
    def Probabilistic_system(mat,click,state):
      def mul_mat_bool(A,B):
          m_a = len(A)
          n_a = len(A[0])
          m_b= len(B)
          n_b= len(B[0])
          if n_a == m_b:
              ans = [[False for i in range(len(B[0]))] for i in range (len(A))]
              for i in range(len(A)):
                  for j in range(len(B[0])):
                      for k in range(len(A[0])):
                          ans[i][j] =  ans[i][j] or (A[i][k] and B[k][j])
          return ans
      start = mat
      if type(mat[0][0])== bool:
          for i in range(click):
              state_click = mul_mat_bool(start,mat_op.transpuesta(state))
              start = mul_mat_bool(start,mat) 
          ans = state_click[:]
          for i in range(len(ans)):
              if ans[i][0]==True:
                  ans[i] = 1
              else:
                  ans[i]=0
          Plot(len(ans),ans)
      else: 
          for i in range(click):
              state_click = mul_mat_real(start,mat_op.transpuesta(state))
              start = mul_mat_real(start,mat)
          state_click = [[round(state_click[i][0]**2,2)] for i in range(len(state_click))]
          Plot(len(mat_op.transpuesta(state_click)),mat_op.transpuesta(state_click))
      return state_click
    ```
3. Base de datos Alsada S.A.S

  - La base de datos de Alsada S.A.S permitio que mis conocimientos en base de datos, crecieran y por decirlo nacieran, fue una experiencia agradable incursionar en la base de datos, un tema interesante, con su complejidad pero con mucha imprtancia, un posible camino futuro para la carrera.
    ```
    	/*El id del empleado se genera automaticamente debe ser de 7 digitos obligatoriamente.
		seq_idEmpleado*/
		CREATE SEQUENCE seq_idEmpleado
		START WITH 1000000
		INCREMENT BY 1;
		
		CREATE OR REPLACE TRIGGER TG_idEmpleado_Aut
		BEFORE INSERT ON Empleados
		FOR EACH ROW
		BEGIN
			:New.idEmpleado := seq_idEmpleado.nextval;
		END;
		/
    ```
