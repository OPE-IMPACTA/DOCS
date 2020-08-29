# Automação de Front End

## NPM (Node Package Manager)

- Gerenciador de pacotes
- Link: <https://www.npmjs.com/>

Verificar a versão:
~~~javascript
npm -v
~~~

## Package.json

`package.json` - Arquivo local com as configurações e dependências de pacotes NPM

Inicia uma nova configuração local do npm
~~~javascript
npm init
~~~

Instala todas as dependências listadas no arquivo `package.json`
~~~javascript
npm install
~~~

~~~json
{
  "name": "projetoanimais",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "jquery": "^3.5.1"
  }
}
~~~

## Instalar pacotes

Instala o pacote jquery no diretório atual:
~~~javascript
npm install jquery
~~~

Instala o pacote globalmente:
~~~javascript
npm install eslint -g
~~~

Atualiza o pacote jquery:
~~~javascript
npm update jquery
~~~

Desinstala o pacote jquery:
~~~javascript
npm uninstall jquery
~~~

Obs:
- Ao instalar um pacote ele ficará como dependência do projeto
- Será criado uma pasta `node_modules` com os pacotes instalados
- Será criado um arquivo `package-lock.json` com os pacotes e as versões instaladas

## ESlint
 - Evitar problemas
 - Indica a existência de possíveis padrões problemáticos no códigos
 - Definir padrões
 - Padronizar e manter consistência entre diferentes códigos JavaScript
 - Link: <https://eslint.org>

## Instalar ESlint

Instalar o eslint globalmente:
~~~javascript
npm install eslint -g
~~~

Iniciar repositório NPM no local:
~~~javascript
npm init
~~~

~~~javascript
eslint --init
~~~
- To check syntax, find problems, and enforce code style
- JavaScript modules (import/exports)
- None of these
- No
- Browser
- Use a popular style quide
- Airbnb: https://github.com/airbnb/javascript
- JSON
- Yes

Obs: Será criado arquivo `.eslintrc.json`

~~~json
{
    "env": {
        "browser": true,
        "es2020": true
    },
    "extends": [
        "airbnb-base"
    ],
    "parserOptions": {
        "ecmaVersion": 12,
        "sourceType": "module"
    },
    "rules": {
        "import/extensions": 0
    }
}
~~~

Instalar a extensão no visual studio code
- ESLint

## Webpack

- Bundler
- Agrupa / processa diversos arquivos e otimiza os mesmos.
- Altamente configurável
- Link: <https://webpack.js.org>

Instala o webpack e a cli do mesmo, ter o package.json antes.
~~~javascript
npm install --save-dev webpack webpack-cli
~~~

## NPM Scripts

Permite definirmos uma linha de comando inteira, que será ativada com `npm run nomeScript`, o `scripts` fica dentro do arquivo `package.json`

~~~json
"scripts": {
    "build": "webpack --mode production js/script.js --output js/main.js",
    "dev": "webpack --mode development --watch js/script.js --output js/main.js"
  },

  --mode define o modo da compilação
  --watch define se deve ficar observando
~~~

## Scripts Externos

Podemos facilmente importar scripts externos instalados os mesmo através do NPM e utilizando o Webpack para fazer p bundler final

Exemplos: 

~~~javascript
npm install jquery
npm install lodash
~~~

~~~javascript
import $ from 'jquery';
import _ from  'lodash';
~~~

~~~javascript
$('nav').hide();
_.differenc(['Banana', 'Morango', 'Uva'], ['Banana', 'Morango', 'Uva']);
//Uva
~~~

## Babel
- Compilador
- Transforma código novo em código antigo, exemplo:

~~~javascript
const nome = 'Matheus'; vira var nome = 'Matheus';
~~~

Browser suporte
- Para que um browser possa suportar algo novo de JavaScript é preciso que ele esteja atualizado, mas nem todo usuário possui a última versão do browser instalada.

Can I Use
- O site <https://caniuse.com/> mostra em quais browsers a novidade está disponível ou não.

## Polyfill vs Transpiler

Polyfill
- Cria métodos / funções com o mesmo nomo das atuais, porém utilizando código antigo para permitir o uso em browsers que não possuem a API
  
Tranpiler
- Transforma código novo em código antigo. Ou seja, transforma `const` em `var`.

## Instalar Babel
- Link: <https://babeljs.io/docs/en/usage>

~~~javascript
npm install --save-dev @babel/core @babel/cli @babel/preset-env
npm install --save @babel/polyfill
~~~

## Criar um arquivo de configuração

Precisamos configurar o webpack, para utilizarmos o @babel/polyfill

`webpack.config.js`

~~~javascript
npm install whatwg-fetch --save
~~~

~~~javascript
const path = require('path');

module.exports = {
  entry: ['@babel/polyfill', 'whatwg-fetch', './js/script.js'],
  output: {
    path: path.resolve(__dirname, './js'),
    filename: 'main.js',
  },
};
~~~

`package.json`

~~~json
"scripts": {
    "build": "webpack --mode production",
    "dev": "webpack --mode development --watch"
  },
~~~

