# Creator Data Marketing System: Sistema de Inteligência de Dados e Leitura Preditiva

Projeto desenvolvido no **Desafio Criativo DIO — Sistema de Inteligência de Dados e Leitura Preditiva**. O objetivo é sair do monitoramento passivo de métricas de vaidade e construir um painel preditivo que antecipa quedas de faturamento e identifica momentos de aceleração de caixa.

> **Nota:** o projeto "Contas Claras", o produto, o ticket médio e todos os números deste repositório são **simulados (fictícios)** e assumidos como tal, para efeitos do desafio.

📄 **Documento completo:** [(https://docs.google.com/document/d/1bNT21ToakzqDJ941LQEy2yANM8H5US_LknV2nVMbajM/edit?usp=sharing)]

---

## 🎯 Sobre o projeto

O sistema foi construído em 3 etapas sequenciais, com apoio de IA (Claude) num único chat para acumular o contexto:

1. **Definir a Métrica Mãe**: um objetivo SMART de 90 dias e a única métrica que valida o crescimento real de caixa.
2. **Estruturar as métricas da jornada**: Atenção, Intenção e Ação, com referência saudável e piso de alerta para cada taxa.
3. **Mapear sinais preditivos**: cenários de queda, estabilidade e escala, indicador antecedente e ritual semanal de 10 minutos.

## 🧩 Contexto simulado

| Item | Valor |
| --- | --- |
| Projeto | Contas Claras (consultoria e conteúdo sobre contabilidade e dados) |
| Produto | Mentoria em grupo de 4 semanas, ticket médio de €197 |
| Canais | LinkedIn (aquisição), newsletter (nutrição), página de vendas (conversão) |
| Objetivo de 90 dias | €11.820 de receita bruta (60 vendas) com margem de contribuição ≥ 70% (pelo menos €8.274 líquidos) |

## 1. Métrica Mãe

**Receita líquida semanal proveniente do LinkedIn** (vendas atribuídas × ticket, menos taxas e custos diretos).

**Teste de invalidação de vaidade (seguidores):** os seguidores podem subir 50% e o caixa ficar a zero, porque (1) a audiência pode não ser o público que compra e (2) seguir não é um ato de compra nem de intenção. Seguidores medem atenção acumulada; a Métrica Mãe mede dinheiro que entrou.

## 2. Métricas essenciais da jornada

| Etapa | Métrica semanal |
| --- | --- |
| Atenção (topo) | Impressões das publicações no LinkedIn |
| Intenção (meio) | Leads qualificados (inscrições na newsletter + pedidos de contacto) |
| Ação (fundo) | Vendas da mentoria atribuídas ao LinkedIn |

**Fórmulas**

- `Taxa 1 = leads ÷ impressões`
- `Taxa 2 = vendas ÷ leads`
- `Taxa global = vendas ÷ impressões`

**Réguas calibradas**

| Taxa | Referência saudável | Piso de alerta |
| --- | --- | --- |
| Taxa 1: Atenção → Intenção | 1,0% | 0,6% |
| Taxa 2: Intenção → Ação | 5,0% | 3,0% |
| Taxa global: Atenção → Ação | 0,05% | 0,018% |

Com as taxas saudáveis, cerca de 9.200 impressões por semana bastam para cumprir as 60 vendas em 90 dias.

## 3. Mapa preditivo de sinais

| Cenário | Taxa 1 | Taxa 2 | Decisão |
| --- | --- | --- | --- |
| Pré-queda, amarelo | 0,6% a menos de 0,9% ou | 3,0% a menos de 4,5% (2 semanas seguidas) | Corrigir uma variável por semana |
| Pré-queda, vermelho | abaixo de 0,6% ou | abaixo de 3,0% | Parar experiências e acionar o diagnóstico |
| Estabilidade | 0,9% a menos de 1,3% | 4,5% a menos de 6,0% | Manter e monitorizar |
| Escala | 1,3% ou mais e | 6,0% ou mais (2 semanas seguidas) | Aumentar publicação e investimento cerca de 30%, com margem ≥ 70% |

**Indicador antecedente primário:** a **Taxa 1**. Os leads captados esta semana viram vendas 1 a 2 semanas depois, por isso a Taxa 1 cai antes de a receita sentir o problema.

## ⏱️ Ritual semanal de 10 minutos

Fazer à segunda-feira, com os dados da semana anterior.

1. **Minutos 0 a 3, alimentação de dados:** copiar impressões, leads, vendas e receita líquida, e calcular as três taxas.
2. **Minutos 3 a 7, leitura hierárquica:** comparar a receita líquida com a meta média (cerca de €636 por semana) e classificar a Taxa 1 e a Taxa 2 no mapa.
3. **Minutos 7 a 10, acionamento da IA (só em caso de alerta):**

> Atua como meu analista de growth. A minha Métrica Mãe é a receita líquida semanal do LinkedIn (meta média de cerca de €636 líquidos por semana). Esta semana: impressões = [X], leads = [Y], vendas = [Z]. Taxa 1 = [%] (referência 1,0%, piso 0,6%) e Taxa 2 = [%] (referência 5,0%, piso 3,0%). O sinal é [amarelo/vermelho]. Diz-me: (1) em que etapa está a perda, (2) as 3 causas mais prováveis, e (3) uma única correção para testar esta semana, com o resultado esperado.

## 📂 Estrutura do repositório

```
creator-data-marketing-system/
├── README.md
└── docs/
    ├── Manual-Inteligencia-Dados-Leitura-Preditiva.pdf
    └── Manual-Inteligencia-Dados-Leitura-Preditiva.docx
```

## 🛠️ Ferramentas utilizadas

- Claude (IA como parceira de calibração das réguas e da matriz preditiva)
- Claude Docs / Google Docs (documento de entrega)
- GitHub (documentação e portefólio)

## 💡 Principais aprendizados

- Métricas de vaidade medem atenção; só a Métrica Mãe valida o crescimento real de caixa.
- Uma jornada em 3 etapas (Atenção, Intenção, Ação) mostra em que ponto está a perda.
- Taxas com referência e piso transformam o monitoramento em decisões automáticas.
- A taxa que pisca primeiro (indicador antecedente) permite agir antes de o faturamento cair.

## 👤 Autora

**Alda Benta**, contabilista a desenvolver competências em análise de dados.

---

*Projeto educativo. Todos os dados são simulados.*
