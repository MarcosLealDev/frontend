yarn init -y

yarn add react react-dom

Babel: converter (transpilar) código do React para um código que o browser entenda.
Webpack: Pra cada tipo de arquivo (.js, .css, .png) eu vou converter o código de uma maneira diferente

Loaders: babel-loader, css-loader, image-loader


yarn add @babel/core @babel/preset-env @babel/preset-react webpack webpack-cli

add file below based on the website http://babel.js.io
babel.config.js 

With the command below ...
yarn add @babel/cli

... you will be able to exectute the follwing
yarn babel src/index.js --out-file public/bundle.js

Now, create the file
webpack.config.js

install 
yarn add babel-loader

Depois de configurar webpack.config.js

yarn webpack --mode development

And now to run all the time, install
yarn add webpack-dev-server -D 

add to webpack.config.js
devServer: {
        contentBase: path.resolve(__dirname, 'public'),
    }

And run:
yarn webpack-dev-server --mode development

JSX: HTML dentro do JavaScript (Javascript XML)
Component é uma função que retorna HTML

Fragment: using <></> em vez de ter uma div (extra component)

3 conceitos mais importante do React
1. Componente
2. Propriedade (colocar um atributo no componente como se fosse uma função)
3. Estado e Imutabilidade

useState retorna um array com 2 posições
1. a variável com seu valor inicial
2. Função para atualizarmos esse valor

New rule on webpack for css
yarn add style-loader css-loader file-loader

edit the webpack.config.js to add new rules

Installing axios (responsável por fazer chamadas api no front-end conectando com backend)

Using useEffect (utilizar para disparar funções quando tiver alterado)
yarn add axios

No backend instalar cors
yarn add cors

Installar Babel plugin to add async await
yarn add @babel/plugin-transform-runtime -D