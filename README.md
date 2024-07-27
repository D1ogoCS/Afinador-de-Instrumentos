# Afinador de Instrumentos
## Afinador que se ajusta automaticamente ao instrumento musical escolhido pelo utilizador

Foi proposto realizar um projeto que englobasse uma área de Processamento Digital de Sinais e decidi criar uma aplicação, que tem como função ser um afinador que se adapta ao instrumento musical escolhido pelo utilizador.

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

### Bibliotecas utilizadas:

- __tkinter__: É uma biblioteca gráfica que permite criar interfaces gráficas para o utilizador (GUI's) em Python. Com o tkinter, é possível criar janelas, botões, caixas de texto, menus, entre outros elementos da interface gráfica.

- __matplotlib.animation.FuncAnimation__: É uma classe da biblioteca matplotlib que permite criar animações em Python. É usada para criar animações de gráficos, como gráficos de linha, de barra, de dispersão, entre outros. A classe FuncAnimation permite criar animações com base numa função que é chamada repetidamente em intervalos regulares.

- __matplotlib.pyplot__: É uma função da biblioteca matplotlib que fornece uma interface para criar gráficos em Python. É usada para criar gráficos de linha, de barra, de dispersão, entre outros. A biblioteca pyplot é baseada na biblioteca MATLAB e é muito útil para visualizar dados em Python.

- __pyaudio__: É uma biblioteca que fornece uma interface para trabalhar com áudio em Python. É usada para gravar e reproduzir áudio em tempo real. A biblioteca pyaudio é muito útil para criar aplicações que precisam trabalhar com áudio, como aplicações de gravação de voz, de reconhecimento de fala, entre outros.

- __numpy__: É uma biblioteca que fornece suporte para arrays e matrizes multidimensionais em Python. É usada para realizar operações matemáticas em arrays e matrizes, como adição, subtração, multiplicação, divisão, entre outras. A biblioteca numpy é muito útil para trabalhar com dados numéricos em Python.

- __scipy.signal.butter__: É uma função da biblioteca scipy.signal que é usada para projetar filtros digitais que podem ser usados para filtrar sinais de áudio, sinais de vídeo, entre outros.

- __scipy.signal.lfilter__: É uma função da biblioteca scipy.signal que é usada para filtrar sinais digitais. A função lfilter é muito útil para filtrar sinais de áudio, sinais de vídeo, entre outros.

- __threading__: É uma biblioteca que fornece suporte para threads em Python. É usada para criar e gerir threads no Python. A biblioteca threading é muito útil para criar aplicações que precisam executar várias tarefas simultaneamente.

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

