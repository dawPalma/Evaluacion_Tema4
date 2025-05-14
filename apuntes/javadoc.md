# Apuntes sobre Javadoc

Javadoc es una herramienta que permite generar documentación en formato HTML a partir de comentarios en el código fuente de Java. Esta documentación es útil para desarrolladores y usuarios para entender el funcionamiento de una aplicación.

---

## Comentarios de Documentación:
Para que Javadoc genere la documentación, los comentarios deben estar estructurados de una forma específica, y deben colocarse **encima de clases, métodos o atributos**:

```java
/**
 * Esta clase representa un coche con sus atributos y métodos.
 */
public class Coche {
    
    /**
     * Marca del coche.
     */
    private String marca;
    
    /**
     * Modelo del coche.
     */
    private String modelo;
    
    /**
     * Constructor de la clase Coche.
     * 
     * @param marca Marca del coche.
     * @param modelo Modelo del coche.
     */
    public Coche(String marca, String modelo) {
        this.marca = marca;
        this.modelo = modelo;
    }
    
    /**
     * Devuelve la marca del coche.
     * 
     * @return La marca del coche.
     */
    public String getMarca() {
        return marca;
    }
    
    /**
     * Establece la marca del coche.
     * 
     * @param marca Nueva marca del coche.
     */
    public void setMarca(String marca) {
        this.marca = marca;
    }
}
Etiquetas Comunes:
@param: Describe un parámetro de un método.

@return: Explica el valor de retorno de un método.

@throws: Indica las excepciones que un método puede lanzar.

@see: Enlaza con otras clases o métodos.

@deprecated: Marca un método o clase como obsoleto.

Generación de la Documentación:
Para generar la documentación en HTML, se usa el siguiente comando en la terminal, estando en el directorio donde se encuentra el archivo .java:

bash
Copiar
Editar
javadoc -d ./doc *.java
-d: Define el directorio donde se guardará la documentación.

*.java: Indica que se generará la documentación de todos los archivos Java del directorio.

Navegar por la Documentación:
Una vez generada, se crea una carpeta llamada doc con un archivo index.html. Para visualizarla, puedes abrirlo en un navegador:

bash
Copiar
Editar
firefox doc/index.html
Buenas Prácticas:
Comentar todas las clases y métodos públicos.

Usar etiquetas correctamente para una documentación clara.

Actualizar los comentarios si el método cambia.

Mantener un estilo uniforme en toda la aplicación.
