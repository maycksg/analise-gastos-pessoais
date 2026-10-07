# Análise de Gastos Pessoais (Excel)

Projeto de análise de dados feito em Excel: limpeza, análise e conclusões sobre 6 meses de gastos pessoais.

## Objetivo
Entender para onde vai o dinheiro, identificar onde há espaço para economizar e propor metas realistas.

## Dados
- `gastos.csv`: 105 registros de jan/2025 a jun/2025 (data, categoria, descrição e valor).
- **Dados fictícios**, gerados para estudo, com inconsistências inseridas de propósito (categorias escritas de formas diferentes, duplicatas, valor em branco e linhas com categoria incompatível com a descrição) para praticar a limpeza.
- Premissa: renda mensal de R$ 4.000.

## Ferramentas
Excel: Tabelas, Tabelas Dinâmicas, `SOMASES`, `SOMARPRODUTO`, `TEXTO`, `PROCX` e gráficos.

## Estrutura da planilha (`gastos.xlsx`)
| Aba | Conteúdo |
|---|---|
| Dados Brutos | Dados originais, sem alterações |
| Dados Tratados | Dados limpos, em formato de Tabela |
| Premissas e Logs | Renda, metas e registro de tudo o que foi alterado ou removido |
| Análises | Tabelas dinâmicas e gráficos |
| Conclusões | Indicadores e frases geradas por fórmula (atualizam sozinhas) |

## Tratamento dos dados
- **Padronização** de categorias e descrições.
- **2 duplicatas removidas** (R$ 217,12).
- **1 linha removida** por não ter valor.
- **2 linhas reclassificadas**: a categoria era incompatível com a descrição, e a descrição prevaleceu (impacto no total: zero).
- **1 descrição em branco preenchida** por inferência da categoria (Transporte).
- Tudo está documentado na aba *Premissas e Logs*.

## Principais resultados
- **Gasto total:** R$ 17.148,43 em 6 meses, com média de R$ 2.858,07 por mês (mínimo em fevereiro, máximo em abril).
- **Moradia** representa 42,0% do gasto. Somada a Contas, os **custos fixos chegam a 51,2%**.
- **Poupança média:** 28,5% da renda, com pior mês em abril (25,2%) e melhor em fevereiro (31,5%).
- **Lazer e Transporte** são as categorias mais voláteis: oscilaram R$ 209,48 e R$ 229,07, respectivamente, entre o mês mais baixo e o mais alto.

## Metas propostas
| Meta | Resultado |
|---|---|
| Lazer até R$ 350/mês | Estourada em 5 dos 6 meses |
| Transporte até R$ 200/mês | Estourada em 4 dos 6 meses |
| **Economia se cumpridas** | **R$ 856,63 no período (≈ R$ 143/mês)** |
| **Poupança média** | **de 28,5% para 32,1% (+3,6 p.p.)** |

São metas desafiadoras, mas já foram atingidas em alguns meses (Lazer em 1 dos 6 e Transporte em 2 dos 6).

## Limitações
- Apenas 6 meses de dados, o que não permite identificar sazonalidade.
- Dados fictícios e renda fixa.
- A reclassificação das 2 linhas assumiu que a descrição estava correta.

## Próximos passos
- Refazer a análise em **SQL** (SQLite) e em **Python/Pandas**.
- Criar um **dashboard no Power BI** com filtros por mês e categoria.
- Adicionar uma previsão simples do gasto do próximo mês.

## Estrutura do repositório
```
analise-gastos-pessoais/
├── README.md
├── gastos.csv
├── gastos.xlsx
└── imagens/
    └── graficos.png
```
