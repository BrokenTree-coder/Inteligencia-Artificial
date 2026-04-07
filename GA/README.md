✈️ Projeto: Otimização de Rotas via Algoritmo Genético (TSP)

Este projeto foi desenvolvido para a disciplina de Inteligência Artificial na UFRN. O objetivo é encontrar a rota mais eficiente (menor distância total) que percorra uma série de aeroportos e retorne ao ponto de origem, utilizando uma abordagem de Algoritmos Genéticos.



🛠️ Estrutura do Projeto

O projeto está dividido em três etapas principais, cada uma documentada em seu respectivo notebook:



tratamento\_dataset\_AG.ipynb: Limpeza e filtragem do dataset original de aeroportos. Aqui são selecionados os pontos de interesse e preparados os dados geográficos (latitude e longitude).



matriz\_de\_distancias.ipynb: Cálculo da matriz de adjacência. Utiliza as coordenadas geográficas para calcular a distância (via fórmula de Haversine) entre todos os pares de aeroportos, servindo de entrada para o AG.



algoritmo\_genetico.ipynb: A implementação do motor de evolução. Contém a lógica de população, seleção, cruzamento e mutação.



🧬 Detalhes do Algoritmo Genético

O algoritmo busca a solução ótima simulando o processo de evolução natural:



Indivíduo: Uma sequência (rota) que visita todos os aeroportos selecionados.



Fitness (Aptidão): O inverso da distância total da rota (quanto menor a distância, maior a aptidão).



Seleção: Método de torneio para escolher os melhores pais.



Crossover (Cruzamento): Operador especializado para rotas (como o Ordered Crossover - OX) que evita repetição de cidades.



Mutação: Troca de posição entre dois aeroportos na rota (Swap Mutation) para evitar a convergência precoce para um mínimo local, e na camada dos indices dos aeroportos, se tiver apenas um no estado, não tem mutação, mas se tiver mais de um no estado, é sorteado outro indice dentre os restantes.



📊 Tecnologias Utilizadas

Python 3



Pandas: Manipulação de dados e leitura dos datasets CSV.



NumPy: Cálculos matemáticos e manipulação da matriz de distâncias.



Matplotlib/Seaborn: Visualização da evolução da melhor rota ao longo das gerações.



🚀 Como Executar

O fluxo deve seguir a ordem dos notebooks:



Execute o tratamento\_dataset\_AG.ipynb para gerar o arquivo de dados limpos.



Execute o matriz\_de\_distancias.ipynb para gerar a matriz que o algoritmo usará.



Execute o algoritmo\_genetico.ipynb para rodar a simulação e ver o gráfico de convergência.



Desenvolvido por Jean Lucas de A. Lima

