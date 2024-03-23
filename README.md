# dio-machine-learning
laboratorio de machine learning da DIO
---


## Criação do ambiente

1) No portal azure > iniciar o estudo > cria o workspace
2) dentro do ML automatizado clica em novo trablho ML automatizado

## Configuração do experimento
### informações
3) preenche as informações do nome do experimento, a descrição

### configurações da tarefa e dos dados
4) selecionamos regressão no tipo de tarefa
5) seleciona os tipo de dados e selciona a fonte dos dados https://aka.ms/bike-rentals
6) São feitas as configurações dos dados e como eles serão lidos, escolhendo o formato, delimitador, codificação e cabeçalhos das colunas
7) são configurados os tipos de dados que tem as colunas <- quando são escolhidos tipos de dados e a coluna tem um tipo diferente é remplazado pelo valor nulo

### configurações do treinamento
8) é selecionada a coluna que vai ser o target para a previsão no caso é rentals(integer)
9) è selcionada a metrica primaria utilizando NormalizedRootMeanSquaredError - Raiz do erro quadratico meio normalizado
10) em modelos são escolhidos RandomForest e LightGBM
11) São configurados os limites -> Maximo de avaliações | 3  - Maximo de avaliações simultaneas | 3  - Maximo de nós | 3 - Limite da puntuação da metrica | 0.085 - Tempo limite do experimento | 15 minutos - Tempo limite da interação | 15 minutos - habilitamos o encerramento antecipado - Tipo de validação | Divisão de validação de treinamento - Validação de percentual de dados | 10
12) selecionamos o tipo de computação, no caso sem servidor, tipo de maquina virtual sendo Cpu, tipo de maquina virtual como Dedicado, o tamanho Standar, e no numero de instancias sendo 1
13) Clicamos em enviar trabalho de treinamento

## Validação dos resultados
14) Depois de realizado o treinamento, o modelo fica disponivel para analisé e teste
15) Nas metricas podem ser encontrados os graficos residuais e onde pode ser visualizados o resultados dos valores reais comparados com os valores preditos
16) Selecionando no botão de pontos de extremidade podem ser realizados os testes: eles são realizados utilizando um JSON, pudendo modificar ele para analizar os diferentes resultados
