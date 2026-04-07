🚗 Projeto: Controle de Velocidade via Lógica Fuzzy

Este projeto foi desenvolvido para a disciplina de Inteligência Artificial na UFRN. Ele consiste em um sistema de controle de cruzeiro adaptativo simplificado, que decide a aceleração de um veículo com base na distância do carro à frente e na velocidade atual.



📝 Descrição do Problema

O controlador simula a tomada de decisão de um motorista ou de um sistema autônomo usando lógica nebulosa para garantir uma condução segura e fluida.



Variáveis de Entrada (Antecedentes):

Distância (0 a 100m): Classificada em Perto, Média e Longe (usando funções de pertinência Trapézio e Gaussiana).



Velocidade (0 a 120 km/h): Classificada em Baixa, Média e Alta.



Variável de Saída (Consequente):

Ação (-100 a 100): Define se o carro deve Frear, Manter a velocidade ou Acelerar.



🛠️ Tecnologias Utilizadas

Python 3



scikit-fuzzy: Para modelagem do sistema de controle fuzzy.



NumPy: Para criação dos universos de discurso (escalas das variáveis).



Matplotlib: Para geração dos gráficos das funções de pertinência e dos resultados da defuzzificação.



🧠 Lógica e Regras

O sistema utiliza 9 regras lógicas. Por exemplo:



Se a distância é Perto e a velocidade é Alta → Frear.



Se a distância é Longe e a velocidade é Baixa → Acelerar.



Se a distância é Média e a velocidade é Média → Manter.



O cálculo final da ação é feito através do método do Centróide (defuzzificação), que transforma o conjunto nebuloso em um valor numérico exato para o acelerador/freio.

