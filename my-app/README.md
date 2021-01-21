# Principais conceitos

>Estudando os conceitos básicos do *__React__* utilizando a [documentação oficial](https://pt-br.reactjs.org/docs/hello-world.html).

#### --------------------------------------------------------------------------------------------------------------
#### --------------------------------------------------------------------------------------------------------------
### 00 - Hello World

> O famingerado [Hello World](https://pt-br.reactjs.org/docs/hello-world.html) para espantar qualquer urucubaca. 

#### ---------------------------------------------------------------------------------------------------------
index.js

```
  ReactDOM.render(    
    <h1>Hello ... World!</h1>
    document.getElementById('root')
  );

```

> O menor exemplo em React conforme indica o site oficial.

***
### 01 - Introduzindo JSX

> O [JSX](https://pt-br.reactjs.org/docs/introducing-jsx.html) é uma extensão de sintaxe para JavaScript. 

#### ---------------------------------------------------------------------------------------------------------

index.js

```
  const name = 'Josh Perez';
  const element = <h1>Hello, {name}</h1>;

  ReactDOM.render(
    element,
    document.getElementById('root')
  );
```
> Você pode inserir qualquer expressão JavaScript válida dentro das chaves em JSX.
***

### 02 - Renderizando elementos

> Os [elementos](https://pt-br.reactjs.org/docs/rendering-elements.html) são os menores blocos de construção de aplicativos React.

#### --------------------------------------------------------------------------------------------------------------

index.js

```
function tick() {  
  const element = (
    <div>
      <h1>Couting time ... </h1>
      <h2>It is {new Date().toLocaleTimeString()}!</h2>
    </div>
  )

  ReactDOM.render(
    element,
    document.getElementById('root')
  )
}

setInterval(tick(), 1000)
```
> O React somente atualiza o estritamente necessário.
***

### 03 - Componentes e Props

> Quando o React vê um elemento representando um [componente](https://pt-br.reactjs.org/docs/components-and-props.html) definido pelo usuário, 
  ele passa atributos JSX e componentes filhos para esse componente como um único 
  objeto. Nós chamamos esse objeto de “[props](https://pt-br.reactjs.org/docs/components-and-props.html)”.

#### ------------------------------------------------------------------------------------------------------------------------

index.js

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```
##### Vamos recapitular o que acontece:
1. Nós chamamos ReactDOM.render() com o elemento __```<Welcome name="Sara" />```__.
2. React chama o componente Welcome com __```{name: "Sara"}```__ como props.
3. Nosso componente Welcome retorna um elemento __```<h1>Hello, Sara</h1>```__ como resultado.
4. React DOM atualiza eficientemente o DOM para corresponder __```<h1>Hello, Sara</h1>```__.
***

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
