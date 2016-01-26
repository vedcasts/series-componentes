## Vedcasts.com.br - Séries - HTML Components

O código fonte deste repositório foi desenvolvido durante a série de aulas sobre HTML Components encontrada em [http://www.vedcasts.com.br/series/html-components](http://www.vedcasts.com.br/series/html-components).

### Instruções de Instalação

Usando o Terminal, clonar o projeto localmente com `git clone git@github.com:vedcasts/series-componentes.git`. Acessar a pasta do projeto com `cd <nome da pasta>` (possivelmente cd series-componentes/).

As bibliotecas/frameworks Javascript obrigatórias para o projeto estão listadas no arquivo `/package.json` encontrado na raiz do site. Trata-se do arquivo lido pelo NPM que fará o download do Javascript do projeto.

Assim, é obrigatório ter o Node.js/NPM instalados. Sua instalação é simples e está disponível para todos os principais sistemas operacionais. Mais info [http://www.nodejs.org](http://www.nodejs.org).

Após certificar-se de que seu ambiente atende aos pré-requisitos listados logo acima, basta usar o Terminal para navegar até a pasta do projeto e rodar o comando `npm install`. Isso criará a pasta /node_modules na raiz do projeto e ali armazenará os scripts necessários.

### Rodar o projeto

Após instalar todas as dependências, basta executar `npm run dev` e no browser acessar `http://localhost:8080`. O comando `npm run dev` está em *package.json* e nada mais é do que uma sequência de comandos para o terminal. *Importante:* é necessário ter o webpack instalado globalmente. Verifique no Terminal `webpack -v` e caso não tenha, instale com `npm install -g webpack`.  

### Dúvidas e sugestões

Por gentileza assista às aulas e deixe suas dúvidas ou sugestões no sistema de comentários existente em cada página de videos.