Minha API em REST
Este pequeno projeto faz parte do material diático da Disciplina Desenvolvimento Full Stack 

O projeto consiste em uma api rest + api externa da viacep + interface(front end), onde será realizada na api externa consultas por cep, para identificar o endereco correto das pessoas. Isso para criar um sistema de encomendas em uma determina regiao, com o intuito de impulsionar a efetividade de uma empresa que realiza encomendas por si própria.

O objetivo aqui é apresetar uma API emplementada seguindo o estilo REST.

As principais tecnologias que serão utilizadas aqui é o:

Flask
SQLAlchemy
OpenAPI3
SQLite
Instalação
Será necessário ter todas as libs python listadas no requirements.txt instaladas. Após clonar o repositório, é necessário ir ao diretório raiz, pelo terminal, para poder executar os comandos descritos abaixo.

É fortemente indicado o uso de ambientes virtuais do tipo virtualenv.

(env)$ pip install -r requirements.txt
Este comando instala as dependências/bibliotecas, descritas no arquivo requirements.txt.

Executando o servidor
Para executar a API basta executar:



(env)$ flask run --host 0.0.0.0 --port 5000
Em modo de desenvolvimento é recomendado executar utilizando o parâmetro reload, que reiniciará o servidor automaticamente após uma mudança no código fonte.



(env)$ flask run --host 0.0.0.0 --port 5000 --reload
Acesso no browser

Abra o http://localhost:5000/#/ no navegador para verificar o status da API em execução.

Como executar através do Docker
Certifique-se de ter o Docker instalado e em execução em sua máquina.

Navegue até o diretório que contém o Dockerfile e o requirements.txt no terminal. Execute como administrador o seguinte comando para construir a imagem Docker:

$ docker build -t rest-api . ou docker build -t rest-api ./minhaapi

Uma vez criada a imagem, para executar o container basta executar, como administrador, seguinte o comando:

$ docker run -p 5000:5000 rest-api
Uma vez executando, para acessar a API, basta abrir o http://localhost:5000/#/ no navegador.

Alguns comandos úteis do Docker
Para verificar se a imagem foi criada você pode executar o seguinte comando:

$ docker images
Caso queira remover uma imagem, basta executar o comando:

$ docker rmi <IMAGE ID>
Subistituindo o IMAGE ID pelo código da imagem

Para verificar se o container está em exceução você pode executar o seguinte comando:

$ docker container ls --all
Caso queira parar um conatiner, basta executar o comando:

$ docker stop <CONTAINER ID>
Subistituindo o CONTAINER ID pelo ID do conatiner

Caso queira destruir um conatiner, basta executar o comando:

$ docker rm <CONTAINER ID>
Para mais comandos, veja a documentação do docker.