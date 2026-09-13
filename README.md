# Relatório de Aging de Registros ANVISA

## Contexto

A pedido do gerente da área de Controladoria (atuando como Cientista de Dados), desenvolvi, ainda na função de Assistente de Qualidade e Assuntos Regulatórios, um relatório de acompanhamento de vencimento de registros de produtos junto à ANVISA, cobrindo um total de **373 registros**.

A demanda partiu de uma área de dados da própria empresa, que buscava aplicar uma lógica de classificação de risco já validada (a mesma metodologia usada no controle de itens próximos ao vencimento) a um problema diferente: acompanhamento de validade regulatória, não de produto físico em estoque.

## Abordagem

1. **Extração**: coleta dos dados de vencimento de registro a partir do ERP interno da empresa.
2. **Classificação por faixa de aging**:

| De (dias) | Até (dias) | Classificação |
|---|---|---|
| — | — | 00 - Registro Isento / Vigente |
| 0 | 180 | 01 - Registro vencido / a vencer em 0–180 dias (verificar situação) |
| 181 | 365 | 02 - Registro a vencer (verificar situação) |
| 366 | 10.000.000 | 03 - Registro a vencer (realizar acompanhamento) |

3. **Entrega**: relatório consolidado disponibilizado à Controladoria para acompanhamento da situação regulatória do portfólio.

## Ferramentas

- Microsoft Excel (fórmulas avançadas, classificação por faixa)
- Extração de dados de sistema ERP interno

## Resultado

Relatório entregue à área de Controladoria, dando visibilidade sobre a situação de vencimento de registro em um portfólio de 373 itens, informação que antes não existia de forma consolidada e classificada por risco.

## Sobre os dados neste repositório

Nenhum número de registro ANVISA real, nome de produto ou dado da empresa está incluído. Este repositório documenta a metodologia aplicada, não uma cópia do relatório original.
