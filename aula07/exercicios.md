# Aula 07: Exercícios

Exercícios da [lista do professor](https://github.com/Herysson/Engenharia-de-Software/blob/main/Exerc%C3%ADcios/Requisitos%20-%20Lista%20de%20Exerc%C3%ADcios.pdf) e as práticas do slide final. Os conceitos estão no [resumo da aula](README.md).

Cada exercício tem **uma** solução possível, escondida: clique em **Ver solução** para abrir. Tente fazer antes de olhar.

Categorias usadas nas soluções:
- **RF** (requisito funcional): o que o sistema deve fazer. É um verbo.
- **RNF** (requisito não funcional): qualidade ou restrição, com a categoria da aula (produto, organizacional ou externo).
- **Normativo**: imposto por lei, norma ou regulamento. A aula não define esse termo; o mais próximo nos slides é o RNF externo (legal/ético).
- **Regra de negócio**: política, condição ou restrição da organização (definição da aula 09).

## Sumário

| # | Exercício | Origem |
|---|---|---|
| 1 | [A Fazenda Digital](#1-a-fazenda-digital) | lista |
| 2 | [Clínica Medisafe](#2-clínica-medisafe) | lista |
| 3 | [Sistema de biblioteca](#3-sistema-de-biblioteca) | slides, Prática 1 |
| 4 | [Documento de requisitos livre](#4-documento-de-requisitos-livre) | slides, Prática 2 |

---

### 1. A Fazenda Digital

> João quer modernizar a fazenda com um sistema integrado: painel de controle acessível pelo computador e pelo smartphone; sensores que preveem o clima e alertam sobre tempestades e secas; irrigação controlada pelos dados dos sensores, sem desperdício; câmeras que identificam pragas e doenças e alertam na hora; controle de inventário com avisos de falta ou excedente; um e-commerce para vender direto aos consumidores, com pedidos e agendamento de entregas; câmeras de segurança monitoradas em tempo real; integração com os dispositivos inteligentes que ele já tem; facilidade de uso, tutoriais em vídeo e manuais; um canal de suporte; e conformidade com as regulamentações de agricultura, comércio eletrônico e privacidade.
>
> Identifique e classifique os requisitos em funcionais, não funcionais e normativos.

<details>
<summary>Ver solução</summary>

**Requisitos funcionais**

| ID | Requisito |
|---|---|
| RF01 | O sistema deve exibir um painel de controle com o monitoramento de todos os aspectos da fazenda. |
| RF02 | O sistema deve prever as condições climáticas a partir dos dados dos sensores. |
| RF03 | O sistema deve alertar o João sobre possíveis tempestades ou períodos de seca. |
| RF04 | O sistema deve controlar a irrigação com base nos dados dos sensores. |
| RF05 | O sistema deve identificar pragas ou doenças nas plantas pelas imagens das câmeras e alertar o João. |
| RF06 | O sistema deve monitorar o inventário e notificar quando os suprimentos estiverem baixos ou houver excedente de produtos. |
| RF07 | O sistema deve permitir que os clientes façam pedidos dos produtos da fazenda. |
| RF08 | O sistema deve permitir que os clientes agendem a entrega dos pedidos. |
| RF09 | O sistema deve permitir monitorar as câmeras de segurança em tempo real. |
| RF10 | O sistema deve oferecer um canal para o João entrar em contato com o suporte. |

**Requisitos não funcionais**

| ID | Requisito | Categoria |
|---|---|---|
| RNF01 | A interface deve ser amigável e fácil de usar por quem não é especialista em tecnologia. | produto: usabilidade |
| RNF02 | O painel deve poder ser acessado pelo computador e pelo smartphone. | produto: portabilidade |
| RNF03 | A irrigação deve fornecer a quantidade adequada de água, evitando desperdício. | produto: eficiência |
| RNF04 | O alerta de pragas e doenças deve ser imediato. | produto: eficiência (tempo de resposta) |
| RNF05 | O sistema deve se integrar a outros dispositivos e plataformas. | externo: interoperabilidade |
| RNF06 | O sistema deve ser entregue com tutoriais em vídeo e manuais de usuário. | organizacional: entrega |

**Requisitos normativos**

| ID | Requisito |
|---|---|
| N01 | O sistema deve seguir as regulamentações locais e nacionais de agricultura. |
| N02 | O sistema deve seguir as regulamentações de comércio eletrônico. |
| N03 | O sistema deve seguir as regulamentações de privacidade de dados. |

- Um mesmo parágrafo pode gerar requisitos de tipos diferentes. Em "Irrigação Inteligente", controlar a irrigação é RF (RF04) e "sem desperdício" é RNF (RNF03).
- O canal de suporte foi tratado como RF porque é algo que o sistema oferece ao usuário. Também daria para defini-lo como requisito organizacional, se for um serviço prestado pela empresa e não uma função do software.
- RNF03 e RNF04 ainda não são mensuráveis. Numa especificação real, precisariam de um critério (por exemplo, o tempo máximo até o alerta).

</details>

### 2. Clínica Medisafe

> A Dra. Maria quer um sistema para a clínica: prontuário eletrônico com o histórico completo (exames, diagnósticos, prescrições, visitas), fácil de recuperar e muito seguro; marcação, reagendamento e cancelamento de consultas pela internet, com lembrete automático por e-mail ou SMS um dia antes; cada paciente só pode reagendar online uma vez, e depois disso só por telefone; glossário interativo de termos médicos; descontos automáticos para idosos e estudantes no faturamento, por política interna; interface moderna, simples e intuitiva; traduções em pelo menos três idiomas; e conformidade total com as regulamentações locais e internacionais de privacidade e segurança de dados médicos.
>
> Identifique e classifique os requisitos em funcionais, não funcionais, normativos e regras de negócio.

<details>
<summary>Ver solução</summary>

**Requisitos funcionais**

| ID | Requisito |
|---|---|
| RF01 | O sistema deve registrar o prontuário eletrônico do paciente, com exames, diagnósticos, prescrições e visitas anteriores. |
| RF02 | O sistema deve permitir consultar o histórico médico do paciente. |
| RF03 | O sistema deve permitir que o paciente marque consultas pela internet. |
| RF04 | O sistema deve permitir que o paciente reagende consultas pela internet. |
| RF05 | O sistema deve permitir que o paciente cancele consultas pela internet. |
| RF06 | O sistema deve enviar lembretes automáticos por e-mail ou SMS um dia antes da consulta. |
| RF07 | O sistema deve oferecer um glossário de termos médicos com busca. |
| RF08 | O sistema deve identificar pacientes idosos e estudantes e aplicar o desconto no faturamento. |

**Requisitos não funcionais**

| ID | Requisito | Categoria |
|---|---|---|
| RNF01 | As informações do prontuário devem ser facilmente recuperáveis. | produto: usabilidade/eficiência |
| RNF02 | Os dados dos pacientes devem ser protegidos contra acesso indevido. | produto: segurança |
| RNF03 | A interface deve ser moderna, simples e intuitiva para a equipe e para os pacientes. | produto: usabilidade |
| RNF04 | O sistema deve estar disponível em pelo menos três idiomas. | produto: usabilidade |

**Requisitos normativos**

| ID | Requisito |
|---|---|
| N01 | O sistema deve cumprir as regulamentações locais e internacionais de privacidade e segurança de dados médicos, garantindo integridade e confidencialidade. |

**Regras de negócio**

| ID | Regra |
|---|---|
| RN01 | Cada paciente pode reagendar uma consulta pela internet só uma vez. Um novo reagendamento deve ser feito por telefone. |
| RN02 | Idosos e estudantes têm direito a desconto (política interna da clínica). |

- A diferença entre RF08 e RN02: a **regra** é a política ("idosos e estudantes têm desconto"); o **requisito** é o sistema aplicar essa regra automaticamente.
- RN01 muda a lógica do RF04: o reagendamento online precisa verificar se o paciente já reagendou antes. É o que a aula 09 diz das regras de negócio: elas influenciam a lógica de execução dos casos de uso.
- O texto não diz quais são os três idiomas nem o valor dos descontos. Isso teria que ser levantado com a Dra. Maria.

</details>

### 3. Sistema de biblioteca

> Crie um documento com os requisitos funcionais e não funcionais de um sistema informatizado de biblioteca. Liste pelo menos um requisito não funcional para cada propriedade: velocidade, tamanho, facilidade de uso, confiabilidade, robustez, portabilidade e segurança.

<details>
<summary>Ver solução</summary>

**Requisitos funcionais**

| ID | Requisito |
|---|---|
| RF001 | O sistema deve permitir cadastrar livros com título, autor, editora, ano, ISBN e número de exemplares. |
| RF002 | O sistema deve permitir cadastrar os usuários da biblioteca. |
| RF003 | O sistema deve permitir pesquisar o acervo por título, autor ou assunto. |
| RF004 | O sistema deve permitir registrar o empréstimo de um exemplar para um usuário. |
| RF005 | O sistema deve permitir registrar a devolução de um exemplar. |
| RF006 | O sistema deve calcular a multa por atraso na devolução. |
| RF007 | O sistema deve permitir renovar um empréstimo. |
| RF008 | O sistema deve permitir reservar um livro que está emprestado. |
| RF009 | O sistema deve emitir o relatório de empréstimos em atraso. |

**Requisitos não funcionais**

| ID | Propriedade | Requisito |
|---|---|---|
| RNF001 | Velocidade | A pesquisa no acervo deve retornar o resultado em no máximo 2 segundos. |
| RNF002 | Tamanho | O banco de dados deve suportar um acervo de pelo menos 100 mil exemplares. |
| RNF003 | Facilidade de uso | Um bibliotecário deve conseguir registrar empréstimos e devoluções depois de 2 horas de treinamento. |
| RNF004 | Confiabilidade | O sistema deve ficar disponível durante pelo menos 99% do horário de funcionamento da biblioteca. |
| RNF005 | Robustez | Depois de uma falha, o sistema deve voltar a funcionar em até 5 minutos, sem perder os empréstimos já registrados. |
| RNF006 | Portabilidade | O sistema deve funcionar nos navegadores Chrome, Firefox e Edge. |
| RNF007 | Segurança | Só bibliotecários autenticados podem registrar empréstimos e devoluções. |

- Todo RNF tem um número ou uma condição que dá para testar: segundos, exemplares, horas de treinamento, porcentagem, minutos, navegadores, perfil de acesso.
- Os valores são exemplos. Num projeto real, eles saem do levantamento com os stakeholders.

</details>

### 4. Documento de requisitos livre

> Imagine um software a ser desenvolvido e crie um documento com os seus requisitos.

<details>
<summary>Ver solução</summary>

Não tem uma resposta única. Um bom ponto de partida é a estrutura do [modelo de documento do professor](https://github.com/Herysson/Engenharia-de-Software/blob/main/Exerc%C3%ADcios/Doc.%20Analise%20de%20Requisito%20de%20Software.docx):

| Seção | O que escrever |
|---|---|
| Histórico de revisões | data, versão, descrição da alteração e autor |
| Identificação dos envolvidos | papel, nome e e-mail do analista de requisitos, do Product Owner, dos principais stakeholders e do patrocinador |
| Problema de negócio | o problema e o motivo da necessidade, nas palavras do cliente, **sem** propor soluções ou funcionalidades |
| Requisitos de sistema | requisitos numerados (R1, R2...), cada um com sub-requisitos (R1.1, R1.2...) e uma descrição |

Exemplo do próprio modelo: o problema de negócio é o alto número de devoluções no e-commerce; o requisito R1 é "possibilitar autorização de devolução em lote", detalhado em R1.1 (recurso de seleção múltipla) e R1.2 (botão que autoriza os pedidos selecionados, verificando se o produto já foi enviado).

Para conferir o seu documento:
- cada RF começa com um verbo e descreve uma única função
- cada RNF tem um critério mensurável
- o problema de negócio não fala de telas nem de botões

</details>
