<h1>Simulador de API - Monitoramento GoodWe (Mock Server)</h1>

Este projeto é uma API simples feita em FastAPI que simula o comportamento de uma API de monitoramento de energia solar da GoodWe.
Ela serve como um mock server, gerando dados aleatórios de status, consumo e geração, para que você possa testar a sua Alexa Skill sem precisar de uma API externa real.
<h2>Endpoints Disponíveis</h2>
Rota	Método	Descrição	Exemplo de Retorno
/status	GET	Retorna um status aleatório do sistema	{ "status": "Operando normalmente" }
/consumo	GET	Retorna um valor de consumo aleatório (kW)	{ "consumo": "3.45 kW" }
/geracao	GET	Retorna um valor de geração aleatório (kW)	{ "geracao": "6.28 kW" }
<h2>Como Rodar Localmente</h2>

    Instale as dependências:

pip install fastapi uvicorn

    Rode o servidor:

uvicorn main:app --reload

    Isso vai disponibilizar a API localmente em:
    http://127.0.0.1:8000

<h2>Exemplos de Teste</h2>

    Status:
    GET http://127.0.0.1:8000/status

    Consumo:
    GET http://127.0.0.1:8000/consumo

    Geração:
    GET http://127.0.0.1:8000/geracao

<h2>Testando no Navegador</h2>

Você também pode abrir no navegador a documentação automática gerada pelo FastAPI:

    Swagger UI:
    http://127.0.0.1:8000/docs

    Redoc:
    http://127.0.0.1:8000/redoc

<h2>Lógica Interna</h2>

    Os dados são gerados aleatoriamente a cada requisição.

    Não há persistência de dados.

    Ideal apenas para testes locais ou de desenvolvimento.

<h1>Observações Importantes</h2>

    Este projeto não é uma API oficial da GoodWe.

    É apenas uma simulação para fins de desenvolvimento e teste de integração com a Alexa Skill.

