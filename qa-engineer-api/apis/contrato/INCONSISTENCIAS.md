# Inconsitências encontradas

Neste arquivo descrevo algumas inconsistências que encontrei ao estudar a documentação e a API propriamente dita.

## Documentação

- Na página https://docs.idwall.co/docs/what-is-a-report, o link do segundo parágrafo na palavra "dashboard" aponta para a url https://dashboard.idwall.co/reports, caindo numa tela de login. Este link não deveria ser para https://docs.idwall.co/docs/dashboard?

- No repositório https://github.com/idwall/desafios-qa/tree/master/qa-engineer-api/apis, na parte "Dicas", a locução "dia a dia" não possui hífen com o novo acordo ortográfico.

- Na mesma seção acima, último item, está escrito "independênte". Esta palavra não possui acento (independente).

- Na página https://github.com/idwall/desafios-qa, seção Carreira IDwall, o link Carreira IDwall, dá 404 (https://idwall.gupy.io/).

- Na página https://docs.idwall.co/docs/what-is-a-report, seção "Creating report", link da palavra "dashboard" leva a uma página 404 (https://docs.idwall.co/v2.1/docs/dashboard#section-integra-o-api)

- Na página https://github.com/idwall/desafios-qa/tree/master/qa-engineer-api/apis, em "Atenção: Não armazenar o token nos arquivos deste projeto!", deve ser usado "onde" e não "aonde". "Aonde" tem sentido de destino e "onde" expressa ideia de local fixo, moradia, justificando o uso do advérbio onde.


## API
### Por que no Cenário 1 é [ERROR] e no Cenário 2 é [INVALID]
https://github.com/idwall/desafios-qa/tree/master/qa-engineer-api/apis
#### Cenário 1: Regra de data diferente
"mensagem": "Inválido. [ERROR] Não foi possível validar: Data de nascimento informada está divergente da constante na base de dados da Secretaria da Receita Federal do Brasil.",

#### Cenário 2: Regra de nome diferente
"mensagem": "Inválido. [INVALID] Nome diferente do cadastrado na Receita Federal.",

### Por que utilizar horário Zulu nas requisições?

### Contrato de geração de relatório diferente da documentação
https://docs.idwall.co/docs/what-is-a-report
Falta o campo "validation" especificado na documentação

na documentação
{
    "error": "Bad Request",
    "message": "child \"parametros\" fails because [\"dado_aleatorio\" is not allowed]",
    "validation": {
        "source": "payload",
        "keys": [
            "parametros.dado_aleatorio"
        ]
    },
    "status_code": 400
}

retorno real

{
    "error": "Unauthorized",
    "message": "Falha na autenticação. Por favor verifique o token utilizado e se o acesso foi liberado.",
    "status_code": 401
}

### Inconsistência de nomenclatura: "matriz" no POST e "nome" no GET
No payload do POST para o endpoint /relatorios é passado o seguinte parâmetro:
"matriz": "consultaPessoaDefault"

Já no GET para o mesmo endpoint o "consultaPessoaDefault" possui a chave "nome"
"nome": "consultaPessoaDefault"

Essa diferença de nomes para o mesmo parâmetro gera confusão. Favor padronizar.
