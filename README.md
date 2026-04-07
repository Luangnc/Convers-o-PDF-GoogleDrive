# Conversor-PDF-GoogleDrive
Faz a conversão de ficheiros PDF online para o Google Drive utilizando Google collab.

# 1. Abrir o Colab
Acesse: https://colab.research.google.com
Clique em “Novo notebook”

# 2. Colar o código
Cole isso em uma célula:

```python 

import requests

url = "https://YOURLINK"
r = requests.get(url)

with open("/content/arquivo.pdf", "wb") as f:
    f.write(r.content)
```
# 3. Executar
Clique no botão ▶️ (play)
Aguarde alguns segundos

👉 Isso vai:
baixar o PDF
salvar como arquivo.pdf

# 4. Salvar no Google Drive
✔️ Método automático.

Adicione isso em outra célula:
```python
from google.colab import drive
drive.mount('/content/drive')
```
👉 Vai pedir autorização (login Google)

# 5. Depois copie o arquivo para o Drive:
 ```python
import shutil

shutil.copy("/content/arquivo.pdf", "/content/drive/MyDrive/arquivo.pdf")
```
Depois só verificar o arquivo na sua pasta do google drive.
