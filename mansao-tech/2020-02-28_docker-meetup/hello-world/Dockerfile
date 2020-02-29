# Instala a imagem oficial do Python v3.8.1 "alpine" (mais leve)
FROM python:3.8.1-alpine

# Define o diretório de trabalho e copia os dados para lá
WORKDIR /usr/src/app
COPY . /usr/src/app

# Instala as dependências do Postgres para executar com o Python
# RUN apk add gcc musl-dev postgresql-dev python3-dev bash

# Atualiza o gerenciador de pacote do Python (pip) e instala as suas dependências
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Expõe a porta 5000 para uso do app Python/Flask
EXPOSE 5000

# Executa a aplicação
CMD ["python", "./app.py"]

# Instalação
    # Docker: https://docs.docker.com/install/linux/docker-ce/ubuntu/
    # Instale o Docker Compose: https://docs.docker.com/compose/install/

# Para executar apenas o container do Python:
    # docker build -t meetup-docker .
    # docker run -it -p 5000:5000 --rm --name meetup-docker meetup-docker

# Para executar o container Python + Postgres com o Compose:
    # docker-compose build
    # docker-compose up

# Projeto real utilizando Docker, site do www.pyjobs.com.br
    # https://github.com/vmesel/PyJobs
