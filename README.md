# Dashboard de Vendas

Este projeto é um **Dashboard de Vendas Interativo**. O objetivo principal é transformar dados brutos de vendas diárias em informações visuais claras, profissionais e acionáveis, permitindo uma análise eficaz do desempenho de vendas e facilitando a tomada de decisões baseada em dados.

## Funcionalidades

* **Controle de Vendas Centralizado:** Uma base de dados profissional e estruturada para registrar todas as transações.

* **Cálculo Automático de Descontos:** Lógica implementada para aplicar descontos em porcentagem (%) e calcular automaticamente o valor real da venda (receita líquida).

* **Validação de Dados:** Menus suspensos (dropdowns) integrados para padronizar as entradas de pagamento, status de desconto e tipo de entrega, evitando erros de digitação.

* **Visualização Dinâmica:** Um painel (dashboard) com gráficos e indicadores-chave de desempenho (KPIs) atualizados em tempo real.

* **Filtros Interativos (Slicers):** Segmentadores de dados que permitem filtrar todo o dashboard com um clique.

## Estrutura do Projeto

O projeto é dividido em duas abas principais na planilha:

### 1. Base de Dados

A aba principal de inserção de dados. Foi projetada para ser limpa e escalável, contendo as seguintes colunas:

* **ID da Venda:** Identificador único da transação.

* **Data da Venda & Mês:** Registro temporal da venda.

* **Nome do Cliente & Telefone:** Dados de contato e CRM.

* **Produto:** Item comercializado.

* **Quantidade & Valor Unitário:** Dados base da compra.

* **Valor Total (Bruto):** Cálculo automático (`Quantidade * Valor Unitário`).

* **Teve Desconto?:** Validação de dados (`Sim` ou `Não`).

* **% de Desconto:** Porcentagem de desconto aplicada (ex: 5%, 10%).

* **Valor Total com Desconto:** O **valor real** da venda. Se houver desconto, aplica a porcentagem sobre o valor bruto. Se não, repete o valor bruto.

* **Método de Pagamento:** Validação de dados (`Dinheiro`, `Cartão`, `Pix`).

* **Retirada ou Envio:** Validação de dados indicando o tipo de logística da venda.

*Nota: O projeto conta com um dataset de testes com mais de 100 linhas preenchidas para demonstração das métricas.*

### 2. Dashboard

A aba visual onde os dados são consolidados. Inclui:

* **KPIs (Indicadores de Desempenho):**

  * Faturamento Total (Baseado no *Valor Total com Desconto*).

  * Número Total de Vendas realizadas.

* **Gráficos:**

  * Vendas por Produto (Identificação de Best-sellers).

  * Faturamento por Método de Pagamento.

* **Filtros Interativos (Slicers):**

  * **Mês:** Para análises sazonais.

  * **Tipo de Venda (Retirada/Envio):** Para entender a logística mais utilizada.

  * **Produto:** Para isolar o desempenho de itens específicos.

## Tecnologias e Recursos Utilizados

* **Google Sheets (Planilhas do Google)**

* **Fórmulas Condicionais (SE / IF)**

* **Validação de Dados (Data Validation)**

* **Tabelas Dinâmicas (Pivot Tables)**

* **Gráficos Nativos e Segmentadores de Dados (Slicers)**

## Como Usar

1. **Acessar a Planilha:** Faça uma cópia da planilha original.

2. **Inserir Dados:** Navegue até a aba `Base de Dados` e comece a inserir as informações das suas vendas diárias nas próximas linhas vazias. As colunas com fórmulas (Valor Total, Valor Total com Desconto) se calcularão sozinhas.

3. **Analisar Resultados:** Vá para a aba `Dashboard`. Os gráficos serão atualizados automaticamente.

4. **Filtrar Informações:** Use os botões (Slicers) no topo do Dashboard para filtrar a visualização de acordo com a sua necessidade (ex: ver apenas as vendas de "Janeiro" pagas no "Pix").
