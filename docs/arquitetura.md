# Arquitetura do Sistema

## Tecnologias Utilizadas
- **Power BI Desktop**: desenvolvimento do dashboard
- **Python**: exportação dos dados do modelo RNA para CSV/Excel
- **GitHub**: versionamento e documentação

## Modelo C4

### Nível 1 — Context
O analista acessa o dashboard Power BI, que consome arquivos
CSV gerados pelo pipeline de treinamento e avaliação do modelo
de RNA desenvolvido em Python.

### Nível 2 — Container
- **Modelo RNA (Python)**: realiza o treinamento e avaliação,
  exportando métricas para arquivos CSV
- **Arquivos CSV**: armazenam métricas de desempenho, resultados
  por imagem e histórico de treinamento
- **Dashboard Power BI**: consome os CSVs e apresenta as
  visualizações interativas

## Justificativa
A arquitetura é simples e adequada ao problema: o foco é na
análise e visualização dos resultados, não na inferência em tempo
real. O uso de CSV como camada intermediária garante portabilidade
e facilidade de atualização dos dados.
