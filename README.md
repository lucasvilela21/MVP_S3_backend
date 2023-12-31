# Minha API MVP

Projeto de MVP para conclusão do Sprint 3 da Pós Graduação em Engenharia de Software pela PUC-RIO.

Projeto com finalidade de cadastrar Artesões e Vendas dos Artesões, para futuro uso em uma feira de voluntários da APAE de 
Mogi das Cruzes.

---
## Como executar 

Será necessário ter todas as libs python listadas no `requirements.txt` instaladas.
Após clonar o repositório, é necessário ir ao diretório raiz, pelo terminal, para poder executar os comandos descritos abaixo.

> É fortemente indicado o uso de ambientes virtuais do tipo [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html).

```
(env)$ pip install -r requirements.txt
```

Este comando instala as dependências/bibliotecas, descritas no arquivo `requirements.txt`.

Para executar a API  basta executar:

```
(env)$ flask run --host 0.0.0.0 --port 5001
```

Em modo de desenvolvimento é recomendado executar utilizando o parâmetro reload, que reiniciará o servidor
automaticamente após uma mudança no código fonte. 

```
(env)$ flask run --host 0.0.0.0 --port 5001 --reload
```

Abra o [http://localhost:5001/#/](http://localhost:5001/#/) no navegador para verificar o status da API em execução.


## Como executar através do Docker

Certifique-se de ter o [Docker](https://docs.docker.com/engine/install/) instalado e em execução em sua máquina.

Navegue até o diretório que contém o Dockerfile e o requirements.txt no terminal.
Execute **como administrador** o seguinte comando para construir a imagem Docker:

```
$ docker build --pull --rm -f "backend\Dockerfile" -t mvpbackend "backend"  
```

Uma vez criada a imagem, para executar o container basta executar, **como administrador**, seguinte o comando:

```
$ docker run -p 5001:5001 mvpbackend
```

Uma vez executando, para acessar a API, basta abrir o [http://localhost:5001/#/](http://localhost:5001/#/) no navegador.