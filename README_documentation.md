# Documentação do Projeto de Dados: Análise de Perfil de Pacientes com Doenças Cardíacas 
![image](https://github.com/user-attachments/assets/a84266c4-266a-42fa-96c2-f151b50b20da)

### Sumário
- [Contexto e Visão Geral](#contexto-e-visão-geral)
- [Visão Geral da Estrutura de Dados](#visão-geral-da-estrutura-de-dados)
- [Resumo Executivo](#resumo-executivo)
- [Detalhamento dos Insights](#detalhamento-dos-insights)
- [Recomendações dos Próximos Passos](#recomendações-dos-próximos-passos)
- [Aplicativo Streamlit](#Aplicativo-Streamlit)
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
- Os fatores de risco mais relevantes para doenças cardíacas são IMC(BMI) elevado, pressão arterial alta e obesidade. Indivíduos com IMC elevado apresentam 76% de prevalência de doenças cardíacas, indicando uma relação direta entre peso corporal e risco cardiovascular.
![image](https://github.com/user-attachments/assets/9d0e1048-91ee-4f1b-ad3e-2f9d67caed7f)


#### 2.	Cholesterol Impact: 
- Existe uma forte relação entre colesterol elevado e doenças cardíacas. Indivíduos com colesterol acima do normal têm uma prevalência 36% maior de doenças cardíacas em comparação àqueles com colesterol normal.
  ![image](https://github.com/user-attachments/assets/f1cc6369-3589-4a8f-890f-e118fc1b8e8b)
#### 3.	Vulnerable Groups: 
- Indivíduos acima de 60 anos representam 35% dos casos de doenças cardíacas, enquanto aqueles abaixo de 40 anos representam apenas 5%. Homens possuem um risco levemente maior (52%) em relação às mulheres (48%).
  ![image](https://github.com/user-attachments/assets/10016dd8-7e20-407f-971e-a1dfac5453a9)

#### 4.	Lifestyle Influence:
- Indivíduos fisicamente inativos têm uma prevalência de doenças cardíacas 8% maior do que os ativos. Curiosamente, fumantes apresentaram uma prevalência 3% menor em relação aos não fumantes, o que pode indicar viés ou fatores subjacentes.
  ![image](https://github.com/user-attachments/assets/fcb939f1-3fff-4917-8c13-32600f9795db)

#### 5.	Insights Baseados no Modelo de Previsão:
- O modelo de previsão destaca que IMC, pressão arterial alta e idade são os fatores mais importantes para a identificação de riscos de doenças cardíacas.
  ![Captura de Tela (804)](https://github.com/user-attachments/assets/e8990312-b2cb-41d0-bde1-5ff4d65e1f3a)

#### 6.	Campaign Targeting:
- Campanhas devem priorizar grupos com IMC elevado, hipertensão e inatividade física. Além disso, é essencial implementar iniciativas focadas em populações mais velhas e educar sobre a importância de manter um peso saudável.


# Detalhamento Estatístico
![Captura de Tela (811)](https://github.com/user-attachments/assets/9de5a9b7-79f5-411c-b231-f31b22433dfb)

Análises específicas baseadas nos aspectos do resumo executivo:
#### Colesterol e Doenças Cardíacas: 
- A média geral dos níveis de colesterol na população é 1,37, com desvio padrão de 0,68. Indivíduos com diagnóstico positivo têm uma média de colesterol de 1,87, significativamente maior do que os sem diagnóstico (1,12).
#### Pressão Arterial: 
- A média da pressão arterial sistólica é de 128,8 mmHg. Indivíduos com pressão acima de 140 mmHg apresentam prevalência de 68% de doenças cardíacas.
#### Atividade Física: 
- 80,4% da população é ativa fisicamente. Entre os inativos (19,6%), a prevalência de doenças cardíacas é 8% maior.
#### Matriz de Confusão: 
- Indica 3418 falsos negativos, sugerindo aprimoramentos no modelo para reduzir erros de previsão.
  ![Captura de Tela (806)](https://github.com/user-attachments/assets/7e46370a-91c3-44c3-9ab3-960b05b937ee)

#### Curva ROC: 
- O AUC de 0.79 reflete uma boa performance geral do modelo, mas com espaço para melhorias.
![Captura de Tela (805)](https://github.com/user-attachments/assets/0e959ab6-eb29-4518-9195-ee427d70ccb9)

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

# Aplicativo Streamlit
- Nesta etapa do projeto, foi desenvolvida uma aplicação interativa onde o usuário pode inserir suas informações pessoais e de saúde por meio de um formulário. As informações solicitadas no formulário incluem todas as features utilizadas durante o treinamento do modelo, como peso, idade, pressão arterial (tanto alta quanto baixa), níveis de colesterol, glicose, entre outras variáveis relacionadas aos fatores de risco para doenças cardiovasculares. O objetivo dessa aplicação é permitir que o usuário insira seus dados e, com base nas informações fornecidas, o modelo realize a predição da probabilidade de o indivíduo desenvolver uma doença cardíaca. A partir dessa interação, é possível obter uma previsão personalizada e imediata, diretamente relacionada aos fatores de risco individuais de cada usuário.
![image](https://github.com/user-attachments/assets/5cedab3a-e056-43e7-a78f-2bbee95e9375)
- Além da predição percentual sobre a probabilidade de desenvolver doenças cardíacas, a aplicação foi configurada para fornecer dicas personalizadas com base no nível de risco identificado pelo modelo. O nível de risco é dividido em três categorias principais: baixa, média e alta. Dependendo da probabilidade calculada pelo modelo, o usuário recebe orientações específicas adequadas ao seu nível de risco. Essas dicas visam ajudar o usuário a compreender melhor sua situação e tomar medidas apropriadas com base nos resultados obtidos. Assim, a aplicação não só fornece uma previsão quantitativa, mas também oferece recomendações que podem auxiliar na prevenção ou controle dos fatores de risco, dependendo do perfil identificado.
  ![image](https://github.com/user-attachments/assets/b220b5b3-b641-452c-bb7b-1bab8f25a702)

# Análise Técnica e Exploratória dos Dados

### Processo de Limpeza de Dados


Durante o processo de preparação do conjunto de dados, foram realizadas as seguintes etapas para garantir a qualidade e a consistência das informações:

#### Correção do Carregamento de Dados:
- Foi ajustado o carregamento dos dados utilizando o separador correto (';'), o que garantiu a correta delimitação e estruturação das colunas.
#### Conversão de Idade:
- A idade, originalmente armazenada em dias, foi convertida para anos para facilitar a interpretação e a análise dos dados.
#### Tratamento de Valores Irrealistas:
- Foram removidos registros que apresentavam valores fora dos limites aceitáveis para certas variáveis:
 - Altura: limitada a valores entre 140 e 200 cm.
 - Peso: restringido a valores entre 40 e 200 kg.
  - Pressão Arterial Sistólica: valores entre 80 e 220 mmHg.
   - Pressão Arterial Diastólica: valores entre 40 e 120 mmHg.
Também foi garantido que a pressão sistólica fosse maior que a pressão diastólica em todos os registros.
#### Remoção de Valores Nulos e Duplicatas:
- Todos os registros com valores ausentes em qualquer coluna relevante foram removidos.
Foram eliminadas duplicatas para evitar a contagem repetida de informações idênticas.
#### Tratamento de Outliers:
- Valores considerados outliers extremos em variáveis contínuas foram identificados e removidos com base em técnicas estatísticas, como o uso do intervalo interquartil (IQR).
#### Reclassificação do Gênero:
- O gênero foi mapeado para valores binários (0 e 1), simplificando a análise.
#### Impacto da Limpeza:
Após o processo de limpeza, o conjunto de dados foi reduzido de 70.000 para 68.424 registros. Isso representou uma redução de cerca de 2,3%, eliminando dados potencialmente problemáticos, como valores fora dos limites realistas, registros incompletos e duplicados. Este processo foi essencial para garantir a integridade das análises subsequentes

### Análise de Correlação
![image](https://github.com/user-attachments/assets/0cd17526-46e5-4812-a32b-06361a7f60a7)
#### Peso e IMC:
- A correlação mais forte encontrada foi entre o peso (weight) e o índice de massa corporal (IMC), com um coeficiente de correlação de 0.86. Este resultado é esperado, pois o IMC é diretamente calculado a partir do peso e da altura dos indivíduos. Uma correlação tão alta indica que, conforme o peso aumenta, o IMC também tende a aumentar significativamente, reforçando a importância do controle do peso corporal para a manutenção de um IMC saudável.
#### Pressão Arterial e Doenças Cardíacas:
- Em seguida, foi observada uma correlação positiva forte entre a pressão arterial sistólica (ap_hi) e a pressão arterial diastólica (ap_lo), com um coeficiente de correlação de 0.67. Esta correlação indica que, geralmente, quando a pressão sistólica é alta, a diastólica também tende a ser alta. Este comportamento é consistente com a fisiologia do sistema cardiovascular, onde ambos os tipos de pressão arterial são influenciados por fatores comuns como resistência vascular e volume sanguíneo.
#### Colesterol e Glicose:
- Entre os fatores metabólicos, a correlação entre colesterol (cholesterol) e glicose (gluc) foi moderada, com um coeficiente de 0.45. Pacientes com níveis elevados de colesterol tendem a ter níveis elevados de glicose, sugerindo uma possível relação entre dislipidemia e desregulação glicêmica. Esta correlação destaca a importância de uma abordagem integrada no manejo de fatores de risco metabólicos para prevenir doenças cardiovasculares.
#### Fumo e Gênero:
- Outro ponto relevante é a correlação entre fumo (smoke) e gênero (gender), que foi de 0.34. Este valor moderado indica que um dos gêneros tem uma maior prevalência de fumantes. Esta informação pode ser crucial para direcionar campanhas de cessação do tabagismo e intervenções específicas baseadas em gênero.
#### Peso e Pressão Arterial:
- Adicionalmente, foi observada uma correlação fraca entre peso (weight) e pressão arterial sistólica (ap_hi), com um coeficiente de 0.26. Embora a correlação seja menor, ela sugere que um aumento no peso pode estar associado a um aumento na pressão arterial sistólica, ressaltando a importância do controle do peso para a saúde cardiovascular.
#### Idade e Pressão Arterial:
- A correlação entre idade (age_years) e pressão arterial sistólica (ap_hi) também foi fraca, com um coeficiente de 0.20. Isso indica que, conforme a idade aumenta, há uma tendência de aumento na pressão arterial sistólica, embora essa relação não seja muito forte. Este achado é consistente com a tendência geral de aumento da pressão arterial com o envelhecimento.
#### Idade e Doenças Cardiovasculares:
- Por fim, a correlação entre idade (age_years) e a presença de doenças cardiovasculares (cardio) foi de 0.24. Embora fraca a moderada, esta correlação sugere que a probabilidade de desenvolver doenças cardiovasculares aumenta ligeiramente com a idade. Este achado é importante para o desenvolvimento de estratégias de prevenção que visem populações mais idosas.
