# Corpus de Discursos Presidenciais Brasileiros

## Sobre o corpus

Este repositório disponibiliza um **corpus de discursos presidenciais brasileiros**, compilado para fins de pesquisa em **Linguística de Corpus**, especialmente para investigações sobre o discurso político e presidencial brasileiro.

O corpus reúne discursos proferidos por **Luiz Inácio Lula da Silva, Dilma Rousseff e Jair Bolsonaro**, contemplando o primeiro ano do primeiro e do segundo mandatos de Lula e Dilma e o primeiro ano do mandato de Bolsonaro.

A compilação foi realizada no âmbito da pesquisa **“Análise Linguística de Discursos Presidenciais: Um Estudo Baseado em Corpus”**, que combina procedimentos quantitativos da Linguística de Corpus com uma abordagem qualitativa de **Análise Crítica do Discurso**.

O corpus foi organizado de modo a possibilitar diferentes tipos de investigação linguística, incluindo estudos de frequência lexical, palavras-chave, colocação, concordância e análise discursiva.

---

## Objetivo

O corpus foi compilado com o objetivo de fornecer dados linguísticos para a análise de discursos presidenciais brasileiros, permitindo a identificação de padrões lexicais e discursivos associados aos diferentes períodos presidenciais.

Na pesquisa que deu origem ao corpus, foram selecionadas como palavras de interesse:

* **Brasil**
* **Deus**
* **governo**

A escolha dessas palavras possibilitou investigar como diferentes elementos relacionados à identidade nacional, à religiosidade e à atuação governamental são mobilizados nos discursos presidenciais.

O corpus, entretanto, não se limita a essas três palavras e pode ser utilizado em outras pesquisas linguísticas.

---

## Composição do corpus

O corpus é composto por **1.001 discursos**, totalizando aproximadamente **1,6 milhão de tokens**.

A compilação contempla cinco subcorpora:

| Subcorpus | Presidente                |  Ano | Nº de textos |  Nº de tokens | Média de tokens por texto |
| --------- | ------------------------- | ---: | -----------: | ------------: | ------------------------: |
| **L1**    | Luiz Inácio Lula da Silva | 2003 |          207 |       368.918 |                  1.782,21 |
| **L2**    | Luiz Inácio Lula da Silva | 2007 |          240 |       479.349 |                  1.997,28 |
| **D1**    | Dilma Rousseff            | 2011 |          175 |       267.293 |                  1.527,38 |
| **D2**    | Dilma Rousseff            | 2015 |          182 |       253.202 |                  1.391,21 |
| **B1**    | Jair Bolsonaro            | 2019 |          197 |       167.476 |                    850,13 |
| **Total** | —                         |    — |    **1.001** | **1.612.181** |                         — |

O corpus apresenta aproximadamente **35.293 types**.

Devido às diferenças de extensão entre os subcorpora, comparações quantitativas devem considerar, preferencialmente, **proporções e frequências normalizadas**, e não apenas frequências absolutas.

---

## Presidentes e períodos contemplados

### Luiz Inácio Lula da Silva

Foram selecionados discursos correspondentes ao:

* **primeiro ano do primeiro mandato — 2003 (L1);**
* **primeiro ano do segundo mandato — 2007 (L2).**

### Dilma Rousseff

Foram selecionados discursos correspondentes ao:

* **primeiro ano do primeiro mandato — 2011 (D1);**
* **primeiro ano do segundo mandato — 2015 (D2).**

### Jair Bolsonaro

Foi selecionado o:

* **primeiro ano do primeiro mandato — 2019 (B1).**

A seleção foi realizada dessa maneira porque Bolsonaro não possuía, no recorte da pesquisa, um segundo mandato que pudesse ser utilizado para comparação.

Por essa razão, a análise principal da pesquisa concentrou-se nos subcorpora **L1, D1 e B1**, correspondentes ao primeiro ano do primeiro mandato de cada presidente.

---

## Critérios de seleção

Foram considerados discursos oficiais dos presidentes selecionados, de acordo com o recorte temporal estabelecido para a pesquisa.

Foram excluídos:

* discursos proferidos pelos respectivos vice-presidentes;
* discursos correspondentes ao período do governo Michel Temer;
* materiais que não se enquadrassem no recorte estabelecido para a composição do corpus.

A fonte utilizada para a coleta dos discursos foi a **Biblioteca da Presidência da República**, especificamente as páginas destinadas aos discursos presidenciais dos respectivos presidentes.

---

## Fonte dos dados

Os textos foram coletados a partir da **Biblioteca da Presidência da República**.

Os procedimentos de coleta variaram de acordo com o formato originalmente disponibilizado:

* os discursos de **Dilma Rousseff** e **Jair Bolsonaro** foram copiados das páginas da Biblioteca da Presidência e posteriormente salvos em arquivos `.txt`;
* os discursos de **Luiz Inácio Lula da Silva**, disponibilizados em PDF, passaram por conversão para arquivos de texto antes da etapa de tratamento.

Os arquivos foram posteriormente convertidos e/ou salvos em **UTF-8**, garantindo compatibilidade com as ferramentas utilizadas para a análise linguística.

---

## Organização e identificação dos arquivos

Os arquivos foram nomeados utilizando uma convenção baseada em:

**inicial do presidente + número do mandato + data + identificador do discurso**

Essa organização permite identificar o presidente, o período presidencial e a data correspondente a cada texto.

Os subcorpora são organizados da seguinte maneira:

```text
L1 = Lula — primeiro mandato — 2003
L2 = Lula — segundo mandato — 2007
D1 = Dilma — primeiro mandato — 2011
D2 = Dilma — segundo mandato — 2015
B1 = Bolsonaro — primeiro mandato — 2019
```

---

## Tratamento dos textos

Após a coleta, os textos passaram por procedimentos de limpeza e preparação para análise linguística.

Entre os procedimentos realizados estão:

* remoção de quebras de linha;
* remoção de aspas;
* tratamento de informações inseridas entre colchetes;
* padronização dos arquivos em formato `.txt`;
* codificação em **UTF-8**;
* inserção de informações de identificação e metadados;
* segmentação das saudações iniciais e finais.

As informações inseridas entre colchetes foram removidas quando consideradas elementos acessórios do texto, como em:

```text
Universidade [Federal] de Minas Gerais
```

O tratamento buscou produzir arquivos mais adequados à análise automática e semiautomática em ferramentas de Linguística de Corpus.

---

## Metadados

Os textos receberam marcações específicas para a identificação de informações relevantes.

Foram utilizados os seguintes campos:

```text
<nome>
<ocasião>
<local>
<cidade>
<data>
```

Essas marcações permitem recuperar informações contextuais dos discursos e podem ser utilizadas em análises que considerem variáveis relacionadas à situação comunicativa.

---

## Saudações iniciais e finais

As saudações presentes nos discursos foram segmentadas por meio das marcações:

```text
<sinicial>
<sfinal>
```

A separação foi realizada porque as saudações iniciais e finais apresentam elevado grau de padronização e podem constituir objetos específicos de investigação.

A segmentação permite, por exemplo, realizar análises separadas entre:

* corpo principal do discurso;
* saudação inicial;
* saudação final.

---

## Estrutura dos arquivos

Os textos do corpus são disponibilizados em formato:

```text
.txt
```

com codificação:

```text
UTF-8
```

O repositório também disponibiliza arquivos compactados correspondentes aos subcorpora e ao corpus tratado.

Estrutura geral:

```text
Corpus_Discursos_presidenciais/
│
├── B1-20260909T184925Z-1-001.zip
├── D1-20260909T184931Z-1-001.zip
├── D2-20260909T184930Z-1-001.zip
├── L1-20260909T184934Z-1-001.zip
├── L2-20260909T184936Z-1-001.zip
├── corpus_utf8-20260909T184712Z-1-001.zip
└── README.md
```

---

## Ferramentas utilizadas

A preparação e a análise do corpus envolveram diferentes ferramentas.

### AntConc

O **AntConc** foi utilizado para a realização das principais análises quantitativas e exploratórias do corpus, incluindo:

* listas de frequência;
* listas de palavras-chave;
* linhas de concordância (KWIC);
* colocados;
* análise de ocorrências lexicais.

Foi utilizada a versão **4.2.4 (2024)** do programa.

### Outras ferramentas

O tratamento dos textos também envolveu procedimentos de conversão, edição e padronização dos arquivos antes de sua utilização no AntConc.

---

## Procedimentos de análise

Na pesquisa que deu origem ao corpus, foram produzidas:

1. listas de palavras dos subcorpora;
2. listas de palavras-chave;
3. listas de colocados;
4. linhas de concordância (KWIC).

O **Corpus Brasileiro** foi utilizado como corpus de referência para a geração das listas de palavras-chave.

Inicialmente, foram consideradas listas contendo até **5.000 ocorrências**.

Para a análise de colocação, foram selecionados os colocados situados nas posições **1 a 20**, considerando as limitações de tempo e o recorte estabelecido para a pesquisa.

As linhas de concordância também foram utilizadas para a análise qualitativa dos usos lexicais.

---

## Palavras analisadas na pesquisa original

A pesquisa concentrou sua análise em três itens lexicais:

```text
Brasil
Deus
governo
```

A análise das listas de frequência e de palavras-chave indicou a relevância de **Brasil** e **governo** em diferentes subcorpora, enquanto **Deus** apresentou destaque particularmente relacionado ao subcorpus de Jair Bolsonaro.

Esses resultados constituíram o ponto de partida para uma análise discursiva mais aprofundada.

---

## Fundamentação teórica

O corpus foi elaborado a partir dos pressupostos da **Linguística de Corpus**, entendida tanto como abordagem metodológica quanto como perspectiva para o estudo da linguagem.

A pesquisa dialoga especialmente com trabalhos de:

* Tony Berber Sardinha;
* Laurence Anthony;
* McEnery e Hardie;
* McEnery e Wilson;
* John Sinclair.

A análise discursiva articula os procedimentos quantitativos da Linguística de Corpus a uma perspectiva de **Análise Crítica do Discurso**, especialmente a partir das contribuições de:

* **Norman Fairclough**;
* **Ruth Wodak**.

Essa articulação permite relacionar padrões quantitativos identificados no corpus a interpretações sobre os discursos presidenciais e seus contextos de produção.

---

## Possibilidades de pesquisa

Embora o corpus tenha sido originalmente compilado para investigar **Brasil**, **Deus** e **governo**, seus dados podem ser utilizados em diversas outras pesquisas.

Entre as possibilidades estão:

* análise de frequência lexical;
* análise de palavras-chave;
* análise de colocação;
* análise de concordâncias;
* estudos de vocabulário político;
* comparação entre presidentes;
* comparação entre mandatos;
* comparação entre períodos históricos;
* análise de representações discursivas;
* estudos de identidade nacional;
* estudos sobre religião e política;
* estudos sobre governo e poder;
* análise crítica do discurso político;
* estudos diacrônicos do discurso presidencial;
* investigação de padrões lexicogramaticais.

O corpus também pode servir como base para trabalhos de graduação, iniciação científica, mestrado, doutorado e outras pesquisas acadêmicas.

---

## Limitações e cuidados metodológicos

O corpus foi construído especificamente a partir de um recorte temporal e político definido pela pesquisa que o originou.

Assim, os dados **não representam todos os discursos produzidos pelos presidentes** nem todos os períodos de seus governos.

Além disso:

* os subcorpora apresentam extensões diferentes;
* Bolsonaro está representado apenas pelo primeiro ano de seu primeiro mandato no recorte original;
* a quantidade de discursos varia entre os presidentes;
* diferenças de extensão devem ser consideradas nas comparações quantitativas;
* as saudações iniciais e finais foram separadas do restante do discurso;
* as aspas foram removidas durante o tratamento dos textos;
* informações entre colchetes foram removidas em determinadas etapas de limpeza.

Por isso, pesquisadores que utilizarem o corpus devem considerar suas características de compilação e tratamento ao definir seus procedimentos metodológicos.

---

## Reprodutibilidade

Sempre que possível, recomenda-se que pesquisas realizadas com este corpus informem:

* versão do corpus utilizada;
* subcorpus analisado;
* ferramenta utilizada;
* versão da ferramenta;
* parâmetros de análise;
* corpus de referência utilizado;
* procedimentos de normalização;
* critérios de seleção das ocorrências;
* data de acesso aos arquivos.

Essas informações contribuem para a transparência e a replicabilidade das pesquisas realizadas a partir do corpus.

---


## Disponibilidade

O corpus é disponibilizado publicamente neste repositório:

**GitHub — Corpus de Discursos Presidenciais Brasileiros**

https://github.com/IsisBeber/Corpus_Discursos_presidenciais

Os arquivos podem ser utilizados para fins de pesquisa acadêmica, desde que sua origem seja devidamente indicada.

---

## Como citar

Ao utilizar este corpus em trabalhos acadêmicos, recomenda-se citar os responsáveis pela compilação e indicar o repositório utilizado.

### Referência

**FIORILO, Ísis; ROCHA, Bruno. Corpus de discursos presidenciais brasileiros. GitHub, 2024. Disponível em: https://github.com/IsisBeber/Corpus_Discursos_presidenciais. Acesso em: [data de acesso].**

### Citação no texto

Forma parentética:

> (FIORILO; ROCHA, 2024)

Forma narrativa:

> Fiorilo e Rocha (2024)

---

## Referências fundamentais

ANTHONY, Laurence. *AntConc: versão 4.2.4* [computador: programa]. Tóquio: Waseda University, 2024.

BERBER SARDINHA, Tony. *Linguística de Corpus*. Barueri, SP: Manole, 2004.

BERBER SARDINHA, Tony. Linguística de Corpus: histórico e problemática. *D.E.L.T.A.*, v. 16, n. 2, p. 323-367, 2000.

BERBER SARDINHA, Tony. *Pesquisa em Linguística de Corpus com WordSmith Tools*. Campinas: Mercado de Letras, 2009.

FAIRCLOUGH, Norman. *Discurso e mudança social*. Brasília: Editora Universidade de Brasília, 2001.

MCENERY, Tony; HARDIE, Andrew. *Corpus Linguistics: Method, Theory and Practice*. Cambridge: Cambridge University Press, 2012.

MCENERY, Tony; WILSON, Andrew. *Corpus Linguistics*. 2. ed. Edinburgh: Edinburgh University Press, 1996.

SINCLAIR, John. *Corpus, Concordance, Collocation*. Oxford: Oxford University Press, 1991.

WODAK, Ruth. The discourse-historical approach. In: WODAK, Ruth; MEYER, Michael (ed.). *Methods of Critical Discourse Analysis*. London: Sage, 2001.

WODAK, Ruth. *The Discourse-Historical Approach*. In: WODAK, Ruth; MEYER, Michael (ed.). *Methods of Critical Discourse Studies*. 3. ed. London: Sage, 2015.

---

## Autoria

**Ísis Beber de Souza Fiorilo Rocha**
**Bruno Neves Rati de Melo Rocha**

Corpus desenvolvido no âmbito de pesquisa em **Linguística de Corpus**.

---

## Licença e uso

Este repositório é disponibilizado para **fins acadêmicos e de pesquisa**.

Ao reutilizar os dados, recomenda-se:

1. citar adequadamente o corpus;
2. informar a versão utilizada;
3. indicar o repositório de origem;
4. mencionar eventuais modificações realizadas nos arquivos;
5. respeitar as condições de uso das fontes originais dos discursos.

---

## Palavras-chave

**Linguística de Corpus · Corpus Linguistics · Discursos presidenciais · Discurso político · Análise Crítica do Discurso · Lula · Dilma Rousseff · Jair Bolsonaro · Corpus Brasileiro · Brasil · Deus · Governo**

---

## Contato

Para informações sobre o corpus, sua compilação ou utilização em pesquisas acadêmicas, consulte os responsáveis pelo projeto por meio do repositório.

---

### Versão do corpus

**Versão:** 1.0
**Ano:** 2024
**Repositório:** `IsisBeber/Corpus_Discursos_presidenciais`
