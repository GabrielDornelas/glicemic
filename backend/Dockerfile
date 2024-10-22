# Use uma imagem base oficial do Python
FROM python:3

# Defina o diretório de trabalho no container
WORKDIR /glicemic/backend/

# Copie o arquivo de requisitos para o diretório de trabalho
COPY requirements.txt .

# Instale as dependências da API Django
RUN pip install --no-cache-dir -r requirements.txt

# Copie todos os arquivos do backend para o diretório de trabalho
COPY . .

# Exponha a porta do Django (a padrão é 8000)
EXPOSE 8000

# Comando para iniciar o servidor de desenvolvimento do Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
