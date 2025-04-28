# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas seguintes linguagens: Python, JavaScript, TypeScript e Java.

Você deve submeter via Moodle apenas o link do seu `fork`, conforme descrito abaixo.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
pip install gitevo
```

Rode a ferramenta no repositório selecionado através do seguinte comando (dependendo da linguagem do projeto que escolheu):

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r js <git_url>

# TypeScript
$ gitevo -r ts <git_url>

# Java
$ gitevo -r java <git_url>
```

Onde `<git_url>` é URL do repositório a ser analisado.
Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

# Passo 3: Explorar os gráficos de evolução de código (`index.html`)

Ao rodar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), o arquivo `index.html` é gerado com diversos gráficos de evolução de código.

Abra o arquivo `index.html` e observe com atenção os gráficos gerados.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo, 
- Detalhar se as curvas estão de acordo com boas práticas,
- Explicar grandes alterações nas curvas,
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- Etc.

Seja criativo!

# Exercício

Para responder este exercício, primeiramente, você deve fazer um `fork` deste repositório.
No Moodle, você deve submeter apenas a URL do seu `fork`.

Em seguida, adicione o arquivo gerado `index.html` no seu fork.

Por fim, responda as questões abaixo no seu `fork`: 

1. Repositório selecionado: https://github.com/microsoft/vscode

2. Gráfico selecionado: Lines of Code (LOC)

3. Explicação:

Ao observar o gráfico "Lines of Code (LOC)", vemos um crescimento consistente na quantidade de linhas de código do projeto VS Code entre 2020 e 2025. 
O projeto sai de cerca de 711 mil linhas em 2020 para mais de 1,66 milhão em 2025, praticamente dobrando de tamanho nesse intervalo.

Algo que chama bastante atenção é o salto expressivo entre 2024 e 2025: o projeto cresce em mais de 370 mil linhas de código nesse único ano. 
Isso é um aumento muito maior que o observado nos anos anteriores, onde o crescimento anual era em torno de 130 mil linhas.

Para entender melhor o que pode ter acontecido, podemos olhar outros gráficos gerados:

- No gráfico de **TypeScript files**, o número de arquivos `.ts` também cresce bastante nesse mesmo período, de 4580 para 5204 arquivos, indicando que muitos novos módulos foram adicionados.
- No gráfico de **Classes, Interfaces e Type Aliases**, vemos aumento significativo nas três categorias, especialmente em `class_declaration` e `interface_declaration`, o que sugere que o crescimento foi estruturado com novas definições de tipos e padrões de projeto.
- O gráfico de **Functions** mostra que tanto o número de métodos (`method_definition`) quanto de funções do tipo `arrow_function` aumentaram bastante em 2025.
- E o gráfico de **Comments** (comentários no código) também apresenta um crescimento proporcional, indicando que essa nova quantidade de código manteve a preocupação com documentação interna.

Essa expansão no código também foi perceptível na prática. Como usuário do VS Code nesses anos, pude notar a adição de várias novas funcionalidades, como a integração com o GitHub Copilot e melhorias significativas no sistema de sugestões automáticas de código. Especialmente entre 2024 e 2025, o recurso de autocomplete ficou muito mais inteligente e rápido.

Esses padrões sugerem que, entre 2024 e 2025, o VS Code passou por uma grande expansão de funcionalidades e refatorações internas, o que refletiu não só no volume de código, mas também em melhorias concretas na experiência dos desenvolvedores.

Ainda vale ressaltar que o aumento de linhas de código em 2025 não parece ser um crescimento desorganizado, mas sim uma expansão planejada e bem estruturada do projeto.
