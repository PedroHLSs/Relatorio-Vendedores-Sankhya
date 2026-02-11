# Relatório de Vendedores Sintético (com Subrelatório)

Este projeto contém o layout e a estrutura do **Relatório Sintético de Vendedores** com seu respectivo **subrelatório**, desenvolvido no iReport/JasperReports para utilização no Sankhya.

O objetivo é apresentar um resumo consolidado por vendedor e, ao mesmo tempo, permitir o detalhamento das informações por meio do subrelatório, facilitando a análise gerencial e fiscal.

---

## 📊 Estrutura dos Relatórios

- **Relatório Principal (Sintético de Vendedores)**
  - Apresenta os dados consolidados por vendedor  
  - Totalizadores por período, vendedor ou outro critério definido no SQL  
  - Exibe indicadores principais (ex: valor total, quantidade de vendas, etc.)

- **Subrelatório (Detalhamento por Vendedor)**
  - Exibe os lançamentos/detalhes vinculados a cada vendedor  
  - Vinculado ao relatório principal por parâmetro (ex: `CODVEND`, `CODUSU`, etc.)  
  - Permite análise analítica sem poluir o relatório sintético

---

## 🛠️ Tecnologias Utilizadas

- iReport / JasperReports  
- Banco de dados Sankhya (Oracle / SQL Server, conforme ambiente)  
- SQL para consulta dos dados  
- Parâmetros dinâmicos no relatório  

---

## ⚙️ Parâmetros Utilizados

Exemplos de parâmetros (ajuste conforme seu layout real):

- `DT_INI` – Data inicial do período  
- `DT_FIM` – Data final do período  
- `CODVEND` (ou similar) – Código do vendedor  
- `EMPRESA` – Filtro por empresa/filial  

---

## 🔗 Vinculação do Subrelatório

O subrelatório é chamado a partir do relatório principal, recebendo parâmetros como:

- Código do vendedor  
- Período selecionado  
- Demais filtros aplicados no relatório sintético  

Essa vinculação garante que cada vendedor exibido no relatório principal traga apenas seus respectivos registros no subrelatório.

---

## ▶️ Como Utilizar no Sankhya

1. Importar os arquivos `.jrxml` no iReport/Sankhya  
2. Ajustar o SQL conforme ambiente (Oracle / SQL Server)  
3. Validar parâmetros no relatório principal e no subrelatório  
4. Publicar o relatório no Sankhya  
5. Executar com filtros de data e vendedor conforme necessidade  

---

## 🧪 Observações Técnicas

- Verificar caminhos do subrelatório (`SUBREPORT_DIR`)  
- Garantir que os parâmetros do subrelatório tenham o mesmo nome do relatório principal  
- Testar o SQL diretamente no banco antes de publicar  
- Validar `GROUP BY` e totalizadores para evitar erros de agregação  

---

## 📌 Objetivo do Relatório

Ajudar na análise gerencial e fiscal do desempenho dos vendedores, permitindo:

- Visão rápida e resumida (relatório sintético)  
- Acesso ao detalhe quando necessário (subrelatório)  
- Apoio à tomada de decisão e conferências  

---

## 👤 Autor

Desenvolvido por: **Pedro Henrique Lopes Silva**  
