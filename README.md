## Introdução
Bootstrap foi criado no Twitter em meados de 2010 por @mdo e @fat.
- Era conhecido por Twitter Blueprint antes de ser código aberto.

## Passos para uso do NodeJS
- Na pasta raiz do site, digito:
	- $npm init
		- Comando para inicilizar o meu projeto que vai usar o NodeJS
		- As informações iniciais que ele vai pedir, não são necessárias serem informadas
		- Tão logo finalize, vai criar o arquivo "package.json" com as informações do projeto NodeJS criado
## Passos para inclusão do Bootstrap
Todos os passos estão descritos [aqui](https://getbootstrap.com/docs/5.0/getting-started/introduction/)

- tag &lt;link&gt; do CSS do bootstrap no &lt;head&gt;
- tag &lt;script&gt; do JS do bootstrap próximo ao &lt;/body&gt;
	ATENÇÃO: O Bootstrap 5 não precisa mais do jquery como instruído no vídeo.
- [Baixar o pacote de recursos do SASS do Bootstrap](https://github.com/twbs/bootstrap/archive/v5.1.1.zip)
	- Incluir na pasta do site
	- Rodar o CHMOD para dar permissão de execução aos arquivos da pasta
		$chmod 775 -R bootstrap-5.1.1/
	- Alterar o link do CSS para fazer referência ao arquivo local da pasta baixada
	- Alterar o link do JS para fazer referência ao arquivo local da pasta
		Se usar o popper, manter a url do jeito que está.

## Resumo de algumas tags
Explore e testes os conteúdos existentes na documentação: [link aqui:](https://getbootstrap.com/docs/5.0/getting-started/introduction/)

- container-fluid -> cria um container que usa toda a largura disponível da página
- pl* -> usado para padding, ou seja, pra definir a distância dentro do elemento
- pl-lg - padding em tela large
- pl-md - padding em tela middle
- pl-sm - padding em tela small
- ...

- tag <nav> é a tag existente em HTML5. Ela refere-se a um menu de navegação


## Passos para utilizar o CSS estendido no NodeJS

- Se quiseremos alterar os recursos do SASS do Bootstrap, precisamos baixar o compilador SASS. No caso, baixei o node-sass do NodeJS
		$npm install node-sass
- Uma vez baixado, abra aquele arquivo criado quando você inicializou o projeto NodeJS, o "package.json" e inclua em "scripts" após a linha 'teste' uma vírgula e o comando abaixo:
			"init:sass": "node-sass sass/main.scss style_sass.css -w"

 - Esse comando irá abrir o main.scss (arquivo que será compilado) e o style_sass.css é a saída resultado dessa compilação.
- Inclua o style_sass.css no &lt;head&gt;
- Gere o sass/main.scss com os comandos que deseja. Lembre-se de incluir a pasta do bootstrap da versão correta que baixou na primeiras linhas.
- Hora de rodar o comando para compilar o SASS
		$npm run init:sass
- Enquanto este comando estiver rodando, eu posso ir editando o meu arquivo sass/main.scss que ele vai gerando as saídas

## Inclusão de 5 cores de um tema
- Pode escolher a paleta de cores que quiser. Sugiro esses dois sites:
	- [Adobe Color](https://color.adobe.com/pt/create/color-wheel)
	- [Colour Lovers](https://www.colourlovers.com/web/trends/websites)
- Inclui essas cores com o nome que quiser no arquivo "sass/main.scss" para criar o tema
- Adiciona essas cores ao $theme-colors do bootstrap
- Só referenciar esses nomes no index.html da mesma forma que fazia com as cores do theme-colors, como `primary`, `sucess` etc.

## Referências
[1] [Criando um Projeto Front-End com Node.JS + SASS + Bootstrap 4](https://www.youtube.com/watch?v=Hm8Q28wPogM)
[2] [Recriei o Layout do Nubank - Começando no Bootstrap 4](https://www.youtube.com/watch?v=3E68h2-Z8Bs)
[3] [Como mudar as cores do Bootstrap 4 - BS4 + WP #02](https://www.youtube.com/watch?v=yoIxmRs9qhY)
