# 📊 Análise RFM de Clientes

Este repositório apresenta uma **análise de segmentação RFM (Recência, Frequência, Monetização)**, com o objetivo de classificar clientes com base em seu comportamento de compra e ajudar na definição de estratégias de marketing personalizadas.

---

## 🧠 O que é RFM?

A segmentação RFM permite classificar clientes com base em três fatores:

- **Recência (R):** Há quanto tempo o cliente realizou a última compra.
- **Frequência (F):** Quantas vezes o cliente comprou em um período de tempo.
- **Monetização (M):** Quanto dinheiro o cliente gastou.

---

## 📂 Estrutura do Projeto

```
📁 rfm-segmentacao
│
├── 📊 dados/
│   └── vendas.csv
│
│
├── ✅ teste_case/
│   └── segmentacao_rfm_teste.xlsx
│
└── 📄 README.md
```

---

## ⚙️ Como foi feito

### 1. **Tratamento e Unificação dos Dados**
- Utilizei fórmulas como `ÍNDICE` e `CORRESP` para cruzamento de dados entre planilhas.
- A função `ÚNICA` foi aplicada para extrair todos os **Customer IDs** únicos.

### 2. **Cálculo dos Indicadores RFM**
- **Recência**: Usado `MÁXIMO`, `SE`, `FILTRO` e `CONT.VALORES` para identificar o tempo desde a última compra.
- **Frequência**: Contagem de registros de compras por cliente usando `FILTRO` + `CONT.VALORES`.
- **Monetização**: Uso do `SOMASE` para somar os valores monetários gastos por cliente.

### 3. **Pontuação RFM**
- Atribuição de **notas de 1 a 5** para cada métrica com base em percentis (`PERCENTIL`, `SE`).
- Foi calculada a média das notas (NF) e arredondada (`ARRED`) para classificar os clientes.

### 4. **Segmentação**
- Nome dos segmentos atribuídos com `ÍNDICE` e `CORRESP`, com base na pontuação combinada.

---

## 🧪 Teste de Caso

O teste de caso incluído neste projeto foi baseado no seguinte cenário:

**Segmentação de Clientes:**

| Segmento Clientes    | Grupo             | % de Clientes |
|----------------------|-------------------|----------------|
| Campeões             | Campeões          | 4%             |
| Fiéis                | Fiéis             | 27%            |
| Fiéis Potencial      | Fiéis Potencial   | 40%            |
| Hibernando           | Hibernando        | 2%             |
| Não Perder           | Não Perder        | 1%             |
| Novos Clientes       | Novos Clientes    | 2%             |
| Perdidos             | Perdidos          | 10%            |
| Precisam Atenção     | Precisam Atenção  | 2%             |
| Promissores          | Promissores       | 1%             |
| Quase Dormentes      | Quase Dormentes   | 4%             |
| Risco                | Risco             | 8%             |

---

## 💡 Insights e Estratégias

| Segmento           | Estratégia Recomendada |
|--------------------|-------------------------|
| **Campeões**        | Programas de fidelidade VIP, ofertas exclusivas. |
| **Fiéis**           | Oferecer pacotes de vantagens e upgrades. |
| **Fiéis Potencial** | Investir em relacionamento, comunicação ativa. |
| **Novos Clientes**  | Criar boas primeiras experiências, onboarding. |
| **Promissores**     | Estimular novas compras com cupons e descontos. |
| **Precisam Atenção**| Reengajar com promoções personalizadas. |
| **Quase Dormentes** | Enviar comunicações de incentivo e recuperação. |
| **Hibernando**      | Reativar com ofertas agressivas. |
| **Risco**           | Analisar causas e reverter abandono com atenção. |
| **Não Perder**      | Atendimento personalizado e prioridade. |
| **Perdidos**        | Evitar investir em excesso, mas pode testar campanhas de recuperação. |

---

## 🚀 Como Executar

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/rfm-segmentacao.git
```


---

## 📌 Requisitos

- Microsoft Excel ou Google Sheets

---

## 📬 Contato

Se tiver dúvidas ou quiser colaborar, fique à vontade para abrir uma issue ou me chamar!
