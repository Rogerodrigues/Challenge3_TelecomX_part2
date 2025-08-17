# Challenger3_TelecomX_part2

📖 Descrição
Este projeto foca na análise e modelagem preditiva da evasão de clientes (churn) em uma empresa de telecomunicações. O objetivo principal é desenvolver um modelo de machine learning preciso para identificar clientes com alta probabilidade de cancelar seus serviços, além de extrair insights acionáveis sobre os principais fatores que influenciam essa decisão.

Através de um pipeline completo de análise de dados — desde o pré-processamento e tratamento de classes desbalanceadas até a modelagem e avaliação de performance —, o projeto compara dois algoritmos (Regressão Logística e Random Forest) e traduz os resultados em estratégias de negócio para a retenção de clientes.

🗂️ Índice
Descrição
Tecnologias Utilizadas
Instalação
Uso
Metodologia de Análise
Resultados
Conclusão e Recomendações Estratégicas

🛠️ Tecnologias Utilizadas
O projeto foi desenvolvido utilizando as seguintes tecnologias e bibliotecas:

Python 3.11+

Pandas: Para manipulação e análise de dados.

NumPy: Para operações numéricas.

Matplotlib & Seaborn: Para visualização de dados.

Scikit-learn: Para pré-processamento, modelagem e avaliação de métricas.

Imbalanced-learn: Para técnicas de balanceamento de classes (SMOTE).

Google Colab: Como ambiente de desenvolvimento.

⚙️ Instalação
Para executar este projeto localmente, siga os passos abaixo:

1.Clone o repositório:
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio

2.Crie e ative um ambiente virtual (recomendado):
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

3.Instale as dependências:
pip install -r requirements.txt
Obs: O arquivo requirements.txt deve conter pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn e jupyter.

▶️ Uso
Após a instalação, inicie o Jupyter Notebook e abra o arquivo principal para executar a análise:
Google Colab Challenge3_TelecomX_part2.ipynb

O notebook está dividido em seções que cobrem todo o processo de análise, desde o carregamento dos dados até a conclusão final e recomendações de negócio.

🔬 Metodologia de Análise
O fluxo de trabalho seguiu as seguintes etapas:

Preparação dos Dados: O conjunto de dados tratado (dados_tratados.csv) foi carregado e colunas irrelevantes, como ID_Cliente, foram removidas.

Pré-processamento:

Encoding: Todas as variáveis categóricas foram transformadas em formato numérico utilizando a técnica de One-Hot Encoding (pd.get_dummies).

Balanceamento de Classes: Foi identificado um desbalanceamento na variável alvo Churn (73% permaneceram, 27% saíram). A técnica SMOTE (Synthetic Minority Over-sampling Technique) foi aplicada para criar um conjunto de dados sintético e balanceado, garantindo que o modelo aprendesse os padrões de ambas as classes de forma equitativa.

Padronização: As features foram padronizadas (Standardization) com StandardScaler para otimizar o desempenho de modelos sensíveis à escala, como a Regressão Logística.

Análise de Correlação: Foi calculada a correlação entre todas as variáveis e a variável Churn para identificar os fatores com maior impacto (positivo e negativo) na evasão.

Modelagem Preditiva:

Os dados foram divididos em conjuntos de treino (70%) e teste (30%).

Foram treinados dois modelos distintos:

Regressão Logística: Um modelo linear robusto e interpretável.

Random Forest: Um modelo de ensemble mais complexo e com alta capacidade preditiva.

Avaliação de Modelos: Os modelos foram avaliados em dados de teste usando as seguintes métricas:

Acurácia, Precisão, Recall e F1-Score.

Matriz de Confusão para visualizar os acertos e erros (especialmente os Falsos Negativos, que representam o maior custo para o negócio).

Análise de Importância: Foram extraídos os coeficientes da Regressão Logística e a importância das variáveis (feature importance) do Random Forest para validar e aprofundar os insights de negócio.

📊 Resultados
A modelagem forneceu resultados claros e de alto impacto:

Comparação de Desempenho
O modelo Random Forest demonstrou desempenho superior, alcançando uma acurácia e um F1-Score mais elevados nos dados de teste. Sua principal vantagem foi um Recall superior na classe "Churn", indicando uma maior capacidade de identificar corretamente os clientes que realmente iriam cancelar.

Fatores de Influência no Churn
Ambos os modelos apontaram para um conjunto consistente de fatores como os mais influentes na evasão de clientes:

Principais Fatores que AUMENTAM a Chance de Churn:

Contrato Mensal: O indicador mais forte de risco de churn.

Internet com Fibra Ótica: Pode indicar problemas de serviço, preço ou forte concorrência no segmento.

Pagamento com Cheque Eletrônico: Forma de pagamento associada a uma maior taxa de evasão.

Principais Fatores que DIMINUEM a Chance de Churn (Retenção):

Tempo de Contrato (MesesContrato): O fator de retenção mais forte. A lealdade aumenta com o tempo.

Contratos de 1 ou 2 anos: A fidelidade contratual reduz drasticamente a probabilidade de churn.

Serviços Adicionais: A contratação de serviços como suporte técnico e segurança online aumenta o engajamento e a retenção.

🚀 Conclusão e Recomendações Estratégicas
A análise preditiva foi bem-sucedida, resultando em um modelo Random Forest robusto e insights valiosos. Com base nos fatores identificados, recomendamos as seguintes ações estratégicas para a empresa:

Campanha de Migração de Contratos Mensais:

Ação: Lançar uma campanha proativa para clientes com contrato mensal e alto score de risco (identificados pelo modelo), oferecendo incentivos (descontos, serviços adicionais) para migrarem para contratos de 1 ou 2 anos.

Programa de Engajamento para Novos Clientes ("Primeiro Ano Dourado"):

Ação: Desenvolver um programa de comunicação e benefícios focado em clientes com menos de 12 meses (período de maior risco), realizando contatos de "saúde da conta" para garantir a satisfação.

Otimização de Pacotes e Upsell de Serviços de Valor Agregado:

Ação: Criar ofertas de "bundle" que incluam Suporte Técnico ou Segurança Online para clientes com pacotes básicos e faturas mais altas, aumentando a percepção de valor.

Investigação e Ação no Segmento de Fibra Ótica:

Ação: Realizar uma pesquisa de satisfação focada nos clientes de Fibra para entender os motivos da alta evasão (preço, qualidade, atendimento) e criar ações de correção.

Incentivo a Métodos de Pagamento Automáticos:

Ação: Oferecer um crédito único na fatura para clientes que migrarem do pagamento por Cheque Eletrônico para métodos mais seguros, como Cartão de Crédito ou Débito Automático.




