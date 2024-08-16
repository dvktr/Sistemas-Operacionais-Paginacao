# Comparação de Sistemas de Paginação: Algoritmos FIFO vs Aging
Este projeto apresenta uma comparação entre dois algoritmos de substituição de páginas: FIFO (First-In-First-Out) e Aging, no contexto de um sistema de paginação.

## Links Externos
- Relatório: [Trabalho_de_SO.pdf](https://github.com/user-attachments/files/16642599/Trabalho_de_SO.pdf)
- Colab: https://colab.research.google.com/drive/190KyIHxx71qnnaN2FfOF-FunQF8798TP?usp=sharing

## Resumo
Este estudo compara os algoritmos FIFO e Aging utilizando uma sequência de 1000 referências de páginas aleatórias, variando o número de quadros de 1 a 20. Os resultados indicam que ambos os algoritmos exibem desempenho semelhante em termos de falhas de página, principalmente devido ao uso de referências aleatórias. Em cenários práticos com padrões de acesso mais previsíveis, o algoritmo Aging tende a superar o FIFO.

## Introdução
A gestão eficiente da memória é crucial para o desempenho dos sistemas computacionais modernos. Nos sistemas operacionais, a paginação é uma técnica amplamente utilizada que divide a memória em blocos menores, chamados de páginas, que são mapeados para quadros de memória física.

O algoritmo FIFO organiza as páginas cronologicamente, removendo a página mais antiga quando uma nova precisa ser carregada. No entanto, este método pode levar a um desempenho subótimo, especialmente quando certas páginas são frequentemente acessadas. O algoritmo Aging, por outro lado, atribui uma prioridade às páginas com base em seu histórico de acesso, proporcionando uma abordagem mais refinada que pode reduzir falhas de página em cenários específicos.

## Metodologia
### Ambiente de Simulação
A simulação foi implementada utilizando Python devido à sua robustez e suporte a bibliotecas essenciais.

### Parâmetros Experimentais
- Total de Páginas: 1000 referências a páginas de memória.
- Páginas Diferentes: 100 páginas diferentes podem ser referenciadas.
- Quadros: O número de quadros disponíveis varia de 1 a 20.

### Implementação dos Algoritmos
FIFO (First-In-First-Out): Este algoritmo remove a página mais antiga do quadro de memória quando uma nova página precisa ser adicionada.
Algoritmo Aging: Este algoritmo usa um contador de bits para representar a "idade" de cada página, atualizando esses valores a cada acesso. Páginas não acessadas recentemente "envelhecem", enquanto páginas acessadas recentemente são "rejuvenescidas".
Execução dos Experimentos
A simulação utilizou uma sequência de 1000 referências de páginas aleatórias entre 100 páginas diferentes. O número de falhas de página foi registrado para cada tamanho de quadro, e os resultados foram comparados utilizando um gráfico.

### Análise de Dados
Os resultados foram tabulados e analisados estatisticamente. Gráficos foram gerados para visualizar o número de falhas de página em função dos quadros de memória disponíveis.

### Validação e Reprodutibilidade
Para garantir a validação e a reprodutibilidade, a sequência de 1000 referências de páginas foi gerada com uma semente fixa e salva em um arquivo de texto. O código e os dados estão disponíveis para que outros pesquisadores possam reproduzir os experimentos e verificar os resultados.

## Resultados
A comparação mostra que ambos os algoritmos FIFO e Aging têm desempenho semelhante em termos de falhas de página neste experimento. Essa semelhança deve-se principalmente à natureza aleatória das referências de página, que neutraliza as vantagens típicas do algoritmo Aging em cenários reais.

## Conclusão
Em ambientes reais, o algoritmo Aging tende a superar o FIFO, especialmente quando certas páginas são acessadas com mais frequência. No entanto, com referências de páginas aleatórias, como foi o caso aqui, nenhum dos algoritmos é claramente favorecido, resultando em desempenho semelhante.

Referências
Tanenbaum, A. S., & Bos, H. (2016). Sistemas Operacionais Modernos. Pearson.
Deitel, H. M., Deitel, P. J., & Choffnes, D. R. (2005). Sistemas Operacionais. Pearson.
Tanenbaum, A. S., & Woodhull, A. S. (2008). Sistemas Operacionais: Projetos e Implementação. Bookman.
