# Teste de Performance – BlazeDemo

## Cenário
Simulação da compra de passagem aérea no site [https://www.blazedemo.com](https://www.blazedemo.com)

### Fluxo testado
CT01. Acessar home

CT02. Selecionar origem e destino

CT03. Escolher voo

CT04. Preencher dados

CT05. Confirmar compra (Fluxo Principal)

## Configuração do Teste
- Ferramenta: Apache JMeter 5.6+
- Teste de Carga: 250 usuários / 5 min / ramp-up 30s
- Teste de Pico: 500 usuários / 2 min / ramp-up 10s

## Critério de Aceitação
- Throughput ≥ **250 req/s**
- 90th Percentile ≤ **2s**
- Erros = **0%**

## Execução
```bash
jmeter -n -t blazedemo-performance.jmx -l results.jtl -e -o ./report
```

Abra `report/index.html` para visualizar o relatório completo.

## Resultado
- Throughput médio: **262 req/s**
- 90º Percentil: **1.65s**
- Erros: **0.00%**

### Autor
Desenvolvido por Mauricio Cordeiro Lyrio Monteiro
