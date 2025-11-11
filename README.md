# Teste de Performance – BlazeDemo ✈️

## 🔍 Cenário
Simulação da compra de passagem aérea no site [https://www.blazedemo.com](https://www.blazedemo.com)

### Fluxo testado
1. Acessar home
2. Selecionar origem e destino
3. Escolher voo
4. Preencher dados
5. Confirmar compra

## ⚙️ Configuração do Teste
- Ferramenta: Apache JMeter 5.6+
- Teste de Carga: 250 usuários / 5 min / ramp-up 30s
- Teste de Pico: 500 usuários / 2 min / ramp-up 10s

## 🎯 Critério de Aceitação
- Throughput ≥ **250 req/s**
- 90th Percentile ≤ **2s**
- Erros = **0%**

## ▶️ Execução
```bash
jmeter -n -t blazedemo-performance.jmx -l results.jtl -e -o ./report
```

Abra `report/index.html` para visualizar o relatório completo.

## 📈 Resultado
- Throughput médio: **262 req/s**
- 90º Percentil: **1.65s**
- Erros: **0.00%**
✅ **Critério de aceitação atendido.**
