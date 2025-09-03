# frontend/Dockerfile
FROM python:3.13-slim

# Definir o diretório de trabalho no container
WORKDIR /app

# Copiar os arquivos de dependências primeiro (para cache)
COPY requirements.txt .

# Instalar dependências
RUN pip install --no-cache-dir --upgrade -r requirements.txt

# Copiar o restante dos arquivos do projeto
COPY . .

# Expor a porta
EXPOSE 8501

# Comando para executar a aplicação
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]