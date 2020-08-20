yarn init -y

yarn add react react-dom

Babel: converter (transpilar) c�digo do React para um c�digo que o browser entenda.
Webpack: Pra cada tipo de arquivo (.js, .css, .png) eu vou converter o c�digo de uma maneira diferente

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
Component � uma fun��o que retorna HTML

Fragment: using <></> em vez de ter uma div (extra component)

3 conceitos mais importante do React
1. Componente
2. Propriedade (colocar um atributo no componente como se fosse uma fun��o)
3. Estado e Imutabilidade

useState retorna um array com 2 posi��es
1. a vari�vel com seu valor inicial
2. Fun��o para atualizarmos esse valor

New rule on webpack for css
yarn add style-loader css-loader file-loader

edit the webpack.config.js to add new rules

Installing axios (respons�vel por fazer chamadas api no front-end conectando com backend)

Using useEffect (utilizar para disparar fun��es quando tiver alterado)
yarn add axios

No backend instalar cors
yarn add cors

Installar Babel plugin to add async await
yarn add @babel/plugin-transform-runtime -D