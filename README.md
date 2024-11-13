# Build a Simple LLM Application with LCEL

## Resumen
Aplicación construida con LangChain para traducción de texto a otro idioma. Se usa un modelo de lenguaje (LLM) para 
realizar la traducción mediante una llamada y algunas plantillas de mensajes. Es un tutorial para el aprendizaje a trabajar con LangChain y sus funcionalidades.

## Descripción General

- Uso de modelos de lenguaje (LLM)
- Encadenar componentes usando el Lenguaje de Expresiones de LangChain (LCEL)
- Realizar seguimiento y depuración de la aplicación
- Despliegue IA con LangServe


## Arquitectura de la Aplicación

![image](https://github.com/user-attachments/assets/b6bc00e9-c5d0-49c2-aac2-f059a76bd9b8)


Esta aplicación utiliza LangChain para traducir texto de manera eficiente. La arquitectura se divide en los siguientes componentes:
- **PromptTemplate:** Define la estructura del mensaje que el modelo recibirá, indicando qué texto traducir y a qué idioma.
- **LLM Model:** El modelo de lenguaje encargado de procesar el texto y realizar la traducción.
- **OutputParser:** Extrae la respuesta generada por el modelo y la convierte en un formato legible.
- **Encadenamiento (LCEL):** LangChain permite conectar estos componentes en un flujo, usando el operador | para encadenar el PromptTemplate, el modelo LLM y el OutputParser.
- **LangSmith:** Ofrece seguimiento y trazabilidad de las ejecuciones, permitiendo depurar y observar los pasos del proceso de traducción.
- **LangServe:** Una capa de despliegue que expone la cadena como una API REST mediante FastAPI.


## Uso      

1. Para iniciar el servidor, ejecuta:
``` 
python langchainserver.py
```
2. Para iniciar el cliente, ejecuta:
``` 
python langchainclient.py
```
3.  La API estará disponible en http://localhost:8000/chain. También se puede acceder en http://localhost:8000/chain/playground para probar el servicio con streaming de salida.

## Pruebas

### Cliente
![image](https://github.com/user-attachments/assets/73996fe1-2819-469b-9b26-abbd07c0ad53)

### Servidor
![image](https://github.com/user-attachments/assets/5af617cd-9e64-47b6-a763-6c8898ce86a2)
![image](https://github.com/user-attachments/assets/713bf5e7-d35c-4032-a395-f3ab5104a2bf)
![image](https://github.com/user-attachments/assets/71984914-4aef-4cdc-b37d-9dc89f910b6d)


## Autor

- [Daniel Felipe Rojas Hernandez](https://github.com/Knight072)


## Licencia


Este proyecto está bajo la Licencia (MIT) - ver el archivo [LICENSE](LICENSE.md) para ver más detalles.
