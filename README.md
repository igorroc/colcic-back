
<span id="topo"></span>

# EVRON - Back

<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->

<img src="./assets/capa.png" alt="Capa">

> Sistema de gestão de dados de cadastramento de imóveis

## 🚩 Informações do projeto

<!-- Deixe apenas um -->

![Status do projeto](https://img.shields.io/badge/status-fazendo-green)

<!-- ![Status do projeto](https://img.shields.io/badge/status-pausado-yellow)
![Status do projeto](https://img.shields.io/badge/status-finalizado-red) -->

A criação de um MVP do sistema de gerenciamento de dados de cadastramento imobiliário.

-   ### • Links úteis

    -   [Link para o Trello](https://trello.com/c/GCR0aeeO/11-layout)
    -   [Link para o Figma](https://www.figma.com/file/HzaSGcnaV3wxarWwGTgtLi/EVRON?node-id=8%3A5&t=VpnYA0NGy6TPDOgi-1)
    -   [Link para o canal no Discord](https://discord.com/channels/675516131552788508/1044725147921289219)

-   ### • Ajustes e melhorias

    O projeto ainda está em desenvolvimento e as próximas atualizações serão voltadas nas seguintes tarefas:

    -   [x] Tarefa 1
    -   [x] Tarefa 2
    -   [x] Tarefa 3
    -   [ ] Tarefa 4
    -   [ ] Tarefa 5

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:

<!-- Estes são apenas requisitos de exemplo. Adicionar, duplicar ou remover conforme necessário -->

-   Você instalou a versão mais recente de `<linguagem / dependência / requeridos>`
-   Você tem uma máquina `<Windows / Linux / Mac>`. Indique qual sistema operacional é compatível / não compatível.
-   Você leu `<guia / link / documentação_relacionada_ao_projeto>`.

## 🚀 Instalando <Evron>

Para instalar o <Evron>, siga estas etapas:

Linux e macOS:

```bash
$ <comando_de_instalação>
```

Windows:

```bash
$ <comando_de_instalação>
```

## ☕ Usando <Evron>

Para acessar as rotas do projeto:

### • Login

<details>
<summary><code>GET</code> <code><b>/autenticacao</b></code> <code>(Autentica o usuário)</code></summary>

#### • Parâmetros

> | name       | type     | data type | description      |
> | ---------- | -------- | --------- | ---------------- |
> | `username` | required | string    | Nome de usuário  |
> | `password` | required | string    | Senha do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "token": TOKEN}`        |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Formulários

<details>

<summary><code>GET</code> <code><b>/Formulario/formularios</b></code> <code>(Retorna os formulários)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Formulários": "Todos os Formulários"}`      |
> | `201`     | `application/json` | `{"code": "201", "message":"não tem formulários!"}`      |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>POST</code> <code><b>/Formulario/formularios</b></code> <code>(Envia um formulário)</code></summary>

#### • Parâmetros

> | name      | type     | data type | description                     |
> | --------- | -------- | --------- | ------------------------------- |
> | `token`   | required | string    | Token de autorização do usuário |
> | variaveis | required | object    | Variáveis do formulário         |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "message": "Formulario enviado e registro feito por User"}`      |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Lotes

<details>

<summary><code>GET</code> <code><b>/Lote/Lotes</b></code> <code>(Retorna todos os lotes)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Lotes": "Todos os lotes"}`      |
> | `404`     | `application/json` | `{"code": "404", "message":"não tem lotes!"}`      |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>POST</code> <code><b>/Lote/Lotes</b></code> <code>(Cria um lote)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |
> | file    | required | file    | Nome do lote                    |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "message": "Lote Criado!"}`  |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>PUT</code> <code><b>/Lote/Lotes</b></code> <code>(Atualiza um lote)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |
> | id      | required | string    | ID do lote                      |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "message": "lote Atualizado!"}`  |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>DELETE</code> <code><b>/Lote/Lotes</b></code> <code>(Deleta um lote)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |
> | id      | required | string    | ID do lote                      |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "message": "lote Deletado!"}`  |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>GET</code> <code><b>/Lote/Lotes/LotesDisponiveis</b></code> <code>(Retorna todos os lotes disponíveis para aquele usuário)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Lotes disponíveis": "Todos os Lotes disponíveis"}`      |
> | `404`     | `application/json` | `{"code": "404", "message": "Não tem lotes disponíveis"}`      |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Usuários-Lotes

<details>

<summary><code>GET</code> <code><b>/User_lote/Usuarios_Lotes</b></code> <code>(Retorna toda as relações de usuários e lotes)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Relações entre Usuários e Lotes": "Todas as relações"}`       |
> | `404`     | `application/json` | `{"code": "404", "message": "não tem relações!"}`       |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>GET</code> <code><b>/User_lote/Usuarios_Lotes/LotesAssociados</b></code> <code>(Retorna todos os lotes que estão sendo coletados pelo usuário logado)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Lotes Associados a User": "Todos os Lotes associados"}`       |
> | `404`     | `application/json` | `{"code": "404", "message": "Não tem lotes associados a User"}`       |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Logs

<details>

<summary><code>GET</code> <code><b>/Log_User_Lot/Logs_Usuarios_Lotes/</b></code> <code>(Retorna todos os registros de coleta e conclusão dos lotes)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Registros de coleta e conclusão": "Todos os Registros"}`       |
> | `400`     | `application/json` | `{"code":"400","message":"não tem registros!"}` |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Dados Populados do Banco

<details>

<summary><code>GET</code> <code><b>/Imovel/Imovel/</b></code> <code>(Retorna todos os dados padrão para um imóvel)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Todos os Tipos de dados": "Todos os valores dos Tipos"}`       |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

<details>

<summary><code>GET</code> <code><b>/Proprietario/Proprietario/</b></code> <code>(Retorna todos os dados padrão para um proprietário)</code></summary>

#### • Parâmetros

> | name    | type     | data type | description                     |
> | ------- | -------- | --------- | ------------------------------- |
> | `token` | required | string    | Token de autorização do usuário |

#### • Respostas

> | http code | content-type       | response                                 |
> | --------- | ------------------ | ---------------------------------------- |
> | `201`     | `application/json` | `{"code": "201", "Todos os Tipos de dados": "Todos os valores dos Tipos de dados"}`       |
> | `400`     | `application/json` | `{"code":"400","message":"Bad Request"}` |

</details>

---

### • Retorno da API

```json
[
    {"retorno de dados":
        {
        "Rota de Coleta de dados do imovel e proprietario(esses retornos são separados, cada um em sua respesctiva rota)":"-",
        "Imovel":{
            "Tipos de Logradouro": [
                {
                    "nome": "Aeroporto"
                },
                {
                    "nome": "Alameda"
                },
                {
                    "nome": "Área"
                },
                {
                    "nome": "Avenida"
                },
                {
                    "nome": "Campo"
                },
                {
                    "nome": "Chácara"
                },
                {
                    "nome": "Colônia"
                },
                {
                    "nome": "Condomínio"
                },
                {
                    "nome": "Conjunto"
                },
                {
                    "nome": "Distrito"
                },
                {
                    "nome": "Esplanada"
                },
                {
                    "nome": "Estação"
                },
                {
                    "nome": "Estrada"
                },
                {
                    "nome": "Favela"
                },
                {
                    "nome": "Fazenda"
                },
                {
                    "nome": "Feira"
                },
                {
                    "nome": "Jardim"
                },
                {
                    "nome": "Ladeira"
                },
                {
                    "nome": "Lago"
                },
                {
                    "nome": "Lagoa"
                },
                {
                    "nome": "Largo"
                },
                {
                    "nome": "Loteamento"
                },
                {
                    "nome": "Morro"
                },
                {
                    "nome": "Núcleo"
                },
                {
                    "nome": "Parque"
                },
                {
                    "nome": "Passarela"
                },
                {
                    "nome": "Pátio"
                },
                {
                    "nome": "Praça"
                },
                {
                    "nome": "Quadra"
                },
                {
                    "nome": "Recanto"
                },
                {
                    "nome": "Residencial"
                },
                {
                    "nome": "Rodovia"
                },
                {
                    "nome": "Rua"
                },
                {
                    "nome": "Setor"
                },
                {
                    "nome": "Sítio"
                },
                {
                    "nome": "Travessa"
                },
                {
                    "nome": "Trecho"
                },
                {
                    "nome": "Trevo"
                },
                {
                    "nome": "Vale"
                },
                {
                    "nome": "Vereda"
                },
                {
                    "nome": "Via"
                },
                {
                    "nome": "Viaduto"
                },
                {
                    "nome": "Viela"
                },
                {
                    "nome": "Vila"
                }
            ],
            "Fonte": [
                {
                    "nome": "Fonte 1"
                },
                {
                    "nome": "Fonte 2"
                }
            ],
            "Natureza do Imovel": [
                {
                    "nome": "Territorial"
                },
                {
                    "nome": "Predial"
                }
            ],
            "Situação": [
                {
                    "nome": "Uma Frente"
                },
                {
                    "nome": "Esquina"
                },
                {
                    "nome": "Toda Quadra"
                },
                {
                    "nome": "Mais de Uma Frente"
                },
                {
                    "nome": "Vila"
                },
                {
                    "nome": "Encravado"
                },
                {
                    "nome": "Gleba"
                }
            ],
            "Topografia": [
                {
                    "nome": "Plana"
                },
                {
                    "nome": "Aclive"
                },
                {
                    "nome": "Declive"
                },
                {
                    "nome": "Irregular"
                }
            ],
            "Pedologia": [
                {
                    "nome": "Normal"
                },
                {
                    "nome": "Inundável"
                },
                {
                    "nome": "Alagado"
                },
                {
                    "nome": "Rochoso"
                },
                {
                    "nome": "Arenoso"
                }
            ],
            "Ocupação": [
                {
                    "nome": "Construído"
                },
                {
                    "nome": "Construção em Andamento"
                },
                {
                    "nome": "Construção Paralisada"
                },
                {
                    "nome": "Em Ruínas"
                },
                {
                    "nome": "Em Demolição"
                },
                {
                    "nome": "Baldio"
                }
            ],
            "Delimitação": [
                {
                    "nome": "Murado"
                },
                {
                    "nome": "Cercado"
                },
                {
                    "nome": "Sem Delimitações"
                }
            ],
            "Uso": [
                {
                    "nome": "Sem Uso"
                },
                {
                    "nome": "Residencial"
                },
                {
                    "nome": "Comercial"
                },
                {
                    "nome": "Serviço"
                },
                {
                    "nome": "Serviço Público"
                },
                {
                    "nome": "Industrial"
                },
                {
                    "nome": "Esporte/Diversão"
                },
                {
                    "nome": "Cultura"
                },
                {
                    "nome": "Ensino"
                },
                {
                    "nome": "Saúde"
                },
                {
                    "nome": "Religioso"
                },
                {
                    "nome": "Agropecuário"
                }
            ],
            "Regime de Utilização": [
                {
                    "nome": "Próprio"
                },
                {
                    "nome": "Alugado"
                },
                {
                    "nome": "Cedido"
                },
                {
                    "nome": "Fechado"
                }
            ],
            "Tipo de Edificação": [
                {
                    "nome": "Casa"
                },
                {
                    "nome": "Apartamento"
                },
                {
                    "nome": "Sala"
                },
                {
                    "nome": "Loja"
                },
                {
                    "nome": "Galpão"
                },
                {
                    "nome": "Telheiro"
                },
                {
                    "nome": "Especial"
                }
            ]
        },
        "proprietario":{
            "Unidades Federativas": [
                {
                    "nome": "Acre",
                    "sigla": "AC"
                },
                {
                    "nome": "Alagoas",
                    "sigla": "AL"
                },
                {
                    "nome": "Amapá",
                    "sigla": "AP"
                },
                {
                    "nome": "Amazonas",
                    "sigla": "AM"
                },
                {
                    "nome": "Bahia",
                    "sigla": "BA"
                },
                {
                    "nome": "Ceará",
                    "sigla": "CE"
                },
                {
                    "nome": "Distrito Federal",
                    "sigla": "DF"
                },
                {
                    "nome": "Espírito Santo",
                    "sigla": "ES"
                },
                {
                    "nome": "Goiás",
                    "sigla": "GO"
                },
                {
                    "nome": "Maranhão",
                    "sigla": "MA"
                },
                {
                    "nome": "Mato Grosso",
                    "sigla": "MT"
                },
                {
                    "nome": "Mato Grosso do Sul",
                    "sigla": "MS"
                },
                {
                    "nome": "Minas Gerais",
                    "sigla": "MG"
                },
                {
                    "nome": "Pará",
                    "sigla": "PA"
                },
                {
                    "nome": "Paraíba",
                    "sigla": "PB"
                },
                {
                    "nome": "Paraná",
                    "sigla": "PR"
                },
                {
                    "nome": "Pernambuco",
                    "sigla": "PE"
                },
                {
                    "nome": "Piauí",
                    "sigla": "PI"
                },
                {
                    "nome": "Rio de Janeiro",
                    "sigla": "RJ"
                },
                {
                    "nome": "Rio Grande do Norte",
                    "sigla": "RN"
                },
                {
                    "nome": "Rio Grande do Sul",
                    "sigla": "RS"
                },
                {
                    "nome": "Rondônia",
                    "sigla": "RO"
                },
                {
                    "nome": "Roraima",
                    "sigla": "RR"
                },
                {
                    "nome": "Santa Catarina",
                    "sigla": "SC"
                },
                {
                    "nome": "São Paulo",
                    "sigla": "SP"
                },
                {
                    "nome": "Sergipe",
                    "sigla": "SE"
                },
                {
                    "nome": "Tocantins",
                    "sigla": "TO"
                }
            ],
            "Tipo de Pessoa": [
                {
                    "nome": "Física"
                },
                {
                    "nome": "Jurídica"
                }
            ],
            "Orgão Emissor": [
                {
                    "nome": "Secretaria de Segurança Pública",
                    "sigla": "SSP"
                },
                {
                    "nome": "Policia Militar",
                    "sigla": "PM"
                },
                {
                    "nome": "Policia Civil",
                    "sigla": "PC"
                },
                {
                    "nome": "Cartório Nacional de Títulos",
                    "sigla": "CNT"
                },
                {
                    "nome": "Diretoria de Identificação Civil",
                    "sigla": "DIC"
                },
                {
                    "nome": "Carteira de Trabalho e Previdência Social",
                    "sigla": "CTPS"
                },
                {
                    "nome": "Fundo de Garantia do Tempo de Serviço",
                    "sigla": "FGTS"
                },
                {
                    "nome": "Instituto Félix Pacheco",
                    "sigla": "IFP"
                },
                {
                    "nome": "Instituto Pereira Faustino",
                    "sigla": "IPF"
                },
                {
                    "nome": "Instituto Médico-Legal",
                    "sigla": "IML"
                },
                {
                    "nome": "Ministério do Trabalho e Emprego",
                    "sigla": "MTE"
                },
                {
                    "nome": "Ministério da Marinha",
                    "sigla": "MMA"
                },
                {
                    "nome": "Ministério da Aeronáutica",
                    "sigla": "MAE"
                },
                {
                    "nome": "Ministério do Exército",
                    "sigla": "MEX"
                },
                {
                    "nome": "Polícia Federal",
                    "sigla": "POF"
                }
            ],
            "Endereço de Emissão": [
                {
                    "nome": "Proprietário"
                },
                {
                    "nome": "Imóvel"
                }
            ]
        },


        "Rota de login":"-----------------------------",
        "Login":{
            "token": "28bb93733e00957625abf1b666e2484211bd08ef"
        },


        "Rota de Lote":"------------------------------",
        "Criar Lote(POST)":{
            "msg": "Lote Criado!"
        },
        "Pegar Lote(GET)":{
            "Lotes": [
                {
                    "id_lote": 1,
                    "nome": "bug",
                    "quadra": "10"
                }
            ]
        },
        "Atualizar Lote(PATCH/UPDATE)":{
            "msg": "lote Atualizado!"
        },
        "Deletar Lote(DELETE)":{
            "msg": "lote Deletado!"
        }},

        
        "Rota de User_lote":"---------------------------",
        "Criar relação de Usuario e Lote(POST)":{
            "msg": "binho pegou o lote 1!"
        },
        "Ver relaçoes entre usuários e lotes(GET)":{
            "Relações entre Usuários e Lotes": [
                {
                    "id_usuario_lote": 1,
                    "data_obtido": "2023-02-07T11:31:10.801030-03:00",
                    "data_concluido": "2023-02-07T11:31:10.801030-03:00",
                    "id_lote": 1,
                    "id_user": 1
                }
            ]
        },
        "Ver lotes associados ao usuário da request(GET)":{
            "Lotes Associados a binho": [
                {
                    "id_lote": 1,
                    "nome": "bug",
                    "quadra": "10"
                }
            ]
        },


        "Rota de Logs":"--------------------------------",
        "Registros de coleta e conclusão":{
            "registros de coleta e conclusão": [
                {
                    "id_log": 1,
                    "data_obtido": null,
                    "data_concluido": null,
                    "id_lote": 1,
                    "id_user": 1
                },
                {
                    "id_log": 2,
                    "data_obtido": "2023-02-07T11:31:10.801030-03:00",
                    "data_concluido": null,
                    "id_lote": 1,
                    "id_user": 1
                }
            ]
        },


        "Rotas de Formulário":"---------------------",
        "Criar um Formulário(POST)":{
            "msg": "Formulario enviado e registro feito por binho"
        },
        "Ver os Formulários(GET)":{
            "Formulários": {
                "Formulário": [
                    {
                        "id_formulario": 1,
                        "imovel": {
                            "quadra": 2,
                            "lote": 1,
                            "id_caracteristicas": {
                                "area_construida": 100,
                                "area_unidade": 10,
                                "area_privativa": 20,
                                "area_construida_total": 70,
                                "num_blocos": 50,
                                "num_unidades": 2,
                                "num_pavimentos": 4,
                                "id_natureza": {
                                    "nome": "Predial"
                                },
                                "id_hidrometro": {
                                    "num_matricula": 122045,
                                    "quant_casas_atende": 1
                                },
                                "id_situacao": {
                                    "nome": "Esquina"
                                },
                                "id_topografia": {
                                    "nome": "Plana"
                                },
                                "id_pedologia": {
                                    "nome": "Arenoso"
                                },
                                "id_ocupacao": {
                                    "nome": "Construído"
                                },
                                "id_delimitacao": {
                                    "nome": "Murado"
                                },
                                "id_uso": {
                                    "nome": "Comercial"
                                },
                                "id_regime_utilizacao": {
                                    "nome": "Próprio"
                                },
                                "id_tipo_edificacao": {
                                    "nome": "Casa"
                                }
                            },
                            "id_insc_imob": {
                                "num_lograd": "012",
                                "num_metrico": "100",
                                "sub_num": "12",
                                "bloco": "03"
                            },
                            "id_endereco": {
                                "numero": 123,
                                "complemento": "Casa",
                                "id_bairro": {
                                    "nome": "Vespasiano"
                                },
                                "id_logradouro": {
                                    "nome": "Vila",
                                    "tipo": {
                                        "nome": "Vila"
                                    }
                                }
                            },
                            "id_fonte": {
                                "nome": "Fonte 1"
                            },
                            "id_empreendimento": {
                                "nome": "nenhum"
                            }
                        },
                        "proprietario": {
                            "nome": "Larissa",
                            "telefone": "73 99933 33 44",
                            "cpf": "123.456.789-90",
                            "tipo_pessoa": {
                                "nome": "Física"
                            },
                            "endereço": {
                                "logradouro": "algum",
                                "bairro": "Vespasiano",
                                "cidade": "itagimirim",
                                "uf_endereço": {
                                    "nome": "Bahia",
                                    "sigla": "BA"
                                },
                                "cep": "45850-000"
                            },
                            "endereço_emissao": {
                                "nome": "Imóvel"
                            },
                            "identidade": {
                                "num_identidade": "123456789110",
                                "orgao": {
                                    "nome": "Polícia Federal",
                                    "sigla": "POF"
                                },
                                "uf": {
                                    "nome": "Bahia",
                                    "sigla": "BA"
                                }
                            }
                        },
                        "estado": {
                            "nome": "Bahia",
                            "sigla": "BA"
                        },
                        "titulo": "teste1601.2",
                        "cidade": "itagimirim",
                        "pais": "BR",
                        "id_lote": 1
                    }]
            }
        }
    }
]
```

---

## 🤝 Equipe

Membros da equipe de desenvolvimento do projeto:

<table>
  <tr style="display: flex; flex-wrap: wrap;">
    <td align="center">
      <a href="https://github.com/gannjobs">
        <img src="https://github.com/gannjobs.png" width="100px;" alt="Foto de Joabe Ferreira"/><br>
        <b>Joabe Ferreira</b>
        <p>Desenvolvedor Back</p>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/laribrito">
        <img src="https://github.com/laribrito.png" width="100px;" alt="Foto de Larissa Brito"/><br>
        <b>Larissa Brito</b>
        <p>Desenvolvedora Back</p>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/jvrupp">
        <img src="https://github.com/jvrupp.png" width="100px;" alt="Foto de João Rupp"/><br>
        <b>João Rupp</b>
        <p>Desenvolvedor Back</p>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/brunofelipecoder">
        <img src="https://github.com/brunofelipecoder.png" width="100px;" alt="Foto de Bruno Felipe"/><br>
        <b>Bruno Felipe</b>
        <p>Desenvolvedor Back</p>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/igorroc">
        <img src="https://github.com/igorroc.png" width="100px;" alt="Foto de Igor Rocha"/><br>
        <b>Igor Rocha</b>
        <p>Desenvolvedor Front</p>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/mr-nascimento">
        <img src="https://github.com/mr-nascimento.png" width="100px;" alt="Foto de Igor Nascimento"/><br>
        <b>Igor Nascimento</b>
        <p>Desenvolvedor Front</p>
      </a>
    </td>
  </tr>
</table>

[⬆ Voltar ao topo](#topo)<br>
