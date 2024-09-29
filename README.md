## Programa para Calcular Percentual de Faturamento por Estado

Este programa em Python calcula o percentual de representação do faturamento mensal de uma distribuidora para cada estado.

### Funcionamento do Programa

1. **Definição dos Valores de Faturamento**: Os valores de faturamento são armazenados em um dicionário, onde cada chave representa um estado e o valor associado é o faturamento correspondente.
2. **Cálculo do Faturamento Total**: O faturamento total é calculado somando todos os valores do dicionário.
3. **Cálculo dos Percentuais**: Para cada estado, o percentual de representação é calculado dividindo o valor do faturamento pelo faturamento total e multiplicando por 100.
4. **Exibição dos Resultados**: Os percentuais são exibidos formatados com duas casas decimais.

### Código

```python
# Valores de faturamento por estado
faturamento = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

# Calcula o faturamento total
faturamento_total = sum(faturamento.values())

# Calcula o percentual de representação de cada estado
percentuais = {estado: (valor / faturamento_total) * 100 for estado, valor in faturamento.items()}

# Exibe os percentuais formatados
for estado, percentual in percentuais.items():
    print(f"{estado}: {percentual:.2f}%")

