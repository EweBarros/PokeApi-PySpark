 <img src="https://i.postimg.cc/ZRSDQWPG/pokeapi-pyspark.png" width = "500"/> <center>

# Consumindo e analisando dados da PokéApi utilizando Pyspark

Este projeto desenvolve um problema de pipeline de ponta a ponta, seguindo os seguintes passos:
- Extração dos dados da [PokéApi](https://pokeapi.co/docs/v2), API oficial do jogo Pokémon, utilizando Python;
- Interpretação dos dados e levantamento dos atributos necessários para responder a perguntas específicas de negócio;
- Modelagem relacional dos dados de acordo com os atributos necessários;
- Tratamento dos dados;
- Análise dos dados para responder às perguntas de negócio, utilizando PySpark.
  
## Conceitos de Pokémon
Para um melhor entendimento dos problemas, é necessário conhecer alguns conceitos previamente:
  
- Formas: são os estágios evolutivos em que o Pokémon se encontra.
- Primeira forma: o Pokémon no seu estágio inicial, que ainda não evoluiu.
- Segunda forma: o Pokémon que evoluiu a partir da primeira forma.
- Terceira forma: o Pokémon que evoluiu a partir da segunda forma.
- Caminhos evolutivos: são todas as possíveis combinações evolutivas de um Pokémon.
  - Pichu -> Pikachu -> Raichu (apenas 1 caminho evolutivo)
  - Poliwag -> Poliwhirl -> Poliwrath ou Poliwag -> Poliwhirl -> Politoed (2 caminhos
evolutivos).\
  [Neste link](https://www.pokemythology.net/conteudo/grupos/multiplas_evolucoes.htm) pode-se encontrar mais exemplos de Pokémon com mais de um caminho evolutivo.
- Forma padrão: É como o Pokémon é encontrado naturalmente na sua forma atual.\
  Existem formas alternativas para um Pokémon, que dependendo da região em que ele se encontra\
  (conhecidos também por Alolan Form e Galarian Form), ele ganha características diferentes.\
  Também existe um tipo especial de evolução (mega evolução), que não é caracterizado como evolução,\
  mas altera as características do Pokémon na forma atual que ele se encontra.

  
## As seguintes perguntas foram respondidas:
  
### Pergunta 1:
Quais são os maiores Pokémon? Exiba os Pokémon e a altura.  
  
### Pergunta 2:
Quantos Pokémon possuem mais de um caminho evolutivo, ou seja, mais de uma segunda ou terceira forma?\
Informe a quantidade, tomando como base o número distinto de Pokémon na sua primeira forma.

### Pergunta 3:
Quais são os Pokémon do tipo gelo (ice) que mais fornecem experiência ao serem derrotados? Leve em\
consideração apenas os Pokémon que estão em sua forma padrão. Exiba os Pokémon e a experiência que é fornecida.

### Pergunta 4:
Encontre o golpe (move) que é mais aprendido por Pokémon pelo método level-up e em quais versões do jogo\
isso acontece, levando em consideração apenas os Pokémon que estão em sua forma padrão. Em seguida, entre os\
Pokémon que aprendem esse golpe (por level-up e nas versões do jogo encontrada no passo anterior), diga quais\
são os Pokémon que possuem o maior valor do atributo (stat) ‘attack’. Exiba os Pokémon, as versões do jogo\
em que acontece de mais Pokémon aprenderem o golpe e qual é o valor do atributo ‘attack’ deles.
  
### Pergunta 5:
Quais são as 7 evoluções que geram o maior aumento em algum dos atributos? Por exemplo, um Pokémon com o\
stat ‘attack’ igual a 50 evoluir para um com o stat ‘attack’ igual a 150, o aumento seria de 100. A análise deve ser\
feita para todos os atributos de todos os Pokémon, e somente aqueles na sua forma padrão. Exiba a pré-evolução,\
a evolução, o atributo afetado e o quanto ele aumentou com a evolução.
  
### Pergunta 6:
Quais são os Pokémon com maior vantagem atacante sobre outros Pokémon? Leve em consideração apenas o tipo do\
Pokémon (Um Pokémon do tipo fogo/lutador (fire/fighting) possui vantagem atacante em um Pokémon inseto/voador\
(bug/flying), pois o tipo fogo tem vantagem sobre inseto, apesar do tipo lutador não ser eficiente contra o tipo\
inseto e voador) e apenas os Pokémon que estão em sua forma padrão. Exiba os Pokémon, e a quantidade de Pokémon\
que eles possuem vantagem atacante sobre.

**OBS**: As perguntas estão no plural, mas pode ser que apenas um Pokémon seja a resposta. Haverá mais de uma\
resposta quando devidamente explicitado, ou quando os Pokémon possuírem valor igual no que é solicitado (se 2\
Pokémon possuírem a maior altura, os 2 serão a resposta). 

  
