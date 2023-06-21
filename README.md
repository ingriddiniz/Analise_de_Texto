# Analise_de_Texto
Análise de texto usando Python <br>
<br>
Este é um projeto da cadeira de Programação 2 da faculdade de Ciências da Universidade do porto, cujo objetivo é análisar textos a partir de ficheiros de texto.
<br>
Neste projeto processou-se o texto completo do *Sermão de Santo António aos Peixes* do *Padre António Vieira*, extrair métricas simples e reformatar o texto.  
  
## Tarefa 1

Foi feito um download do ficheiro [sermao.txt](../scripts/projeto1/dados/sermao.txt), que contém o texto integral do *Sermão de Santo António aos Peixes* do *Padre António Vieira*.

Aprimeira função `leTexto` lê o conteúdo de um ficheiro de texto para uma lista de linhas de texto, em que cada linha de texto é uma string sem caracteres newline.

## Tarefa 2

A função ``organizaSermao`` organiza uma lista de linhas de texto num tuplo (título,introdução,lista de capítulos), em que cada capítulo é um tuplo (número,lista de parágrafos). Cada linha do título, introdução e parágrafo é por sua vez uma lista de palavras (com pontuação).
Por exemplo, para um sermão dado como a lista de linhas:
```python
['SERMÃO DE EXEMPLO'
,''
,'A título de exemplo.'
,'Veni, vidi, vici.'
,''
,'I'
,''
,'Parágrafo um.'
,'Parágrafo dois.'
]
```
O resultado organizado esperado é:
```python
(['SERMÃO','DE','EXEMPLO'],[['A','título','de','exemplo.'],['Veni,','vidi,','vici.']],[('I',[['Parágrafo','um.'],['Parágrafo','dois.']])])
```

Foram feitas algumas funções auxiliares:
- A função `separaLinha` que parte uma linha (string sem newlines) numa lista de palavras;
- A função `separaLinhas`, que parte uma lista de linhas numa lista de listas de linhas, usando como delimitador strings vazias;
- A função `organizaCapitulos`, que recebe uma lista de listas de linhas correspondente ao texto (sem linhas em branco) dos capítulos de um sermão e retorna uma lista de capítulos como descrito em cima.
