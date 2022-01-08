# LaTeX

Criado no final da década de setenta por Donald Knuth, cientista da computação, o TEX consistia em um programa cujo objetivo era permitir alta qualidade de impressão de trabalhos. Rapidamente, o ambiente se popularizou entre profissionais da área, ganhando força na década de oitenta com a elaboração do sistema LaTeX por Leslie Lamport. Este consiste em um conjunto de comandos de alto nível que definem a formatação do texto de forma ampla e de fácil utilização.

## Benefícios 
1. Alta qualidade tipográfica e excelente estruturação de texto;
2. Ambiente matemático altamente superior;
3. Mudanças nas estruturas são ajustadas automáticamente;
4. Foco na estrutura lógica;
5. Geração de documento de forma profissinal;
6. Interface multiplataforma;
7. Software livre.

## Editores 
As distribuição mais comuns disponíveis são o MacTeX (Mac), MiKTeX (Windows) e TeXLive (multi-plataforma). Já os principais editores disponíveis podem ser vistos na Tabela abaixo:

|  Editor | Descrição |
| :----------: | :-----------: |
| LEd(LaTeX Editor) | *Software* livre apropriado para windows. Ambiente multilíngue possui corretor ortográfico, gratuito, mas não é *open source*. |
| Texmaker| Plataforma livre possui dicas descritivas e atalhos para geração de função aplicado em *linux*, *macosx* e *windows*. |
| TeXnicCenter | *Software Open source* , suporta vários arquivos pode ser utilizado nas plataformas *windows*, *Unix* e *macintosh*|
| WinEdt | Apropriado para *windows*, dicionário para vários idiomas e interface personalizada. Integrável para os sistemas *MikTeX* ou *LiveTeX*  |
|TeXstudio| Compatível com as plataformas *windows*, *Unix/linux* e *Mac OS X*, foi originado uma série de extensões para Texmaker tonando independente. |

## Copilador online

O compilador online sharelatex que permite utilizar todas as funcionalidades do LaTeX sem
a instalação de nenhum programa. É uma opção bastante acessível para a criação e edição de textos, além de permitir a edição colaborativa de um mesmo documento por um grupo de usuários. O sharelatex pode ser acessado pelo link [sharelatex](https://pt.sharelatex.com).

## Informações básicas acerca da linguagem 

A programação em LaTeX exige do usuário conhecimentos básicos sobre a línguagem e estruturação do código que são dividido em dois 

- Preâmbulo: Parte incial do código que são estabelicidos as pré-definições do documento ou classe.

>`% Preâmbulo`

>`%Possibilidade de adicionar pacotes e definições`

- Corpo do documento: Essa parte começa logo após o preâmbulo com o comando:

>`\begin {document}`
   
e  todos os textos que estarão no documento , assim como alguns comandos de definição. Para finalizar o documento utilizamos o comando:

>`\end{document}`
    
Exemplo: 
```
%preâmbulo
%Adicionar pacotes e definições
%exemplos de pacotes 
\documentoclass[a4,twoside]{book}
\usepackage[latin1]{inputenc}
\usepackage[brazil]{label}
\usepackage{graphicx}

% Corpo do documento

\begin{document}

% Pode digitar o documento aqui

\chapter{conceitos básicos}
\section{\latex}
    
texto da seção \LaTeX[...]

end{document}
```

<br/>

# Ambiente matemático 

## Conceitos básicos 

O LaTeX possui um ambiente especifíco para utilização de liguagem matemática dentro do texto, de forma a digitar sinais e fórmulas sem o uso desse espaço ocasiona erros detectados pelo compilador.
    
O ambiente matématico pode ser inciados de várias formas mais como é a utilização do
    
>`$` 
    
delimitando a linguagem, sendo as fórmulas inseridas dentro do texto.

A fórmula apareça centralizada usa-se dois

>`$$`
    
inicializando e concluindo o ambiente. Outra opção é o uso do ambiente `math`.
    
Exemplo:

Fórmula dentro do texto:

`$x^2+y^2=16$`

> ![test](https://latex.codecogs.com/gif.latex?x%5E2&plus;y%5E2%3D16)




Fórmula Centalizada:

`$$ x^2 + y^2 =16 $$`
>$$ x^2 + y^2 =16 $$

Fórmula usando o ambiente **math**:
```
\begin{math}
x^2 + y^2 = 16
\end{math}
```
## Texto no ambiente matemático

Ao utilizar o ambiente matemático, os  caracteres de texto serão considerados como variáveis agrupadas,de forma que os espaços entre elas não serão determinados na visualização.
    
Exemplo:

>Trechodentrodoambiente
    
Assim, a inserção de texto dentro do ambiente matemático se dá através dos comandos 
     
>`\mbox{texto}` e `\mathrm{texto}`

Exemplo: 
```
$y = x, \mbox{se} \; x>0 $
$dW_{\mathrm{saida mecanica}}=
dW_{\mathrm{entrada eletrica}} - dW_{\mbox{energia magnetica}} $
  
```

Resultado:

>y = x,se x > 0

>dWsaidamecanica = dWentradaeletrica − dWenergia magnetica`
## Equações 

Neste caso pode ser usada a equação `\ref{apelido}:`
```
\begin{equation}
\Psi= \int_S (x^6 + 4y^5)ds
\label{apelido}
\end{equation}´
```
Resultado

<!---------$ \Psi= \int_S (x^6 + 4y^5)ds $---->

![equação](https://latex.codecogs.com/gif.latex?%5CPsi%3D%20%5Cint_S%20%28x%5E6%20&plus;%204y%5E5%29ds)

## Eqnarray

No caso de equações que se estendem por várias linhas, ou demonstrações de fórmulas cujo apenas o resultado precisa ser numerado, pode-se utilizar o ambiente eqnarray.

Exemplo:
```
\begin{eqnarray}
x + y + z & = & 10 \\
x+y & = & 5 \nonumber \\
4x + 8y + z & = & 0
\end{eqnarray}
```
Resultado 
>x + y + z = 10 

>x + y = 5

>4x + 8y + z = 0

## Frações

Frações são construídas com o comando `\frac{numerador}{denominador}` dentro do ambiente matemático. A barra também pode ser utilizada para reproduzir uma fracão, mas com resultado diferente.

## Raízes 

A inclusão de raiz quadrada se dá a partir de `\sqrt{radicando}`. No caso de uma raiz enésima, utiliza-se `\sqrt[n]{radicando}`.

Exemplo:
```
$ \frac{x}{2} + x^2 = 10 $\\
$ x/2 + x^2 = 10 $\\
$\sqrt{x^2 + 2x +4} = 8$ \\
$\sqrt[3]{ax^2 + bx + c} = r$ \\
$\sqrt[\frac{3}{2}]{4x^3 + y^2 + z^4} = r$
```
Resultado:

<!-------$ \frac{x}{2} + x^2 = 10 $----->

![fracao](https://latex.codecogs.com/gif.latex?%5Cfrac%7Bx%7D%7B2%7D%20&plus;%20x%5E2%20%3D%2010)

<!-------------$ x/2 + x^2 = 10 $------->

![fracao](https://latex.codecogs.com/gif.latex?x/2%20&plus;%20x%5E2%20%3D%2010)

<!----------$ \sqrt{x^2 + 2x +4} = 8 $------->

![raiz](https://latex.codecogs.com/gif.latex?%5Csqrt%7Bx%5E2%20&plus;%202x%20&plus;4%7D%20%3D%208)

<!------$ \sqrt[3]{ax^2 + bx + c} = r $----->

![raiz](https://latex.codecogs.com/gif.latex?%5Csqrt%5B3%5D%7Bax%5E2%20&plus;%20bx%20&plus;%20c%7D%20%3D%20r)

<!----$ \sqrt[\frac{3}{2}]{4x^3 + y^2 + z^4} = r $--->

![raiz](https://latex.codecogs.com/gif.latex?%5Csqrt%5B%5Cfrac%7B3%7D%7B2%7D%5D%7B4x%5E3%20&plus;%20y%5E2%20&plus;%20z%5E4%7D%20%3D%20r)

## Expoentes e Índices 

Expoentes são definidos utilizando o sinal de circunflexo entre a base e o expoente. No caso do expoente ser uma expressão, deve-se limitá-lo por chaves para identificar a base a qual ele pertence. Já os índices são definidos a partir de um underline, separando a base e o índice. Este segue a mesma regra dos expoentes, no caso de um índice longo. Os dois recursos podem ser combinados na mesma base, e neste caso, o uso das
chaves é obrigatório mesmo para índices e expoentes simples.

Exemplo:

```
$e^{x^2} = 2$ \\
$ x_{1}^{5} + x_{2}^{2} = 9$
```
Resultado:

<!---$ e^{x^2} = 2 $--->

![expo](https://latex.codecogs.com/gif.latex?e%5E%7Bx%5E2%7D%20%3D%202)

<!--$ x_{1}^{5} + x_{2}^{2} = 9 $---->

![expo](https://latex.codecogs.com/gif.latex?x_%7B1%7D%5E%7B5%7D%20&plus;%20x_%7B2%7D%5E%7B2%7D%20%3D%209)

## Funções

A maioria das funcões matemáticas já está  definida no LaTeX e pode ser utilizada por meio de comandos como os apresentados na Tabela
|  Comando | Função |
| :----------: | :-----------: |
|\cos|Cosseno|
|\sin|Seno|
|\tan|Tangente|
|\log|Logarítimica|
|\exp|Exponencial|
|\arcos|Arco cosseno|
|\ln|Logarítmico natural|
|\sec|Secante|

## Limites 

Limites são inseridos utilizando a sintaxe `\lim_{vari´avel \to limite}` função.

Exemplo:
```
$\lim_{x \to x_0 } f(x)$ \\
$ \lim_{x \to \infty} \frac{1}{x} = 
```
Resultado:

<!--$ \lim_{x \to x_0 } f(x) $-->

![lim](https://latex.codecogs.com/gif.latex?%5Clim_%7Bx%20%5Cto%20x_0%20%7D%20f%28x%29)

<!---$ \lim_{x \to \infty} \frac{1}{x} = 0$--->

![lim](https://latex.codecogs.com/gif.latex?%5Clim_%7Bx%20%5Cto%20%5Cinfty%7D%20%5Cfrac%7B1%7D%7Bx%7D%20%3D%200)

## Derivadas

Derivadas podem ser construídas da mesma forma das fracões, por meio do comando `\frac{numerador}{denominador}`,ou usando apóstrofos.
Para derivadas parciais, utiliza-se o comando `\partial{}` para incluir o símbolo *derrô*.

Exemplo:
```
$$ V_{\mathrm{valor médio}} = \frac{df}{dx}=\frac{e^{2x}}{sinx}$$
$$f’(x)= \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}$$
$$ f_x = \frac{\partial{f(x,y)}}{\partial{x}}$$
```
Resultado:

<!--$$ V_{\mathrm{valor médio}} = \frac{df}{dx}=\frac{e^{2x}}{sinx}$$-->

![derivada](https://latex.codecogs.com/gif.latex?V_%7B%5Cmathrm%7Bvm%7D%7D%20%3D%20%5Cfrac%7Bdf%7D%7Bdx%7D%3D%5Cfrac%7Be%5E%7B2x%7D%7D%7Bsinx%7D)

<!--$$f’(x)= \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}$$--->

![derivada](https://latex.codecogs.com/gif.latex?f%27%28x%29%3D%20%5Clim_%7Bh%20%5Cto%200%7D%20%5Cfrac%7Bf%28x&plus;h%29-f%28x%29%7D%7Bh%7D)

<!--$$ f_x = \frac{\partial{f(x,y)}}{\partial{x}}$$-->

![derivada](https://latex.codecogs.com/gif.latex?f_x%20%3D%20%5Cfrac%7B%5Cpartial%7Bf%28x%2Cy%29%7D%7D%7B%5Cpartial%7Bx%7D%7D)

## Integrais

A inserção de integrais ocorre por intermédio do comando `\int_{inicio do intervalo}^{fim do inter
valo}`. 
Integrais duplas e triplas podem ser feitas com comandos `\int` consecutivos ou `\!`, para diminuir o espaço entre os símbolos das integrais. Integrais de contorno são produzidas usando `\oint`.

Exemplo:
```
$\oint_S \vec{A} d \vec{S}=
\int \! \! \int \! \! \int_V (\vec \nabla. \vec A)dv$
```
Resultado:
<!--$\oint_S \vec{A} d \vec{S}=
\int \! \! \int \! \! \int_V (\vec \nabla. \vec A)dv$-->

![integral](https://latex.codecogs.com/gif.latex?%5Coint_S%20%5Cvec%7BA%7D%20d%20%5Cvec%7BS%7D%3D%20%5Cint%20%5C%21%20%5C%21%20%5Cint%20%5C%21%20%5C%21%20%5Cint_V%20%28%5Cvec%20%5Cnabla.%20%5Cvec%20A%29dv)

## Somatório e Produtório 

Somatórios e produtórios usam a seguinte sintaxe:

```
$\vec F=\frac{1}{4\pi \varepsilon_0}. Q . \sum_{k=1}^{N}
\frac{Q_n}{|\vec r-\vec r_k|^3}(|\vec r-\vec r_k|)$
```
Resultado:
<!--$\vec F=\frac{1}{4\pi \varepsilon_0}. Q . \sum_{k=1}^{N}
\frac{Q_n}{|\vec r-\vec r_k|^3}(|\vec r-\vec r_k|)$-->

![somatorio](https://latex.codecogs.com/gif.latex?%5Cvec%20F%3D%5Cfrac%7B1%7D%7B4%5Cpi%20%5Cvarepsilon_0%7D.%20Q%20.%20%5Csum_%7Bk%3D1%7D%5E%7BN%7D%20%5Cfrac%7BQ_n%7D%7B%7C%5Cvec%20r-%5Cvec%20r_k%7C%5E3%7D%28%7C%5Cvec%20r-%5Cvec%20r_k%7C%29)

## Vetores

Vetores podem ser inseridos a partir do comando `\vec{vetor}` ou usando `\overrightarrow{vetor}`,
sendo a primeira opção mais apropriada. 

Exemplo:

```
$\overrightarrow{\nabla}=\frac{\partial}{\partial x}(\vec{i})+
\frac{\partial}{\partial y}(\vec{j})+\frac{\partial}{\partial z}
(\vec{k})$
```
Resultado:

<!--$\overrightarrow{\nabla}=\frac{\partial}{\partial x}(\vec{i})+
\frac{\partial}{\partial y}(\vec{j})+\frac{\partial}{\partial z}
(\vec{k})$-->

![vector](https://latex.codecogs.com/gif.latex?%5Coverrightarrow%7B%5Cnabla%7D%3D%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20x%7D%28%5Cvec%7Bi%7D%29&plus;%20%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20y%7D%28%5Cvec%7Bj%7D%29&plus;%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20z%7D%20%28%5Cvec%7Bk%7D%29)

## Matrizes

15 Matrizes
Matrizes são definidas em um ambiente array similar ao ambiente tabular, usado na construção de tabelas. Após o início do ambiente, deve-se definir o alinhamento dos elementos de cada linha, usando r para alinhar a direita, l para esquerda e c para centralizar.

Exemplo:

```
$
\textrm{rot} \, \vec A = \left|
\begin{array}{ccc}
\vec i & \vec j & \vec k \\
\frac{\partial}{\partial x} &
\frac{\partial}{\partial y} &
\frac{\partial}{\partial z} \\
A_x & A_y & A_z \\
\end{array}
\right|
$
```
Resultado:

<!--$
\textrm{rot} \, \vec A = \left|
\begin{array}{ccc}
\vec i & \vec j & \vec k \\
\frac{\partial}{\partial x} &
\frac{\partial}{\partial y} &
\frac{\partial}{\partial z} \\
A_x & A_y & A_z \\
\end{array}
\right|
$ -->

![matriz](https://latex.codecogs.com/gif.latex?%5Ctextrm%7Brot%7D%20%5C%2C%20%5Cvec%20A%20%3D%20%5Cleft%7C%20%5Cbegin%7Barray%7D%7Bccc%7D%20%5Cvec%20i%20%26%20%5Cvec%20j%20%26%20%5Cvec%20k%20%5C%5C%20%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20x%7D%20%26%20%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20y%7D%20%26%20%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%20z%7D%20%5C%5C%20A_x%20%26%20A_y%20%26%20A_z%20%5C%5C%20%5Cend%7Barray%7D%20%5Cright%7C)

## Tensores

Tensores podem ser criados utilizando dois símbolos barra(||), internamente ao ambiente matemático.

Exemplo:
```
$$
\vec{B}=|| \mu || \vec{H}
$$
```
Resultado:

<!--$$
\vec{B}=|| \mu || \vec{H}
$$-->

![tensores](https://latex.codecogs.com/gif.latex?%5Cvec%7BB%7D%3D%7C%7C%20%5Cmu%20%7C%7C%20%5Cvec%7BH%7D)

## Letras Gregas

O uso de letras gregas e fórrmulas ocorre mediante emprego de comandos que geralmente seguem o nome da letra

|  Comando | Resultado |
| :----------: | :-----------: |
|\alfa|α|
|\delta|δ|
|\pi|π|
|\rho|ρ|
|\teta|θ|

<!------- Alterar-------->

# Documentos de Texto

<br/>


No inicio de um documento Latex é necessario informar ao compilador o tipo de ducumento que será escrito bem como informações sobre sua formatação

Isso é feito por meio do comando:

```Latex
\documentclass[opção_1, opção_2, ..., opção_n]{classe}

```

Em relação as opções descritas no camandos acima, temos augumas delas apresentadas na tabela abaixo:

<br/>

| 11pt, 12pt,...       | Tamanho da fonte                        |
|----------------------|-----------------------------------------|
| onecolumn, twocolumn | Número de colunas                       |
| oneside, twoside     | Impressão em um ou dois lados da página |
| a4, letterpaper      | Tamanho da folha                        |

<br/>
<br/>

## classes de ducumentos

<br/>

Em latex os tipos de documentos são tipicamente chamados de `classes`, Abaixo podemos ver as principais classes de ducumentos existetes:

| report  | Relatórios                   |
|---------|------------------------------|
| book    | Livros e Apostilas           |
| beamer  | Slides                       |
| article | Artigo e documentos pequenos |

Alem dessas temos outras classes de documentos, entre elas temos a classe ABNT, que permite que o ducumento siga as normas sem a necessidade que o usuario  as conheça, podemos obtela por meio do link a seguir:

<br/>

[ABNT CLASS](http://www.abntex.net.br/)

<!------- especificar a utilização dessa classe----->

<br/>
<br/>

## ESTILOS DE PAGINAS

<br/>

No latex é possivel definir imformaçõs fixas para o cabeçalho e rodapé da pagina. Alem disso é possivel definir o tipo de numeração de pagina que será aplicada no documento. 

Para alterar o estilo de pagina utilizamos o seguinte comando:

```Latex
\pagestyle{estilo}
```

O comando descrito acima deve ser inserido no preâmbulo

<br/>

Para alterarr o estilo de um pagina especifica utilizamos o comando

```Latex
\thispagestyle
```

Caso não haja nehum estilo definido, o latex define o estilo de pagina como `defaut`, Na tabela abaixo temos augums estilos comportado pelo Latex:

<br/>

| plain    | Apenas o número da página(estilo de numeração romanos) no rodapé. Estilo default.              |
|:----------:| :------------------------------------------------------------------------------------------------: |
| empty    | Cabeçalho e rodapé vazios.                                                                     |
| headings | Número da página e informações especı́ficas, porém a formatação depende da classe do documento. |
| fancy    | Estilos de páginas personali- zados. Necessita do pacote fancyhdr                              |

<br/>
<br/>

Em latex temos a existencia de estilos de numeração de página, algums desses estilos podem ser vistos na tabela abaixo:

| arabic | algarismos arábicos                                           |
|--------|---------------------------------------------------------------|
| roman  | romanos                                                       |
| Roman  | Romanos maiúsculos (Perceba que a primeira letra é maiúscula) |
| alph   | letras minusculas                                             |
| Alph   | Letras maiúsculas(Perceba que a primeira letra é maiúscula)   |

<br/>

O estilo de numeração de paginas é alterado utilizando o comando a seguir:

```Latex
\pagenumbering{estilo}
```

Este comando tem de ser inserido no preâmbulo.


<br/>

<!-----------Adicionar titulo a essa seção------>

Ainda em Latex é possivel construir paginas personalizadas.
Para personalizar a estrutura do documento utilizamos o comando a seguir:

```Latex

\fancyhead[opções]{informações}

```

Já para personalizar o rodapé utilizamos o comando:

```Latex
\fancyfoot[ opções ]{informações}
```

<br/>
<br/>

Abaixo temos, uma tabela com as `opções` que estão descritas nos comandos acima:

| RO | canto direito em páginas ı́mpares  |
|----|-----------------------------------|
| CO | centro em páginas ı́mpares         |
| LO | canto esquerdo em páginas ı́mpares |
| RE | canto direito em páginas pares    |
| CE | centro em páginas pares           |
| LE | canto esquerdo em páginas pares   |


<br/>


Jã para as `informaçẽs`, temos a seguinte tabela:



| \rightmark | imprime o nome da seção na pagina desejada desejada  |
|------------|------------------------------------------------------|
| \leftmark  | imprime o nome do capitulo na pagina desejada        |

<br/>

Abaixo temos um exemplo da utilização desse comando:

```Latex
\fancyhead[RO]{\rightmark}

\fancyfoot[ LE ]{informações}
```

<BR/>
<br/>

## **PACOTES** 

Em Latex temos uma estrutura chamada Pacotes, essa estrutura é muito semelhante aos pacotes encontrados em outras linguagems de programação. Eles tem como objetivo adicionar uma nova função, que não é fornecida nativamente no Latex, a adição de pacotes é feita no preâmbulo do ducumento utilizando o comando:

```Latex
\usepackage[opções]{nome do pacote}
```
Podemos ver na tabela abaixo augums dos pacotes mais comumente usados:

| amsfonts    | Utilização de sı́mbolos matemáticos.                   |
|-------------|-------------------------------------------------------|
| babel       | Suporte para idiomas.                                 |
| color       | Utilização de cores.                                  |
| fancyhdr    | Criação de cabeçalhos e rodapés personalizados.       |
| graphicx    | Inclusão de figuras e gráficos.                       |
| hyperref    | Criação de hyperlinks.                                |
| inputenc    | Utilização de acentos na forma convencional.          |
| longtable   | Utilização de tabelas longas(maiores que uma página). |
| subeqnarray | Uso de equações em conjunto.                          |
| subfigure   | Inclusão de subfiguras.                               |


<br/>

## **ACENTUAÇÃO**

Para adicionarmos uma acentuação em Latex, temos a seguinte sintaxe, antes de cada letra acentuada adicionamos uma barra invertida é logo em seguida o acento e a letra, comforme vemos a seguir:

```Latex
\`a

\^a

\‘a

\~a
```

O código mostrado acima gera a seguinte saída:

```Latex
à

â

á

ã
```
<br/>

## **COMENTÁRIOS**

Comentários são informações utilizadas para documentar o código ou adicionar uma informação inportante em uma linha especifica. Comentarios não são visualizados no texto compilado, para adicionarmos um utilizamos o sinbolo `%`(porcentagem) e após ele digitamos a informação desejada, a seguir podemos ver um exemplo:

```Latex

\newpage %adiciona um nova pagina ao documento
% exemplo da utilização de comentários
```

A saída para essas linhas de codigo seria:

```Latex

\newpage 

```

Como pode ser observado, os comentários não são exibidos 




##  **Comandos/Caracteres especiais**

Comandos em LaTeX são feitos utilizando \ (barra invertida) seguida da identificação. Dessa forma, a
barra invertida é um comando próprio da linguagem, assim como os símbolos do exemplo 2.2
Todos esses símbolos, com exceção da barra invertida, são produzidos com o comando \Símbolo. A barra
pode ser visualizada no texto usando o camando $\backslash$, onde o $ se refere ao ambiente matemático,
que será explicado no próximo capítulo.

```Latex
\% \& \{ \} $\backslash$ \# \$

```

Temos a seguinte saída:

```Latex
% & { } \ # $
```

## **Capa do documento**

Para as classes report e book, pode-se gerar uma capa automática utilizando o comando \maketitle.
Esse recurso aproveita as informações disponibilizadas no preâmbulo, como nome do autor, título e data, intro-
duzidas a partir dos comandos \author{Nome do autor}, \title{Título do documento} e \date{Data}
ou \date{\today}, respectivamente. Caso exista mais de um autor na publicação, utiliza-se \and entre os
nomes destes.
O usuário também pode criar um estilo de capa a partir do ambiente titlepage e utilizar as opções de
fonte e alinhamento para gerar o resultado desejado. Esses conceitos podem ser visualizados a seguir:

```Latex
\documentclass[a4]{report} %Defini¸c~ao da classe e das op¸c~oes do documento (relat´orio, tamanho a4)
\usepackage[utf8]{inputenc} %Pacote ness´ario para a utiliza¸c~ao de acentos
\usepackage[brazil]{babel} %Utiliza¸c~ao do pacote babel
\usepackage{fancyhdr} %Pacote necess´ario para utilizar o estilo de p´agina fancy
\author{Thyago Monteiro} %Autor
\title{Introdu¸c~ao ao LaTeX} %T´ıtulo
\date{\today} %Data - a fun¸c~ao \today exibe a data corrente

\pagestyle{fancy} %Estilo da p´agina
\fancyhead[RO, RE]{\it \textbf{ Introdu¸c~ao ao \LaTeX }} %Edi¸c~ao do cabe¸calho - canto direito para p´aginas ´ımpares e pares
\fancyfoot[RO, RE]{Thyago S´a} %Edi¸c~ao do rodap´e - canto direito para p´aginas ´ımpares e pares
\pagenumbering{Roman} %Estilo da numera¸c~ao das p´aginas
\begin{document}
\begin{titlepage} %Capa feita manualmente
Universidade Federal de Campina Grande - UFCG \\
Departamento de Engenharia El´etrica - DEE \\
\vspace{6cm}
{\bf Aluno: Thyago Monteiro}
\end{titlepage}
\maketitle %Capa feita automaticamente pelo LaTex
\end{document}
```

## **Divisão do documento**

A divisão do documento é feita por intermédio dos comandos:

```Latex
\part*{T´ıtulo} ou \part{T´ıtulo}
\chapter*{T´ıtulo} ou \chapter{T´ıtulo}
\section*{T´ıtulo} ou \section{T´ıtulo}
\subsection*{T´ıtulo} ou \subsection{T´ıtulo}
\subsubsection*{T´ıtulo} ou \subsection{T´ıtulo}
```

O título se refere ao nome da divisão. O asterisco significa que o autor não deseja que a divisão seja
incluída no sumário nem seja numerada, sendo o título visualizado apenas no texto.
A inclusão do sumário é feita com o comando \tableofcontents. Este pode ser incluso logo no início
do documento, antes da primeira partiçipação e depois da capa do documento. Fazer uma divisão apropriada do
texto torna-se útil pois, conforme as partes forem sendo adicionadas, o sumário é atualizado automaticamente
de acordo com os títulos na sequência em que aparecem no texto. Por padrão, o código deve ser compilado
duas vezes para que as alterações no sumário sejam feitas.
Normalmente, os nomes das divisões aparecem no sumário do mesmo modo que no texto. Entretanto,
se um cabeçalho é muito longo para encaixar-se bem no sumário, pode-se providenciar uma versão reduzida
como um argumento opcional:

```Latex

\tableofcontents
\section[Cabeçalho reduzido]{Este é um cabe¸calho muito mais longo que aparecerá somente no
texto do documento}
\subsection*{Cabeçalho que não será visto no sumário}
```

## **Espaços, linhas e parágrafos**

O LATEX interpreta vários espaços em uma linha como apenas um único, de forma que não importa o
quão distantes estejam duas palavras, apenas um único espaço as separa na versão final. Para burlar esse
fato, costuma-se usar o comando \ \ (duas contra-barras separadas por um espaço) ou a forma simplificada
\hspace{largura do espa¸co}. Sendo a largura dada em cent´ımetros.
Vários espaços consecutivos na vertical são interpretados como uma indicação de novo parágrafo, porém
apenas um basta para essa finalidade ou o uso do comando \par. Para obter-se um determinado espaçamento
vertical pode-se usar \vspace{largura do espaço}.
Pode-se evitar a indentação de um parágrafo específico com o comando \noindent. Já para desabili-
tar a indentação para todo o documento, você pode usar \setlength{\parindent}{0pt}, que define uma
indentação nula. Esse comando também é útil em casos de se desejar definir a largura da indentação.
A declaração de nova linha ocorre com \\ (duas contra barras seguidas) ou utilizando \linebreak,
comandos que terminam mas não iniciam novos parágrafos. A inclusão de uma nova página pode ser feita
usando-se o comando \newpage.

Parte desses conceitos são apresentados a seguir


```Latex
Espaço \ \ Espaço \ \ \ \ \ Espaço \ \ \ \ \ \ \ \ \ \ Espaço \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ Espaço \\
Espaço \hspace{4cm} na horizontal!!!!
\vspace{2cm}
Espaço na vertical!!!!
\par Inicialização de parágrafo!
Inicialização de par´agrafo!
```

Temos a seguinte saída para o código mostrado acima:

```Latex
espaço espaço espaço espaço espaço
Espaço na horizontal!!!!




Espaço na vertical!!!!
Inicialização de parágrafo!
Inicialização de parágrafo!

```

## **Margens**

O LATEX estabelece recuos específicos para o texto, de acordo com o documento. Essa estrutura pode
ser alterada utilizando, no preâmbulo, o comando \setlength{objeto}{largura}, sendo objeto o item
que deseja-se fazer a altera¸cão, identificado com comandos específicos (Tabela 2.3). Já a largura pode ser
apresentada em centímetro (cm), polegadas (in = 2, 54cm) ou pontos (pt), inclusive em valores negativos, ou
seja, contrários aos ditados pelo editor.


Para alterar as margens manualmente utilizamos o seguintes códigos:

```Latex
\hoffset Largura da lateral esquerda
\voffset Largura da barra superior
\headheight Altura do espa¸co de cabe¸calho
\textheight Espa¸co ocupado pelo texto(Altura)
\textwidth Espa¸co ocupado pelo texto (Largura)
```

Para alterar as margens de todo o documento utilizamos os comandos (esses comandos devem ser inseridos no preâmbulo do arquivo):

```Latex
%adicionar ao preâmbulo do documento
\setlength{\hoffset}{-1cm}
\setlength{\voffset}{-1cm}
\setlength{\textheight}{24cm}
\setlength{\textwidth}{16cm}
```

## **Tipos de fontes**

O tipo de fonte default do LATEX é o Romano, porém, existem outros estilos que podem ser usados ao
longo do texto e est˜ao apresentados na Tabela a seguir:

<br/>

 | Comando | Resultado |
 |------------------|-------------------|
 | {\rm romano | romano |
 | \it itálico | itálico |
 | \sf San serif | San serif |
 
<br/>

<!---------------corrigir posteriormente 16-------------->

Outra opção é o comando `\text__{Texto}`, substituindo após a palavra text as duas letras correspondentes
ao estilo de fonte desejado. Para mudar o estilo de fonte do documento por completo, utiliza-se `\rmfamily` ou `\sffamily`, após o `\begin{document}`, alterando a fonte para Romano ou Sans Serif,respectivamente.

<br/>

## **Tamanhos**

O tamanho da fonte pode ser estabelecido entre as opções na definição do documento, ou alterado ao longo do texto a partir dos comandos mostrados a seguir:

<br/>

```latex
{\tiny PET-Elétrica}

{\scriptsize PET-Elétrica}

{\small PET-Elétrica}

{\normalsize PET-Elétrica}

{\large PET-Elétrica}

{\Large PET-Elétrica}

{\LARGE PET-Elétrica} 

{\huge PET-Elétrica} 

{\Huge PET-Elétrica}
```
<br/>

Temos o seguinte resultado para os códigos acima:

![resultadoFonteTamanho](https://static.wixstatic.com/media/1c667d_8e8880e1d439405ebfc533d1c141db83~mv2.png/v1/fill/w_468,h_481,al_c,q_85/1c667d_8e8880e1d439405ebfc533d1c141db83~mv2.webp)

<br/>
<br/>

## **Alinhamento**


O texto em LaTeX é justificado por default, de forma que para modificar esse alinhamento usa-se os
cómandos `center`, `flushright` e `flushleft`. Estes alinham o texto para o centro da página, para a direita ou
esquerda, respectivamente. A utilização desses recursos pode ser vista a seguir:


```Latex
\begin{center}
Texto centralizado!!!
\end{center}
```

```Latex
\begin{flushleft}
Texto alinhado a esquerda!!!!
\end{flushleft}
```


```Latex
\begin{flushright}
Texto alinhado a direita!!!!!
\end{flushright}
```

Temos os seguintes resultados para os comandos visulalizados acima:

![alinhamentoTexto](https://static.wixstatic.com/media/1c667d_413b23aab2034f11b25bf507ee60038d~mv2.png/v1/fill/w_600,h_116,al_c,q_85,usm_0.66_1.00_0.01/1c667d_413b23aab2034f11b25bf507ee60038d~mv2.webp)


<br/>
<br/>

## **Listas**

A construção de listas ocorre nos ambientes `itemize` e `enumerate`, sendo cada item adicionado com o
comando `\item`. A diferença entre os dois ambientes é que o segundo apresenta a lista numerada.
Estes espaços também permitem a criação de listas personalizadas, selecionando um sı́mbolo
entre colchetes após a adição de cada elemento.

A seguir temos os comandos para essas listas:

```Latex
\begin{itemize}
\item Primeiro item;
\item Segundo item;
\item[$\spadesuit$] item;
\end{itemize}
```
O código acima gera o seguinte resultado:

![itemize](https://static.wixstatic.com/media/1c667d_7bf925c6bc0a43df986f903124b3977f~mv2.png/v1/fill/w_384,h_197,al_c,q_85/1c667d_7bf925c6bc0a43df986f903124b3977f~mv2.webp)

<br/>
<br/>

```Latex
\begin{enumerate}
\item Primeiro item;
\item Segundo item;
\item[$\heartsuit$] item;
\end{enumerate}
```
O código acima gera o seguinte resultado:

![enumerate](https://static.wixstatic.com/media/1c667d_1d34e0c97532470eaae6408246865870~mv2.png/v1/fill/w_394,h_176,al_c,q_85/1c667d_1d34e0c97532470eaae6408246865870~mv2.webp)


# Classe Beamer

## Conceitos básicos

A classe de documetos *beamer* é mais utlizada para a criação de slides e apresentação de trabalhos. O início desse tipo de documento se dá na sua definição, atribuindo  *beamer* a classe em `documentclass[opções]{classe}`.
Após isso, é preciso delimitar o documento utilizando `\begin{document}` para o início do documento e `\end{document}` para o fim. Tudo que for digitado externamente a esse ambiente é ignorado na compilação.Os slides são definidos por intermédio de ambientes *frame* que podem ser iniciados de duas maneiras Os pacotes são definidos no preãmbulo, utilizando o comando
`\usepackage{pacote}`, sendo iguais aos de documentos de texto. Entre as opções de slide no modo completo, estão: plain, que omite o cabeçalho e o rodapé (usado geralmente na capa), e fragile, que mantem esses recursos. O alinhamento vertical também pode ser definido
entre os colchetes, utilizando c, t e b para alinhar o texto no centro, no topo ou na base do slide, respectivamente. O texto é centralizado por padrão. Para aplicar em todos os slides, marca-se a opcão desejada na
definição do documento como em `\documentclass[t]{beamer}`, por exemplo.

## Informações do documento

Em apresentações de slides, as informações definidas no preâmbulo do documento são de grande importância. Dependendo do tema utilizado, essas informações aparecerão em todas as partes da apresentação,além de gerarem uma capa automática com o comando `\maketitle`.

```Latex
\author[Abreviação]{Nome do autor}
\title[Abreviação]{Título da apresentação}
\date{Data ou \today}
\institute[Abreviação]{Instituição}
```
Exemplo:

```Latex

%Início de um slide
Início de um slide

\documentclass[xcolor=svgnames]{beamer}
%pacotes
\usepackage[utf8]{inputenc}
\usepackage[brazil]{babel}
\usepackage{graphicx}
\usepackage{color}
%informações do documento
\author{João Maria José}
\title{Trabalho de Conclus~ao de Curso}
\institute[UFCG]{ Departamento de Engenharia Eletrica \\
Universidade Federal de Campina Grande, Brasil \\
\texttt{joaojose@ee.ufcg.edu.br}
}
\date{\today}
\begin{document}
\begin{frame}
\maketitle
\end{frame}
\begin{frame}[plain]{Título do Slide}
Conteúdo do slide!!!
\end{frame}
\frame{
Conteúdo do slide!!!
}
\end{document}
```

O codígo mostrado acima gera a seguinte saída:

<div style="text-align:center"> </p> <!--Centraliza texto-->

<br/>

![capa_slids](https://static.wixstatic.com/media/1c667d_aa78c5abec0c4aa6b88cf8f373814932~mv2.png/v1/fill/w_310,h_232,al_c,q_85,usm_0.66_1.00_0.01/1c667d_aa78c5abec0c4aa6b88cf8f373814932~mv2.webp)

![segundo slide](https://static.wixstatic.com/media/1c667d_2dde9da89f81445baaa167fa0dfe9c29~mv2.png/v1/fill/w_310,h_232,al_c,q_85,usm_0.66_1.00_0.01/1c667d_2dde9da89f81445baaa167fa0dfe9c29~mv2.webp)

![terceiro slide](https://static.wixstatic.com/media/1c667d_f88a671e9075413bb98d99745dddc0d0~mv2.png/v1/fill/w_308,h_232,al_c,q_85,usm_0.66_1.00_0.01/1c667d_f88a671e9075413bb98d99745dddc0d0~mv2.webp)

</div>

<br/>

## Sumário

Na construção de slides, a inclusão do sumário ocorre de maneira semelhante a de documentos de texto
`(\tableofcontents)`. Para contextualizar e dar destaque ás seções, existe a opção de envolver o frame
do sumário com o comando `\AtBeginSection[]` ou `\AtBeginSubsection[]`, assim, o sumário aparecerá
anteriormente a cada marcação (seção ou subseção). O critério de contextualização é definido entre colchetes
após a inclusão do sumário, sendo `\currentsection` para seção e `\currentsubsection` para subseção.

Exemplo:

```Latex
\documentclass[]{beamer}

\begin{document}

=======
```Latex

\begin{frame}{Sumário}

\tableofcontents
\end{frame}
\AtBeginSection[]
{
\begin{frame}{Sumário}
\tableofcontents[currentsection]
\end{frame}
}
\section{Introdução}
\section{Desenvolvimento}
\section{Conclusão}

\end{document}

```
<br/>

Compilando o código visto acima obtemos o seguinte resultado:

<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![Copa](https://static.wixstatic.com/media/1c667d_a8b14677d4e04da8991e1c0a649afcc9~mv2.png/v1/fill/w_346,h_261,al_c,q_85,usm_0.66_1.00_0.01/1c667d_a8b14677d4e04da8991e1c0a649afcc9~mv2.webp)

![introdução](https://static.wixstatic.com/media/1c667d_7eaa0caa39914e37a4025dba2bcea677~mv2.png/v1/fill/w_349,h_261,al_c,q_85,usm_0.66_1.00_0.01/1c667d_7eaa0caa39914e37a4025dba2bcea677~mv2.webp)

![Desenvolvimento](https://static.wixstatic.com/media/1c667d_575bd9331d2c4236ae8ae101ab89da96~mv2.png/v1/fill/w_346,h_261,al_c,q_85,usm_0.66_1.00_0.01/1c667d_575bd9331d2c4236ae8ae101ab89da96~mv2.webp)

![Conclusão](https://static.wixstatic.com/media/1c667d_645c7b8db32b4626855c5743e0eb2971~mv2.png/v1/fill/w_349,h_261,al_c,q_85,usm_0.66_1.00_0.01/1c667d_645c7b8db32b4626855c5743e0eb2971~mv2.webp)

<br/>

</div>

## Logotipo

Logotipos da instituição, departamento ou grupo ao qual a apresentação se destina, podem ser inseridos utilizando `\logo{\includegraphics[scale=0.05]{nome do arquivo.extensão}}` no preâmbulo da apresentação. Isso caso o arquivo de imagem esteja na mesma pasta do editável. Caso contrário, deve-se dizer o diretório no qual a imagem se encontra seguido da extensão do arquivo. A logo, nas dimensões especifícadas, irá aparecer em todos os slides no canto direito da tela. Para que ela não passe a aparecer a partir de certoslide, basta que se repita o comando da seguinte forma: `\logo{}`.

Exemplo:

```Latex
\documentclass[]{beamer}
\usepackage{graphicx}
\logo{\includegraphics[scale=0.1]{ufcg.png}}

\begin{document}

Conteúdo do Slides

\end{document}
```
O código a seguir gera o seguinte slide:

<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![logo](https://static.wixstatic.com/media/1c667d_86cc5b354b1c432fa9138ee085d1fcac~mv2.png/v1/fill/w_479,h_363,al_c,q_85,usm_0.66_1.00_0.01/1c667d_86cc5b354b1c432fa9138ee085d1fcac~mv2.webp)

</div>

<br/>

=======
```Latex
\logo{\includegraphics[scale=0.1]{nome da pasta/ufcg.jpg}}
```


## Temas

Em uma analogia, temas no LaTeX podem ser comparados aos *designs do power point*. Por padrão, a confinguração do *slide* apresenta fundo branco, com título em azul e fonte na cor preta. A utilização de temas é feita com o comando `\usetheme{nome do tema}`, no preâmbulo. Dependendo da escolha, as informações do documento (autor, título, subtítulo), assim como o número do slide, aparecerão em todos os frames por meio de barras no canto inferior ou na lateral. Cada tema possui uma cor padrão, mas isso também pode ser modificado, como serão explicado no decorrer do guia. Além disso, cada opção também apresenta diversas configurações, alteráveis utilizando o comando `\usecolortheme{configuração}`.

## *Overlays* e Listas

Algumas partes do texto do slide, ou tópicos, podem ser escondidos para posterior apresentação. Isso é
feito utilizando o comando `\pause.` O uso de listas dentro do ambiente frame ocorre igualmente ao visto para documentos de texto, sendo este recurso fortalecido pelo uso de *overlays*

Exemplo:

```Latex
\documentclass[]{beamer}

\begin{document}

\begin{frame}{Uso de Listas e Overlays}
\begin{itemize}
\item Um;
\item Dois;
\pause
\item Três;
\end{itemize}
\end{frame}

\end{document}
``` 

Compilando o código visto acima obtemos o seguinte resultado:

<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![um](https://static.wixstatic.com/media/1c667d_224ebe142333464b96d8afc8b36573df~mv2.png/v1/fill/w_330,h_250,al_c,q_85,usm_0.66_1.00_0.01/1c667d_224ebe142333464b96d8afc8b36573df~mv2.webp)

![dois](https://static.wixstatic.com/media/1c667d_39af992e35cc4ee3b304d3bc3994429f~mv2.png/v1/fill/w_338,h_250,al_c,q_85,usm_0.66_1.00_0.01/1c667d_39af992e35cc4ee3b304d3bc3994429f~mv2.webp)

</div>

<br/>

## Rodapé

Alguns temas oferecem em seu layout a opção de rodapé contendo informações do documento. Caso esse recurso não esteja disponível no tema desejado, ele pode ser adicionado no preâmbulo do documento com o comando `\useoutertheme{infolines}` que gera, no rodapé do slide, uma barra horizontal contendo o nomedo autor, título do trabalho, data da última compilação e nuúmero do slide. Já para inserir apenas o número do slide, usa-se `\setbeamertemplate{footline}[frame number]`Caso deseje-se eliminar a barra de ferramentas que aparece no rodapé, deve-se inserir a diretiva `\setbeamer template{navigation symbols}`, no prêambulo do documento.

## Blocos

Teoremas, exemplos e corolários podem ser facilmente inseridos no texto. De acordo com o tema utilizado,
esses ambientes podem ser realçados, dando destaque as informações em seu interior. Outro importante
recurso da classe beamer é a utilizacão do ambiente **block**, que pode ser combinado com listas e *overlays*.
Isso pode ser visto no exemplo 4.5 que usa o tema *Warsaw*.

Exemplo:

```Latex
\documentclass[]{beamer}

\begin{document}

\newtheorem{teorema}{Teorema}
\begin{frame}{Blocos}
\begin{teorema}
Teoremas são realçados pelo uso da classe beamer!!!
\end{teorema}
\pause
\begin{block}{Nome do bloco}
Aqui é digitado o texto que fica no bloco!!!
\end{block}
\end{frame}

\end{document}
```

Compilando o código visto acima obtemos o seguinte resultado:

<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![bloco1](https://static.wixstatic.com/media/1c667d_d14f002fec8d41929902cb4cc63c78b8~mv2.png/v1/fill/w_328,h_246,al_c,q_85,usm_0.66_1.00_0.01/1c667d_d14f002fec8d41929902cb4cc63c78b8~mv2.webp)

![bloco2](https://static.wixstatic.com/media/1c667d_9db840cef7eb4aaa92eb3362c0d2fbab~mv2.png/v1/fill/w_331,h_246,al_c,q_85,usm_0.66_1.00_0.01/1c667d_9db840cef7eb4aaa92eb3362c0d2fbab~mv2.webp)

</div>

<br/>

## Colunas

O uso de colunas no *slide* pode deixar a apresentação mais dinâmica, além de servir para um melhor aproveitamento do espaço. Isto pode ser feito mediante o ambiente **columns** indicando o espaço onde as colunas se encontram. O início de uma coluna ocorre com o comando `\column[alinhamento{largura}.` Entre as opcões de alinhamento, estão **t** ou **b**, indicando se o texto será colocado no topo ou na base da coluna. A largura é indicada em centímetros, porém é mais fácil indicar porcentagem da largura do *slide* com o trecho valor `\textwidth.` Não é necessário indicar o fim de uma coluna, apenas o início da próxima.

Exemplo:
```Latex
\documentclass[]{beamer}

\begin{document}

\begin{columns}
\column[t]{.5\textwidth}
\begin{itemize}
\item Espécie de diciário;
\item Veículo de informação personalizada;
\item Formação coletiva;
\item Profissão: Blogueiro.
\end{itemize}
\column[t]{.5\textwidth}
\begin{figure}
\includegraphics[scale=0.8]{figuras/blog2.jpg}
\end{figure}
\end{columns}

\end{document}
```
<br/>

Compilando o código visto acima obtemos o seguinte resultado:
<br/>
<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![coluna](https://static.wixstatic.com/media/1c667d_d806d156293549e49e85f9a5e7e912fe~mv2.png/v1/fill/w_397,h_296,al_c,q_85,usm_0.66_1.00_0.01/1c667d_d806d156293549e49e85f9a5e7e912fe~mv2.webp)

</div>
<br/>

# Fonte

## Tamanho da Fonte

O tamanho de fonte padrão do beamer é 14 pontos, porém é possível alterar o tamanho desta para 8, 9, 10, 11, 12, 14, 17 e 20 nas opcções ao definir o documento `(\documentclass[opções]{classe})`, em alguns computadores o TeXMaker não realiza essa alteração. Outros valores de pontos não são considerados pelo compilador.

Exemplo:
```Latex
\documentclass[17pt]{beamer}
```
## Estilos de fonte

Adicionando o comando `\setbeamerfont{structure}{opcões}` no preâmbulo do documento é possível alterar a estrutura da fonte dos cabeçalhos, rodapés e capa, mantendo o texto central do **slide** inalterado.

Entre as opcões disponíveis estão:

  Comando | Resultado |
| :----------: | :-----------: |
|family=\rmfamily|Fonte em letra romana|
|shape=\itshape|Formato em itálico|
|series=\bfseries|Formato em negrito|

Já o estilo da fonte interna do *slide* pode ser modificado a partir do comando `\usefonttheme{opções}`, lembrando que fÓrmulas matemáticas e textos internos a esse ambiente não são modificadas pela utilizção desse recurso. Todas as opções de fonte podem ser encontradas no documento de definição da classe *beamer*

## Margens

O tamanho padrão do slide, na classe *beamer*, é de 128mm por 96mm, valores fixos e que não podem ser alterados. Contudo, é possível alterar as margens laterais - 1cm padrão utilizando no preâmbulo o comando `\setbeamersize{larguras}`

Exemplo:
```Latex
\setbeamersize{text margin left=4mm, text margin right=4mm}
```
## Cores

Conforme pode ser observado, os temas utilizados já possuem cores padrões de layout. Porém, isso pode ser modificado utilizando no preâmbulo a diretiva `\usecolortheme[named= nome da cor]{structure}.` As cores dependem do arquivo xcolor que deve ser carregado explicitamente na definicão do documento, fazendo com que as cores estejam disponíveis. As principais cores que podem ser usadas encontram-se em anexo.

Exemplo:

``` Latex
\documentclass[xcolor]{beamer}
```
O pacote xcolor também permite misturar as cores, formando outras opcões. Isso é feito utilizando uma
porcentagem de uma cor A e (100- porcentagem) de uma cor B, da seguinte forma: `A!porcentagem!B.`

Exemplo:

```Latex
red! 15!yellow
```
Há outros pacotes de cores como dvipsnames ou svgnames, que disponibilizam outros tipos de cores, como
exposto nas fíguras B.1 e B.2, encontradas em anexo.

## Plano de fundo

O plano de fundo do slide em LATEX é branco por padrão. Isso que pode ser mudado utilizando o comando
`\setbeamercolor{normal text}{bg=cor}` no corpo do documento. Uma porcentagem da cor também pode
ser usada. Esse recurso demanda um certo cuidado, pois dependendo da cor escolhida para compor o fundo
do texto, este pode não ser visualizado perfeitamente. É bom ressaltar que um texto branco com contorno preto sempre será vissível não importa a cor do plano de fundo, porémm enfatiza-se a importância de ter bom senso nas escolhas das cores.

Exemplo:

```Latex
\setbeamercolor{normal text}{bg=green!26}
```
Também é possível gerar diferentes combinações de cores no topo e na base do *slide*.

Exemplo:
```Latex
\setbeamertemplate{background canvas}
[vertical shading][bottom=white!100,top=green!50]
```
Imagens também podem ser inseridas como plano de fundo dos slides, porém assim como para as cores, esse recurso deve ser usado com parcimônia, pois uma imagem muito extravagante pode deixar a apresentação confusa e inapropriada.

Exemplo:
```Latex
\setbeamertemplate{background}
{\includegraphics[width=\paperwidth]{nationalgeo.jpg}}
```
## Referências bibliográficas

As referências bibliográficas 
gera um visualização apropriada e profissional. O uso de referências cruzadas pode ser usado da forma já mencionada.

Exemplo:

```Latex
\documentclass[]{beamer}

\begin{document}

\begin{thebibliography}{9}
\bibitem{ref1}[1] CARDOZO, Missila Loures.
{\it Twitter:Microblog e Rede Social}
.Caderno.com, Vol. 4 - No 2 - 2o semestre de 2009.
\bibitem{ref2}[2] NÓREGA, Lívia de Pádua.
{\it A construcão de identidades nas Redes Sociais}.
Fragmentos de Cultura, vol. 20, jan/fev.2010.
\bibitem{ref3}[3] GUTIERRES, Daniel Cianelli Bull.
{\it As mídias sociais e o Twitter}.
\bibitem{ref4}[4] AGUIAR, Giseli Adornato de.SILVA,
José Fernando Modesto da.{\it As bibliotecas
universitárias nas redes sociais:facebook, orkut, myspace,
ning}.II Seminário Internacioanl de Bibliotecas Digitais, Brasil.
\end{thebibliography}

\end{document}
```
Compilando o código visto acima obtemos o seguinte resultado:
<br/>
<br/>

<div style="text-align:center"> </p> <!--Centraliza texto-->

![referencia](https://static.wixstatic.com/media/1c667d_87371c3f0d104aa7abfa7b6636f28ec8~mv2.png/v1/fill/w_432,h_321,al_c,q_85,usm_0.66_1.00_0.01/1c667d_87371c3f0d104aa7abfa7b6636f28ec8~mv2.webp)

</div>
<br/>

# Fonte

Grupo PET Engenharia Elétríca. Apostila 7° edição de LATEX. Campina Grande: UFCG, 2016.
