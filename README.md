Este script carga en memoria diferentes conjuntos de datos de tiendas a partir de archivos CSV alojados en la web o en rutas específicas.

📌 Descripción
El código utiliza la librería pandas para leer datos desde cuatro fuentes distintas (url, url2, url3, url4), almacenando cada dataset en un DataFrame separado:

python
Copiar
Editar
import pandas as pd

tienda = pd.read_csv(url)
tienda2 = pd.read_csv(url2)
tienda3 = pd.read_csv(url3)
tienda4 = pd.read_csv(url4)
tienda → Datos de la tienda principal.

tienda2 → Datos de la segunda tienda.

tienda3 → Datos de la tercera tienda.

tienda4 → Datos de la cuarta tienda.

📦 Requisitos
Python 3.8 o superior

Librería pandas instalada

bash
Copiar
Editar
pip install pandas
▶️ Uso
Asegúrate de tener las variables url, url2, url3, url4 definidas con las direcciones de los CSV (pueden ser URLs o rutas locales).

Ejecuta el script para cargar los datos en memoria.

Una vez cargados, puedes manipular, limpiar o analizar los DataFrames según tus necesidades.

💡 Ejemplo de uso posterior
python
Copiar
Editar
Ver las primeras filas de tienda3
print(tienda3.head())

Filtrar productos con precio mayor a 100
productos_caros = tienda[tienda['precio'] > 100]
🗂 Notas
Asegúrate de que las URLs o rutas sean accesibles y que los archivos CSV tengan el formato correcto (separador, codificación).

Si los archivos usan otro separador (por ejemplo, ;), agrega el parámetro sep=";" en read_csv.
