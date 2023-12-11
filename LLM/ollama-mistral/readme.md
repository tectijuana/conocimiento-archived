Para generar un script de prueba de estrés para un modelo de lenguaje como "Ollama" instalado localmente en un MacBook Pro, podemos crear un código en Python que envíe solicitudes de manera repetida y mida el tiempo de respuesta del modelo. Este tipo de prueba puede ayudar a identificar cómo el modelo maneja cargas de trabajo intensas.

El siguiente es un ejemplo básico de cómo podrías hacer esto:

```python
import time
import requests

def stress_test(model_url, test_phrase, num_requests):
    total_time = 0

    for i in range(num_requests):
        start_time = time.time()

        # Envía la solicitud al modelo
        response = requests.post(model_url, json={"prompt": test_phrase})

        # Mide el tiempo de respuesta
        elapsed_time = time.time() - start_time
        total_time += elapsed_time

        print(f"Request {i+1}: {elapsed_time} seconds")

    print(f"Average response time: {total_time / num_requests} seconds")

# URL del modelo Ollama
model_url = "http://localhost:port"  # Reemplaza 'port' con el puerto correcto
test_phrase = "Describe the Eiffel Tower."
num_requests = 100

stress_test(model_url, test_phrase, num_requests)
```

Este script realiza las siguientes acciones:
1. Envía 100 solicitudes (o el número que definas) al modelo "Ollama".
2. Mide y registra el tiempo de respuesta de cada solicitud.
3. Calcula y muestra el tiempo promedio de respuesta.

**Nota importante:** 
- Asegúrate de tener el servidor del modelo "Ollama" corriendo localmente y reemplaza `"http://localhost:port"` con la URL y puerto correctos.
- Este script usa la biblioteca `requests` de Python, asegúrate de tenerla instalada (`pip install requests`).
- Este código es solo un ejemplo básico. Puedes necesitar ajustarlo según la API específica de "Ollama" y tus necesidades de prueba.


# PRUEBA ELABORADA 

```bash
➜  ~ python3 test.py
/Users/rene/Library/Python/3.9/lib/python/site-packages/urllib3/__init__.py:34: NotOpenSSLWarning: urllib3 v2 only supports OpenSSL 1.1.1+, currently the 'ssl' module is compiled with 'LibreSSL 2.8.3'. See: https://github.com/urllib3/urllib3/issues/3020
  warnings.warn(
Request 1: 0.009418010711669922 seconds
Request 2: 0.002167940139770508 seconds
Request 3: 0.0018551349639892578 seconds
Request 4: 0.0017511844635009766 seconds
Request 5: 0.0017828941345214844 seconds
Request 6: 0.0021059513092041016 seconds
Request 7: 0.002398252487182617 seconds
Request 8: 0.002482175827026367 seconds
Request 9: 0.0019159317016601562 seconds
Request 10: 0.0017809867858886719 seconds
Request 11: 0.002168893814086914 seconds
Request 12: 0.0022962093353271484 seconds
....
....
....
Request 90: 0.0016658306121826172 seconds
Request 91: 0.0017290115356445312 seconds
Request 92: 0.0016779899597167969 seconds
Request 93: 0.0016138553619384766 seconds
Request 94: 0.0016090869903564453 seconds
Request 95: 0.00168609619140625 seconds
Request 96: 0.00164794921875 seconds
Request 97: 0.0016391277313232422 seconds
Request 98: 0.001631021499633789 seconds
Request 99: 0.0017473697662353516 seconds
Request 100: 0.0020542144775390625 seconds
Average response time: 0.0018872714042663574 seconds
```

