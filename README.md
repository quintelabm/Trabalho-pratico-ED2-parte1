# Trabalho 1: Processamento de Texto

O objetivo desta tarefa é desenvolver um programa para ler e processar arquivos ASCII para encontrar as palavras mais usadas na língua portuguesa. Para isso iremos utilizar como base livros em língua portuguesa disponíveis em:  [Projeto Guteberg](https://www.gutenberg.org/browse/languages/pt) 
Podem escolher 10 livros de forma aleatória.

## Projeto
Há muitas maneiras de atingir esse objetivo, mas vamos usar uma tabela hash para contar o número de vezes que cada palavra única ocorre à medida que digitalizamos o arquivo ascii. Deve-se iniciar com uma tabela de hash vazia. Em seguida, você lerá uma palavra do arquivo ascii e inserirá essa palavra na tabela de hash. Se a palavra já for encontrada na tabela de hash, você incrementa o contador de palavras correspondente em vez de adicionar uma entrada duplicada. Se a palavra não for encontrada na tabela  hash, insira uma nova entrada na tabela de hash com um contador de palavras definido como 1 (um). Quando você terminar de processar o documento, a tabela de hash conterá N palavras exclusivas e seus contadores de palavras associados.

Para encontrar as 50 palavras mais usadas no documento, seu programa deve copiar o conteúdo da tabela de hash em um vetor "words" e ordená-lo em ordem decrescente.

Existem várias questões-chave de design que devem ser abordadas neste trabalho: 
1. como ler o arquivo de texto e extrair as palavras individuais;
2. como armazenar e acessar pares de "palavras / contagem" na tabela de hash;
3. como extrair e classificar pares de "palavras/contagem" para identificar as 50 palavras mais usadas no documento.

Para esta tarefa, os alunos devem usar um encadeamento separado para implementar a tabela hash. Essa abordagem usa listas encadeadas para lidar com colisões na hash, portanto, os alunos devem implementar "list.cpp" no diretório src. Os alunos também são incentivados a consultar o programa "word_hash.cpp" para obter exemplos de E/S de arquivo. 
A tabela de hash de amostra em "hash.cpp" ilustra a API típica para uma tabela de hash e mostra como a sondagem linear pode ser usada para lidar com colisões.

Experimentos que devem ser realizados

1 - Criar casos de testes unitários para testar as funções de hash. 
O grupo pode adotar um dos sistemas de testes unitários: CTest, Googletest e Catch 2.

2. Analisar o desempenho dos métodos de ordenação
Ao identificar as 50 palavras mais usadas de um livro, o grupo deve analisar o desempenho de pelo menos 3 métodos de ordenação. Sendo obrigatoriamente um deles o quicksort, o segundo pode ser qualquer outro método de ordenação visto em aula e o terceiro método de livre escolha do grupo, desde que não tenha sido visto em aula.  As métricas de desempenho são: número de comparações, número de movimentação e tempo de processamento.
Usar o método mais eficiente obtido nas pŕoximas etapas.

2 - Identificar as 50 palavras mais usadas de cada livro
Para cada livro, faça o processamento e escreva em um arquivo ascii as 50 palavras mais frequentes com suas respectivas contagens.

3 - Identificar as 50 palavras mais usadas no total
Escreva em um arquivo ascii as 50 palavras mais frequentes no total com suas respectivas contagens ordenadas em ordem decrescente. Considere para essa atividade que 10 livros devem ser processados.

Observações:
Palavras como artigos (o, a, um…), preposições (de, em, para, …) e pontuações (‘.’ , ‘ !’, ‘?’, ...) devem ser ignoradas nas contagens. 
