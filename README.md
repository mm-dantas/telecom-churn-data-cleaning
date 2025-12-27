Telecom Churn - Limpeza e Tratamento de Dados
Este projeto foca-se na etapa de Data Wrangling de um conjunto de dados de uma empresa de telecomunicações. O objetivo principal é transformar dados brutos (formato JSON aninhado) num formato estruturado, limpo e pronto para etapas futuras de análise exploratória e modelagem de Machine Learning para previsão de Churn (cancelamento de clientes).

🛠️ Tecnologias Utilizadas
Python 3

Pandas: Manipulação e análise de dados.

NumPy: Operações matemáticas e tratamento de valores nulos.

📋 Etapas do Projeto
O notebook está organizado seguindo um fluxo lógico de tratamento de dados:

Carregamento e Normalização:

Leitura de dados brutos em formato JSON.

Uso de json_normalize para transformar dicionários aninhados em colunas individuais (ex: dados de cliente, telefone e internet).

Identificação e Tratamento de Dados Vazios:

Deteção de strings vazias na variável alvo (Churn) e remoção de registos irrelevantes.

Tratamento de valores NaN em colunas críticas como tempo_servico.

Conversão de Tipos:

Transformação de colunas numéricas que estavam carregadas como objetos (ex: cobranca.Total).

Codificação de Variáveis (Encoding):

Mapeamento de variáveis categóricas binárias (sim/nao, masculino/feminino) para valores numéricos 0 e 1.

Aplicação de técnicas para lidar com variáveis multicategóricas (ex: métodos de pagamento e tipos de contrato).

Remoção de Outliers:

Análise estatística e remoção de valores atípicos que poderiam enviesar modelos futuros.

🚀 Como Executar
Clone o repositório:

Bash

git clone https://github.com/seu-usuario/telecom-churn-data-cleaning.git
Instale as dependências:

Bash

pip install pandas numpy
Certifique-se de que o ficheiro dataset-telecon.json está no mesmo diretório ou ajuste o caminho no notebook.

📊 Estrutura do Dataset Original
O dataset original continha informações sobre:

Cliente: Género, idade, se possui parceiro ou dependentes.

Serviços: Telefone, múltiplas linhas, internet, segurança online, backup, streaming, etc.

Conta: Tipo de contrato, método de pagamento e valores de cobrança (mensal e total).# telecom-churn-data-cleaning
