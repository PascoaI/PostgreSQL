## Explicações das Queries SQL

### 1. Consulta de Vendedores
Seleciona vendedores ativos, ordenados pelo nome. A cláusula `ORDER BY` organiza os resultados em ordem alfabética.

### 2. Funcionários com Salário Acima da Média
A subquery `AVG(salario)` calcula a média salarial. O `WHERE` filtra os funcionários que têm salário superior a essa média.

### 3. Resumo por Cliente
Calcula o total de pedidos transmitidos por cliente. O `COALESCE(SUM(valor_total), 0)` garante que clientes sem pedidos retornem `0`, evitando valores `NULL`. O `ORDER BY` ordena pelo total de forma decrescente.

### 4. Situação por Pedido
Define a situação do pedido com base nas datas preenchidas. Utiliza `CASE WHEN` para classificar os pedidos como `CANCELADO`, `FATURADO` ou `PENDENTE`, conforme a presença de datas.

### 5. Produtos Mais Vendidos
Soma a quantidade e o valor total vendido de cada produto. `COUNT(DISTINCT id_cliente)` conta os clientes únicos, e `COUNT(DISTINCT id_pedido)` os pedidos distintos. O `ORDER BY` prioriza produtos com mais vendas e, em caso de empate, usa o valor total vendido.

