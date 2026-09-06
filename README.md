# Exercício Módulo 21 - Back End Python EBAC

# FastAPI + Docker + Poetry

Aplicação FastAPI containerizada com Docker e gerenciamento de dependências via Poetry, incluindo hot-reload para desenvolvimento.

O arquivo .env é de uso exclusivo da equipe de desenvolvimento do projeto, mas para fins de estudo está disponível nesse repositório (por se tratar de um programa pouco complexo)

## Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Como executar

1. Clone o repositório:

```bash
   git clone https://github.com/lucas-machi/exercicio-m21-backend
```

2. Construa e inicie os containers em segundo plano:

```bash
   docker-compose up --build -d
```

3. Acesse a aplicação em:
http://localhost:8000


4. Para parar os containers:

```bash
   docker-compose down
```

## Desenvolvimento

O código-fonte é montado como volume no container, então qualquer alteração nos arquivos `.py` recarrega a aplicação automaticamente (hot-reload via `--reload` do Uvicorn).


## Variáveis de ambiente

As variáveis de ambiente usadas pela aplicação estão definidas no `docker-compose.yml`, na seção `environment`. Ajuste conforme necessário para o seu ambiente.

## Comandos úteis

| Comando | Descrição |
|---|---|
| `docker-compose up --build -d` | Constrói as imagens e inicia os containers em background |
| `docker-compose down` | Para e remove os containers |
| `docker-compose logs -f` | Acompanha os logs da aplicação em tempo real |
| `docker-compose exec app bash` | Abre um shell dentro do container da aplicação |
