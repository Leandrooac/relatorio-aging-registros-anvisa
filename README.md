# Relatório de Aging de Registros ANVISA

## Contexto

Ainda como Auxiliar de Controle de Qualidade, desenvolvi, a pedido da área de Controladoria, um relatório de acompanhamento de vencimento dos registros de produtos junto à ANVISA, cobrindo **373 registros**.

A ideia era aplicar a mesma lógica de classificação de risco do [controle de itens próximos ao vencimento](https://github.com/Leandrooac/controle-aging-vencimento) a outro problema: a validade regulatória do registro, e não a do produto físico em estoque.

## Abordagem

1. **Extração**: coleta dos dados de vencimento de registro a partir do ERP interno da empresa.
2. **Classificação por faixa de aging**:

| De (dias) | Até (dias) | Classificação |
|---|---|---|
| — | — | 00 - Registro isento / vigente |
| 0 | 180 | 01 - Registro vencido ou a vencer em até 180 dias (verificar situação) |
| 181 | 365 | 02 - Registro a vencer (verificar situação) |
| Acima de 365 | — | 03 - Registro a vencer (realizar acompanhamento) |

3. **Entrega**: relatório consolidado disponibilizado à Controladoria para acompanhar a situação regulatória do portfólio.

## Ferramentas

- Microsoft Excel (fórmulas avançadas, classificação por faixa)
- Extração de dados de sistema ERP interno

## Resultado

A Controladoria passou a ter visibilidade da situação de vencimento de 373 registros, informação que antes não existia de forma consolidada nem classificada por risco.

## Sobre os dados neste repositório

Nenhum número de registro ANVISA, nome de produto ou dado da empresa está incluído. Este repositório documenta a metodologia aplicada, não uma cópia do relatório original.
