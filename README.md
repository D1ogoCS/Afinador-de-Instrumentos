# Afinador de Instrumentos
## Afinador que se ajusta automaticamente ao instrumento musical escolhido pelo utilizador

Foi proposto realizar um projeto que englobasse uma área de Processamento Digital de Sinais e decidi criar uma aplicação, que tem como função ser um afinador que se adapta ao instrumento musical escolhido pelo utilizador.

### Objetivos:
- O utilizador deve escolher qual o instrumento musical que quer afinar
- Ser possível visualizar um gráfico com as frequências que estão a ser capturadas em tempo real
- Mostrar a frequência que está a ser captada
- Indicar a nota e a oitava
- Se o instrumento estiver desafinado, indicar com uma seta para que lado se encontra a nota mais próxima. Se o instrumento estiver afinado, deve aparecer a mensagem "Ok"
- Utilizar um filtro que foi lecionado durante as aulas de Processamento Digital de Sinais

### Ferramentas utilizadas:
- IDLE (Python 3.10 64-bit)

### Tecnologias utilizadas:
- Linguagem Python

### Requisitos técnicos:
- Python 3.7 ou superior
- tkinter
- matplotlib
- pyaudio
- numpy
- scipy
- threading

### Bibliotecas:

- __tkinter__: É uma biblioteca gráfica que permite criar interfaces gráficas para o utilizador (GUI's) em Python. Com o tkinter, é possível criar janelas, botões, caixas de texto, menus, entre outros elementos da interface gráfica.

- __matplotlib.animation.FuncAnimation__: É uma classe da biblioteca matplotlib que permite criar animações em Python. É usada para criar animações de gráficos, como gráficos de linha, de barra, de dispersão, entre outros. A classe FuncAnimation permite criar animações com base numa função que é chamada repetidamente em intervalos regulares.

- __matplotlib.pyplot__: É uma função da biblioteca matplotlib que fornece uma interface para criar gráficos em Python. É usada para criar gráficos de linha, de barra, de dispersão, entre outros. A biblioteca pyplot é baseada na biblioteca MATLAB e é muito útil para visualizar dados em Python.

- __pyaudio__: É uma biblioteca que fornece uma interface para trabalhar com áudio em Python. É usada para gravar e reproduzir áudio em tempo real. A biblioteca pyaudio é muito útil para criar aplicações que precisam trabalhar com áudio, como aplicações de gravação de voz, de reconhecimento de fala, entre outros.

- __numpy__: É uma biblioteca que fornece suporte para arrays e matrizes multidimensionais em Python. É usada para realizar operações matemáticas em arrays e matrizes, como adição, subtração, multiplicação, divisão, entre outras. A biblioteca numpy é muito útil para trabalhar com dados numéricos em Python.

- __scipy.signal.butter__: É uma função da biblioteca scipy.signal que é usada para projetar filtros digitais que podem ser usados para filtrar sinais de áudio, sinais de vídeo, entre outros.

- __scipy.signal.lfilter__: É uma função da biblioteca scipy.signal que é usada para filtrar sinais digitais. A função lfilter é muito útil para filtrar sinais de áudio, sinais de vídeo, entre outros.

- __threading__: É uma biblioteca que fornece suporte para threads em Python. É usada para criar e gerir threads no Python. A biblioteca threading é muito útil para criar aplicações que precisam executar várias tarefas simultaneamente.

### Funções desenvolvidas:
Para que o código da aplicação fique mais organizado e não exista repetição de código, foram implementadas algumas funções.

- __executarComoThread()__: Define a animação do gráfico. Cria uma animação do gráfico que é atualizada a cada 500 milissegundos. A função atualizarGrafico() é executada a cada atualização e é responsável por atualizar o gráfico.

- __atualizarGrafico()__: Define uma função que recebe um parâmetro i. A função atualiza os valores do eixo X e cria um gráfico com os valores das frequências. O gráfico é composto por duas linhas, uma vermelha e outra azul, que representam as frequências sem filtro e com filtro, respetivamente. O gráfico também possui um título, rótulos para os eixos X e Y e uma legenda. O limite do eixo Y é definido de acordo com o instrumento escolhido. Além disso, a função adiciona os valores no gráfico.

- __butterBandpass()__: Define uma função que implementa um filtro passa-banda Butterworth. Aceita quatro argumentos: lowcut, highcut, fs e order.

    lowcut: A frequência de corte inferior do filtro em Hz.

    highcut: A frequência de corte superior do filtro em Hz.

    fs: A taxa de amostragem do sinal em Hz.

    order: A ordem do filtro Butterworth. 

    A função retorna dois arrays NumPy, *b* e *a*, que representam os coeficientes do filtro. Esses coeficientes podem ser usados para filtrar um sinal usando a função lfilter do módulo scipy.signal.

- __butterBandpassFilter()__: Define uma função que implementa um filtro passa-banda Butterworth de ordem *n* para um sinal de entrada com frequências de corte e taxa de amostragem. O filtro é implementado usando a função butterBandpass() que retorna os coeficientes do filtro. Em seguida, a função lfilter() é usada para aplicar o filtro ao sinal de entrada usando os coeficientes do filtro. O sinal filtrado é retornado pela função.

- __buscarBlocoNotas()__: Define uma função que recebe um argumento "option" e define a variável global "blocoNotas" com base no valor de "option".

- __introduzirNotas()__: Define uma função que recebe um número variável de argumentos. A função tem como objetivos: procurar um bloco de notas, limpar o dicionário "notas", ler o bloco de notas e armazená-las as notas no dicionário "notas". Em seguida, a função procura o menor e o maior valor do dicionário "notas" e armazena-os nas variáveis globais "menorValor" e "maiorValor", respetivamente. Por fim, a função imprime o menor e o maior valor do dicionário "notas" e verifica se o dicionário está correto, imprimindo as chaves e os valores do dicionário "notas".

- __ouvir()__: Define uma função que durante um intervalo de tempo recolhe o que é captado pelo microfone e guarda esses dados num array. Após isso, o array é convertido para um array numpy do tipo int16, é aplicado o filtro passa-banda e são calculadas as frequências com e sem filtro.
Depois são executadas algumas operações com base no valor de "selected_option". Se "selected_option" for igual a "Notas Gerais", o código percorre o dicionário "notas" e encontra o valor mais próximo da frequência. Se "selected_option" não for igual a "Notas Gerais", o código percorre o dicionário "notas" e encontra a nota que corresponde à frequência fornecida. Se a frequência captada for menor que a frequência exata da nota, a variável "simbolo" é definida como "--->" e a variável "cor" é definida como "red". Se a frequência captada for maior que a frequência exata da nota, a variável "simbolo" é definida como "<---" e a variável "cor" é definida como "red". Caso contrário, a variável "simbolo" é definida como "OK" e a variável "cor" é definida como "green".

### Resultados:
![Janela principal](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/janelaPrincipal.png)

*Janela principal*

![Instrumentos disponíveis](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/instrumentosDisponiveis.png)

*Instrumentos disponíveis*

![Nota correta](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/frequenciaCorreta.png)

*Nota correta*

![Nota incorreta](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/frequenciaErrada.png)

*Nota incorreta*

![Gráfico de frequências em tempo real](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/graficoFrequencias.png)

*Gráfico de frequências em tempo real*

![Ilustração do filtro Butterworth](https://github.com/D1ogoCS/Afinador-de-Instrumentos/blob/main/imagens/filtroButterworth.png)

*Iustração do filtro Butterworth*

