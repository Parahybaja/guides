# Tutorial Markdown

## O que é Markdown?
Markdown é uma linguagem de marcação leve com sintaxe de formatação de texto simples projetada para que ela possa ser convertida em HTML e muitos outros formatos usando uma ferramenta com o mesmo nome. Markdown é usado frequentemente para formatar arquivos readme.

## Benefícios de usar Markdown
O principal benefício de usar o markdown é a portabilidade. Qualquer editor de qualidade de markdown poderá pegar um documento de markdown (.md ou .mkd) e convertê-lo em outros formatos. além disso outro benefício do uso de markdown é que a sintaxe é direta. 

<br/>
<br/>
<br/>

# Editores de código Markdown online

<br/>


![replit](https://cp4l.org/images/replit_logo.png)

<br/>

### **Vantagens de uso:**

- Edição de código simultaneo. 
- Baixa curva de aprendizado.
- Gratuito.

### **Desvantagens de uso:**

  - Apresenta travamentos repentinos.
  - Consome muitos recursos do dispositivo.

<br/>

**Link**[ [replit](https://replit.com/) ]

<br/>
<br/>

## DILLINGER

![DILLINGER](https://www.bypeople.com/wp-content/uploads/2014/12/online-markdown-editor.png)

<br/>

### **Vantagens de uso:**

- Praticidade(com poucos clicks já é possivel iniciar a edição)
- Fácil adaptação a plataforma. 
- Gratuito.
- Oferece diferentes formas de exportar o arquivo editado.

### **Desvantagens de uso:**

  - Não possui serviço de armazenamento do código próprio.
  - Não possui tema de cores escuro.

  <br/>

  **Link**[ [DILLINGER](https://dillinger.io/) ]

<br/>

<br/>

## **Editores de código markdown offline**

![VS CODE](https://surveymonkey-assets.s3.amazonaws.com/survey/271006234/08441d03-100f-49e6-9124-fe311fad2e2a.png))


<br/>

### **Vantagens de uso:**

- Modularidade.
- Ampla quantidade de módulos desenvolvido pela comunidade para markdown.
- Gratuito.


### **Desvantagens de uso:**

  - Elevado processamento e memoria RAM.
  - Instabilidades ocassionais.

  <br/>

  **Link**[ [VS CODE](https://code.visualstudio.com/download) ]

<br/>

<br/>


## Cabeçalhos 
O número de cerquilha determina o tamanho da fonte de acordo com o exemplo abaixo, temos o seguinte texto renderizado:

<br/>

# C1
## C2
### C3
#### C4
##### C5
###### C6

<br/>


Para gerar as fontes com tamanhos diferentes vistas acima, temos os seguites códigos em markdown:

```markdown
# C1
## C2
### C3
#### C4
##### C5
###### C6
```


<br/>
<br/>


## Padrões dos caracteres

<br/>

Para adicionar ênfase ao conteúdo que será escrito, usa-se o asterisco `*` ou traço-baixo (underline)  `_` , a combinação desses dois caracteres nos dá o seguinte resultado:


<br/>

| Código em markdown | saida após a  renderização     |
| :-------------------: | :----------------------:|
|       `*Italico*`            |     *Italico*    |
|      `_Italico_`      |       _Italico_        |
| `**Negrito** ` | **Negrito** |
| `__Negrito__` | __Negrito__ |
| `~~Cortado~~`| ~~Cortado~~ |

<br/>

No markdown também é possivel fazer mais de um tipo de modificação em uma mesma fonte, na tabela a seguir podemos ver algum dos casos:

<!----- citação ---------->

<br/>
<br/>


## Bloco de citação
Para transformar um texto em uma citação ou comentário, utilize o sinal  `>`   no início da linha que será formatada.

```markdown
> Tutorial Markdown
```
Apos a renderização temos o seguinte resultado

> Tutorial Markdown

<br/>

## Listas
No Markdown existem duas tipologia de listas: listas ordenadas e listas desordenadas.

<br/>

### Listas ordenadas

1. primeiro item
2. segundo item
3. terceiro item

<br/>

Para gerar a lista ordenada,temos o seguinte código em markdown:



```markdown

1. primeiro item
2. segundo item
3. terceiro item

```

<br/>

### Listas desordenadas

- Primeiro item
- Segundo item
- Terceiro item

<br/>

Para gerar a lista ordenada,temos o seguinte código em markdown:



```markdown

- Primeiro item
- Segundo item
- Terceiro item

```

<br/>

### Barra Horizontal 
Adicione no mínimo três underline para construir uma barra horizontal.

<br/>

___

<br/>

Para gerar a barra horizontal vista acima, temos o seguinte código:

```markdown

___

```

<br/>


### Tabela 
Escolha os títulos das colunas e use | para delimitar as colunas. Depois, utilize hífen - na segunda linha para indicar que acima estão os títulos das colunas, usando novamente o | para delimitar colunas. Veja um exemplo abaixo:

|  Sintaxe | Descrição |
| :----------: | :-----------: |
| Cabeçalho | Título |
| Paragrafo | Texto |

A tabela acima foi costruida com o seguinte código em mardown:

```

| Sintaxe | Descrição|
| ----------- | ----------- |
| Cabeçalho | Título |
| Paragrafo | Texto |

```


## Códigos

### Código em bloco
Para obter múltiplas linhas de código: envolva as linhas de código com três acentos graves ˋˋˋ

![bloco de codigo](https://static.wixstatic.com/media/1c667d_28b07221f6ad49f59c2d891ccef084e9~mv2.png/v1/fill/w_488,h_97,al_c,q_85/1c667d_28b07221f6ad49f59c2d891ccef084e9~mv2.webp)

<br/>

As Linhas de código vistas acima geram a seguinte saida renderizada:

```
print("hello word")
print("hello markdown")
```
<br/>

### Código em linha

adicione um acento grave ˋ no início e no final do código.

<br/>

`cout<<"Tutorial Markdown";`

<br/>

A saida renderizada vistas acima é resultado da seguinte Linha de código:

```
`cout<<"Tutorial Markdown";`
```

<br/>

## Adição de links em Markdown

<br/>

![LINK](https://www.apptuts.net/wp-content/uploads/2019/08/destaque-3.jpg)

<br/>
<br/>
<br/>

Para adicionar um Link temos a seguinte sintaxe:


```
[ CLICK EM MIM ](https://www.markdownguide.org/)
```

Onde dentro dos colchetes deve ser inserido o nome que sera mostrado ao usuario e dentro dos parenteses deve ser inserido o link desejado

<br/>


## [ CLICK EM MIM ](https://www.markdownguide.org/)

<br/>

Ao clicar no nome desejado somos redirecionados ao link escolhido 


<br/>
<br/>


## Adição de imagens em Markdown

<br/>

![IMAGENS](https://image.freepik.com/vetores-gratis/ilustracao-de-galeria-icone_53876-27002.jpg)


<br/>
<br/>

Para adicionarmos uma imagem em markdown temos a seguinte sintaxe


```markdown
![ markdown ]( https://d33wubrfki0l68.cloudfront.net/f1f475a6fda1c2c4be4cac04033db5c3293032b4/513a4/assets/images/markdown-mark-white.svg )

```

Onde dentro dos colchetes deve ser inserido o nome que será dado a imagem e dentro dos parenteses deve ser inserido o link da imagem desejada. Na pespectiva do usuario será apresentada apenas a imagem, vegamos um exemplo:

<br/>

![ markdown ]( https://d33wubrfki0l68.cloudfront.net/f1f475a6fda1c2c4be4cac04033db5c3293032b4/513a4/assets/images/markdown-mark-white.svg )



<br/>
<br/>
<br/>

## **FONTES ADICIONAIS:** 

- ### https://www.markdownguide.org/

<br/>

- ### https://alyssonmach.github.io/Minicurso-Git-e-GitHub/jup-not/CriandoEmMarkdown.html


