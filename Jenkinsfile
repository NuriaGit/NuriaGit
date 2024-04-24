def numero1 = 10
def numero2 = 2
def texto

pipeline
{
  agent any
  stages
  {
      stage("Calculos")
      {
          steps
          {
              script
              {
                 suma = numero1 + numero2
                 texto = "La suma de " + numero1 + " y " + numero2 + " es " + suma
                 println "La suma de " + numero1 + " y " + numero2 + " es " + suma
                  
                 resta = numero1 - numero2
                 texto = texto + "\nLa resta de " + numero1 + " y " + numero2 + " es " + resta
                 println "La resta de " + numero1 + " y " + numero2 + " es " + resta
              
                 multiplicacion = numero1 * numero2
                 texto = texto + "\nLa multiplicación de " + numero1 + " y " + numero2 + " es " + multiplicacion
                 println "La multiplicación de " + numero1 + " y " + numero2 + " es " + multiplicacion
             
                 if (numero1 == 0 || numero2 == 0)
                    division = 0
                 else
                    division = numero1 / numero2
                 texto = texto + "\nLa división de " + numero1 + " y " + numero2 + " es " + division
                 println "La división de " + numero1 + " y " + numero2 + " es " + division
              }
          }
      }

      stage("Ejecutar comando de CMD")
      {
            steps
            {
                bat "ipconfig /flushdns"
            }
      }
    
      stage("Crear fichero")
      {
          steps
          {
              script
              {
                  writeFile(file: "Ejercicio_3.txt", text: texto)
                  println "fichero Ejercicio_3.txt generado"
              }
          }    
      }
  }
}
