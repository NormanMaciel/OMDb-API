# OMDb-API
The OMDb API is a RESTful web service to obtain movie information


# OMDb API Java Integration

## Descripción

Este proyecto implementa la [OMDb API](http://www.omdbapi.com/) (Open Movie Database API) utilizando **Java**. La OMDb API proporciona información detallada sobre películas, series de televisión, episodios y más, incluyendo detalles como el elenco, directores, calificaciones, sinopsis y géneros.

Con esta integración, puedes realizar búsquedas de películas y series por título, obtener información detallada sobre una película específica utilizando su ID de IMDb, e incluso acceder a las calificaciones de diferentes fuentes como IMDb, Rotten Tomatoes, y Metacritic.

## Características del proyecto

- Búsqueda de películas/series por título.
- Búsqueda avanzada con filtros como año o tipo de contenido (película/serie/episodio).
- Obtención de información detallada de películas utilizando el ID de IMDb.
- Manejo de datos en formato JSON.
- Despliegue de resultados en consola o interfaces gráficas de usuario (pendiente de implementación).

## Tecnologías utilizadas

- **Lenguaje**: Java 8+
- **API utilizada**: OMDb API
- **Dependencias**:
  - `HttpClient` para realizar peticiones HTTP.
  - `JSON` para el manejo de la respuesta.

## Instalación y configuración

1. Clonar el repositorio:

    ```bash
    git clone https://github.com/tu-usuario/omdb-java-integration.git
    ```

2. Obtener una API Key de OMDb:

    - Ve a [OMDb API](http://www.omdbapi.com/apikey.aspx) y regístrate para obtener tu propia clave API (gratuita o de pago, según el uso que necesites).

3. Configurar la API Key:

    - Añade tu API Key en el archivo `config.properties` o en el código donde se realiza la petición HTTP.

4. Compilar el proyecto:

    Puedes compilar y ejecutar el proyecto utilizando Maven o Gradle.

    - **Con Maven**:

      ```bash
      mvn clean install
      ```

    - **Con Gradle**:

      ```bash
      gradle build
      ```

## Uso

### Ejemplo de uso básico

```java
// Ejemplo simple de cómo realizar una búsqueda de película por título
public class OMDbClient {
    private static final String API_KEY = "tu_api_key";
    private static final String BASE_URL = "http://www.omdbapi.com/";

    public static void main(String[] args) throws Exception {
        String title = "Inception";
        String url = BASE_URL + "?t=" + title + "&apikey=" + API_KEY;
        
        // Aquí realizas la petición HTTP y procesas la respuesta JSON
        String jsonResponse = makeHttpRequest(url);
        System.out.println("Respuesta de OMDb API: " + jsonResponse);
    }

    private static String makeHttpRequest(String url) throws IOException {
        // Implementación de petición HTTP
    }
}
