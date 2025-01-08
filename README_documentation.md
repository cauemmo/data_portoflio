# Documentação do Projeto de Dados: Análise de Perfil de Pacientes com Doenças Cardíacas 
### Sumário
- [Contexto e Visão Geral](#contexto-e-visão-geral)
- [Visão Geral da Estrutura de Dados](#visão-geral-da-estrutura-de-dados)
- [Resumo Executivo](#resumo-executivo)
- [Detalhamento dos Insights](#detalhamento-dos-insights)
- [Recomendações dos Próximos Passos](#recomendações-dos-próximos-passos)
- [Análise Técnica e Exploratória dos Dados](#análise-técnica-e-exploratória-dos-dados)

# Contexto e Visão Geral
A análise foi conduzida para abordar um problema crítico enfrentado pela organização: como identificar os principais fatores de risco para doenças cardíacas em diferentes grupos populacionais e priorizar iniciativas preventivas. O aumento dos custos associados ao tratamento de doenças cardiovasculares e a alta prevalência de condições relacionadas reforçam a necessidade de uma abordagem baseada em dados para melhorar os resultados em saúde e reduzir despesas.A organização busca entender padrões comportamentais e características clínicas que contribuem para o aumento dos casos de doenças cardíacas. Fatores como idade, gênero, pressão arterial e hábitos de vida (ex.: tabagismo e atividade física) são fundamentais para criar um plano de prevenção eficiente.
### Perguntas de Negócio:
#### Risk Factors Analysis: 
- Quais são os principais fatores de risco associados às doenças cardíacas na população analisada?
#### Cholesterol Impact: 
- Existe uma relação significativa entre níveis de colesterol elevados e a presença de doenças cardíacas?
#### Vulnerable Groups: 
- Quais grupos (segmentados por idade, gênero ou comportamento) apresentam maior vulnerabilidade?
#### Lifestyle Influence:
- Como o estilo de vida (ex.: fumar, beber álcool e prática de atividade física) influencia o risco cardiovascular?
#### Campaign Targeting:
- Quais campanhas devemos nos especificar para maximizar o impacto preventivo? 
## 
## Links relevantes:
- Dashboard Interativo:
- Notebooks de Análise: 

# Visão Geral da Estrutura de Dados
A base de dados contém 70.000 registros e 13 colunas, conforme descrito abaixo:
- id: Identificador único.
- age: Idade em dias.
- gender: Gênero (1 para feminino, 2 para masculino).
- height: Altura em cm.
- weight: Peso em kg.
- ap_hi: Pressão arterial sistólica.
- ap_lo: Pressão arterial diastólica.
- cholesterol: Nível de colesterol (1: normal, 2: acima do normal, 3: muito acima do normal).
- gluc: Nível de glicose (1: normal, 2: acima do normal, 3: muito acima do normal).
- smoke: Fumante (0: não, 1: sim).
- alco: Consumo de álcool (0: não, 1: sim).
- active: Atividade física (0: não, 1: sim).
- cardio: Diagnóstico de doença cardíaca (0: não, 1: sim).
  
#### Diagrama de Entidade e Relacionamento (DER): 

![Captura de Tela (810)](https://github.com/user-attachments/assets/960eea40-4a98-4d88-b6b1-3b6bfb128494)


# Resumo Executivo
Os principais insights obtidos incluem:
#### 1.	Risk Factors Analysis: 
- Os fatores de risco mais relevantes para doenças cardíacas são IMC elevado, pressão arterial alta e obesidade. Indivíduos com IMC elevado apresentam 76% de prevalência de doenças cardíacas, indicando uma relação direta entre peso corporal e risco cardiovascular.
#### 2.	Cholesterol Impact: 
- Existe uma forte relação entre colesterol elevado e doenças cardíacas. Indivíduos com colesterol acima do normal têm uma prevalência 36% maior de doenças cardíacas em comparação àqueles com colesterol normal.
#### 3.	Vulnerable Groups: 
- Indivíduos acima de 60 anos representam 35% dos casos de doenças cardíacas, enquanto aqueles abaixo de 40 anos representam apenas 5%. Homens possuem um risco levemente maior (52%) em relação às mulheres (48%).
#### 4.	Lifestyle Influence:
- Indivíduos fisicamente inativos têm uma prevalência de doenças cardíacas 8% maior do que os ativos. Curiosamente, fumantes apresentaram uma prevalência 3% menor em relação aos não fumantes, o que pode indicar viés ou fatores subjacentes.
#### 5.	Insights Baseados no Modelo de Previsão:
- O modelo de previsão destaca que IMC, pressão arterial alta e idade são os fatores mais importantes para a identificação de riscos de doenças cardíacas.
#### 6.	Campaign Targeting:
- Campanhas devem priorizar grupos com IMC elevado, hipertensão e inatividade física. Além disso, é essencial implementar iniciativas focadas em populações mais velhas e educar sobre a importância de manter um peso saudável.


# Detalhamento dos Insights
Análises específicas baseadas nos aspectos do resumo executivo:
#### Colesterol e Doenças Cardíacas: 
- A média geral dos níveis de colesterol na população é 1,37, com desvio padrão de 0,68. Indivíduos com diagnóstico positivo têm uma média de colesterol de 1,87, significativamente maior do que os sem diagnóstico (1,12).
#### Pressão Arterial: 
- A média da pressão arterial sistólica é de 128,8 mmHg. Indivíduos com pressão acima de 140 mmHg apresentam prevalência de 68% de doenças cardíacas.
#### Atividade Física: 
- 80,4% da população é ativa fisicamente. Entre os inativos (19,6%), a prevalência de doenças cardíacas é 8% maior.
#### Matriz de Confusão: 
- Indica 3418 falsos negativos, sugerindo aprimoramentos no modelo para reduzir erros de previsão.
#### Curva ROC: 
- O AUC de 0.79 reflete uma boa performance geral do modelo, mas com espaço para melhorias.

# Recomendações dos Próximos Passos
#### Campanhas Focadas em Grupos de Risco: 
- Desenvolver campanhas personalizadas para indivíduos com IMC elevado e hipertensão, destacando a importância de mudanças de estilo de vida para reduzir riscos cardiovasculares.
#### Iniciativas Corporativas: 
- Criar parcerias com empresas para oferecer programas de saúde e bem-estar para funcionários. Benefícios como triagens regulares e acesso a academias podem melhorar os indicadores de saúde entre trabalhadores.
#### Incentivos para Atividade Física: 
- Estabelecer programas comunitários gratuitos, como caminhadas em grupo ou eventos esportivos, para incentivar hábitos saudáveis em comunidades menos ativas.
#### Promoção de Alimentação Saudável: 
- Estabelecer parcerias com o setor alimentício para aumentar a disponibilidade de opções saudáveis em supermercados e restaurantes, além de promover rótulos claros sobre benefícios cardiovasculares.
#### Monitoramento Regional: 
- Identificar regiões com maior prevalência de fatores de risco e alocar recursos para essas áreas, promovendo iniciativas locais que atendam às necessidades específicas da comunidade.

#### Essas recomendações foram ajustadas para oferecer soluções práticas e estratégicas, alinhadas ao contexto do negócio, visando reduzir a prevalência de doenças cardíacas e melhorar os resultados populacionais.


# Análise Técnica e Exploratória dos Dados
Descreva a análise exploratória realizada, os métodos aplicados e as descobertas mais relevantes.
