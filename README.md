# 🏦 Análise de Crédito com SQL e Storytelling

## Descrição do Projeto
Este projeto consiste em uma **Análise Exploratória e Diagnóstica Completa** de uma base de dados de clientes de cartão de crédito. Utilizando **SQL (Structured Query Language)**, o objetivo foi extrair insights profundos sobre o perfil demográfico, financeiro e comportamental dos clientes, culminando em um **Plano de Ação Estratégico** focado em Retenção e Rentabilidade.

O notebook conduz a análise através de consultas SQL, focando em:
* **Segmentação:** Distribuição de clientes por gênero, renda e escolaridade.
* **Maturidade da Base:** Resumo estatístico da idade dos clientes.
* **Comportamento de Crédito:** Análise do tipo de cartão, limite de crédito, volume de transações e meses de inatividade (risco de *churn*).

---

## ⚠️ Destaque de Infraestrutura (AWS S3)
Este projeto foi concebido e testado em um ambiente *cloud-ready*, com o código preparado para integração com o **Amazon Simple Storage Service (AWS S3)**.

Em um pipeline de produção, o AWS S3 serviria como a principal camada de armazenamento, garantindo:
1.  **Ingestão de Dados:** O *dataset* de crédito seria lido diretamente de um *bucket* S3.
2.  **Persistência:** Os resultados finais das análises SQL (tabelas de *insights*, segmentações) seriam exportados de volta para o S3, facilitando o consumo por ferramentas de *Business Intelligence (BI)* e *dashboards*.

A utilização do ambiente Colab (ou Jupyter) permite a prototipagem da análise, mas a estrutura do código e as bibliotecas (como o potencial uso de `boto3` para interação com o AWS) garantem a portabilidade para um ambiente de dados robusto.

---

## Estrutura da Análise e Principais Insights

| Análise Executada | Principal Insight Extraído | Ação Estratégica Proposta |
| :--- | :--- | :--- |
| **Demografia** (Gênero) | A base é majoritariamente **Masculina (61%)**. | Focar a comunicação e ofertas de produto para o público masculino. |
| **Crédito** (Tipo de Cartão) | Quase **95%** dos clientes possuem o **Cartão Blue** (de entrada). | Foco em campanhas de **Upgrade Proativo** (Silver/Gold). |
| **Comportamento** (Inatividade) | **36.9%** dos clientes registram **3 meses de inatividade**. | **Retenção:** Lançar campanhas de reengajamento a partir do 2º mês de inatividade. |
| **Crédito** (Limite) | **42%** dos clientes possuem limite inferior a **\$5.000**. | Reforça a estratégia de *upgrade*, focando em aumentar o limite para clientes de bom perfil. |

---

## 🔍 Retrato do Cliente Típico (Via SQL)
* **Idade Média:** 46 anos.
* **Renda:** Abaixo de \$40K (27.34%).
* **Escolaridade:** Mestrado, Ensino Médio ou "Não-Educado" são os maiores grupos (cerca de 67% combinados).
* **Comportamento:** Bom pagador (baixo uso de rotativo) e moderadamente ativo (média de 41 transações/ano).

---

## Tecnologias
* **Python:** Linguagem de orquestração e ambiente Jupyter/Colab.
* **SQL (SQLite/Pandas):** Linguagem utilizada para todas as consultas de transformação e análise de dados.
* **Pandas:** Usado para ler os dados e executar as consultas SQL no ambiente Python.
* **AWS S3 (Conceptual):** Plataforma *cloud* sugerida e testada para armazenamento de dados escalável.

---

## Como Executar
O projeto é contido em um único *notebook* Jupyter/Colab.

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/willcosta29/Projeto-analise-de-credito-em-sql.git](https://github.com/willcosta29/Projeto-analise-de-credito-em-sql.git)
    ```
2.  **Abra o Notebook:** Abra `Projeto_análise_.ipynb` no Google Colab ou em um ambiente Jupyter local.
3.  **Execução:**
    * *Setup:* Verifique se as bibliotecas básicas (`pandas`, `sqlite3` ou similar) estão instaladas.
    * *Passos:* Execute as células sequencialmente. As consultas SQL estão embutidas nas células de código, e os *outputs* com os *insights* (tabelas e gráficos) são apresentados em seguida.

---

## ✒️ Autor
William Costa - GitHub: [willcosta29](https://github.com/willcosta29)
Notebook: `Projeto_análise_.ipynb`
