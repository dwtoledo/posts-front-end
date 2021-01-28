# 5 - Tags HTML que você precisa conhecer e Dicas do VS Code.

*Publicações anteriores:*

[1 - O que é HTML? Principais Tags e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/README.md)

[2 - Tags HTML mais utilizadas, Código Semântico e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/2%20-%20Tags%20HTML%20mais%20utilizadas%2C%20C%C3%B3digo%20Sem%C3%A2ntico%20e%20Dicas%20do%20VS%20Code.md)

[4 - Tags HTML para Tabelas e Dicas do VS Code](https://github.com/dwtoledo/posts-front-end/blob/main/3%20-%20Tags%20HTML%20para%20Tabelas%20e%20Dicas%20do%20VS%20Code.md)

[4 - Tags HTML para Formulários e Dicas do VS Code](https://github.com/dwtoledo/posts-front-end/blob/main/4%20-%20Tags%20HTML%20para%20Formul%C3%A1rios%20e%20Dicas%20do%20VS%20Code.md)

Agora que você já viu [...]
* as principais tags e;
* tabelas e;
* formulários em HTML.

[...] chegou a hora daquelas tags pouco conhecidas, mas que você precisa conhecer!

### **Tag \<details>**
Quando usada com a tag \<summary> faz com que um conteúdo escondido seja exibido ao clicar no elemento *summary*. Se clicar novamente, o conteúdo é escondido. E o melhor, sem precisar de JavaScript!

Podemos criar *drop-menu* com essa funcionalidade. Olha só que legal!

```html
<details>
        <summary>Menu</summary>
        <a href="https://google.com/" target="_blank">Google</a><br>
        <a href="https://bing.com/" target="_blank">Bing</a><br>
        <a href="https://duckduckgo.com/" target="_blank">DuckDuckGo</a>
    </details>
```

O resultado é um Menu que ao clicarmos exibe 3 links (Google, Bing e DuckDuckGo):

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/hc4jz3bsa9g5vey2wmaq.gif)

Se tivermos um conteúdo logo abaixo, ele será "empurrado" ou "puxado" quando clicarmos no Menu, veja um exemplo:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/9y4js7aa3a6uetybh54d.gif)
___

### **Tag \<source> com a tag \<audio>**

Você sabia que cada navegador tem preferência por um determinado tipo de audio? O navegador Safari da maça por exemplo, adora o audio ogg!

Então vamos dar aos navegadores o que eles querem para evitar que seu conteúdo não fique disponível para o usuário, segue um exemplo:

```html
<audio controls>
     <source src="./sound.mp3" type="audio/mpeg">
     <source src="./sound.ogg" type="audio/ogg">
     Seu navegador não suporta a tag de audio.
</audio>
```
O resultado é:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/tpyubrxrlwajciwu94f2.png)

O navegador irá mostrar a mensagem "Seu navegador não suporta a tag de audio." caso não consiga carregar nenhuma opção de arquivo de áudio.

___

### **Tag \<source> com a tag \<video>**

Semelhante ao audio:

```html
<video controls>
        <source src="./video.mp4" type="video/mp4">
        <source src="./video.mov" type="video/mov">
        Seu navegador não suporta a tag de vídeo.
</video>
```

O resultado é um player de vídeo:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/g5y76dy8ns3mycqfvg78.png)

O navegador irá mostrar a mensagem "Seu navegador não suporta a tag de vídeo." caso não consiga carregar nenhuma opção de arquivo de vídeo.

Encontrei uma explicação mais detalhada sobre os formatos de audio e vídeos compatíveis nos navegadores, **recomendo a leitura: [MDN Web Docs - Formatos de mídia suportados por elementos HTML de áudio e vídeo
](https://developer.mozilla.org/pt-BR/docs/Web/HTML/formatos_midia_suportados)**

___

### **Tag \<picture>**
Você sabia que é possível deixar suas imagens mais responsivas* só com HTML e sem usar CSS? Usamos a tag picture da seguinte maneira:

```html
<picture>
        <source media="(min-width: 512px)" srcset="./512.jpg">
        <source media="(min-width: 256px)" srcset="./256.jpg">
        <img src="./150.jpg" alt="">
</picture>
```
###### *carregar uma imagem de menor resolução para telas menores e carregar uma imagem com resolução maior para telas maiores.

Explicando:
* se a tela é maior que 512px, o HTML irá carregar "512.jpg";
* se a tela é entre 256px e 512px, o HTML irá carregar "256.jpg";
* se a tela é menor que 256px, será carregado "150.jpg".
* **a ordem é muito importante, sempre do maior tamanho de tela ao menor, caso contrário, não irá funcionar muito bem.**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/gh1axt24vk8nu5n0zrnl.png)

O resultado é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/uurnbqbbfiexerqkeneq.gif)

___

### **Tag \<dl>**
Existem as listas ordenadas *\<ol>* e as listas não ordenadas *\<ul>*. Mas você sabia que existe uma lista de descrições *\<dl>*? Geralmente essa lista é usada em glossários. Vamos ao exemplo de código:

```html
<h2>Filmes do Harry Potter:</h2>

    <dl>
        <dt>Harry Potter e a Pedra Filosofal (2001)</dt>
        <dd>Descrição do 1º filme.</dd>

        <dt>Harry Potter e a Câmara Secreta (2002)</dt>
        <dd>Descrição do 2º filme.</dd>

        <dt>Harry Potter e o Prisioneiro de Azkaban (2004)</dt>
        <dd>Descrição do 3º filme.</dd>

        <dt>Harry Potter e o Cálice de Fogo (2005)</dt>
        <dd>Descrição do 4º filme.</dd>

        <dt>Harry Potter e a Ordem da Fênix (2007)</dt>
        <dd>Descrição do 5º filme.</dd>

        <dt>arry Potter e o Enigma do Príncipe (2009)</dt>
        <dd>Descrição do 6º filme.</dd>

        <dt>Harry Potter e as Relíquias da Morte: Parte 1 (2010)</dt>
        <dd>Descrição do 7º filme.</dd>

        <dt>Harry Potter e as Relíquias da Morte: Parte 2 (2011)</dt>
        <dd>Descrição do 8º filme.</dd>
    </dl>

    <img src="./harry-potter-movies.png" alt="Capas de todos os filmes do Harry Potter">
```

No código acima, temos uma lista *\<dl>* envolvendo todos os filmes do Harry Potter:
* cada título de filme está na tag *\<dt> description term*;
* cada descrição do filme está na tag *\<dd> descriptions*.

O resultado é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/oozao1frotvtfp3fxl8x.png)

___

**O post já está ficando grande e ainda tenho tags interessantes para te mostrar! Então vamos chamar esse post de Parte 1 e vou fazer em breve a Parte 2 para vocês!**

____

## **Parabéns!!!**
Fico muito feliz que chegou até o final dessa publicação.
Espero que você tenha aprendido muito!

## **Quer aprender mais?**
Te convido a visitar e seguir o meu canal lá na Twitch: https://www.twitch.tv/dwtoledo.
Lá a gente faz muitas lives de front-end e tem uma playlist muito legal sobre conceitos de HTML!
