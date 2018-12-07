# Framework ReactJS

## O que é necessário termos em nossa máquina ?

Para desfrutar do framework, são necessárias algumas dependências em nossa estação de trabalho, são elas:

* **npm** *(Node Package Manager)* ou **yarn**
* **Node.js**

## Iniciando uma aplicação utilizando React

Para darmos inicio a nossa aplicação, vamos instalar o *create-react-app* para já baixar uma **pré** configuração deu uma aplicação *React*.

Vamos então ao nosso terminal e digitar o seguinte comando:

```
npm install -g create-react-app
```

> Definimos o *-g* quando quando queremos adicionar este pacote de forma **global**.

Com isso feito, partimos para a criação de nossa primeira aplicação.

## Criando a nossa primeira aplicação

Com o nosso pacote instaldo, devemos agora criar nossa aplicação, para isso, digitamos no terminal, o comando abaixo:

```
create-react-app nome-da-aplicação
```

## Entendendo Componentes no React

A estrutura de um componente é basicamente essa:

```typescript
import React, { Component } from 'react';

class App extends Component {
  render() {
    return (
      <div className="App">
        <h1>Hello RocketSeat!</h1>
      </div>
    );
  }
}

export default App;
```

Nada mais é do que uma classe que importa e extende por padrão a classe *Component* do React. 

### Arquivos dos Componentes gerados

O arquivo *index.js* é o principal arquivo de renderização de nossa aplicação **React**, é a partir dele que ela é iniciada.

```typescript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import * as serviceWorker from './serviceWorker';

ReactDOM.render(<App />, document.getElementById('root'));

// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: http://bit.ly/CRA-PWA
serviceWorker.unregister();
```

> Importa-se sempre o componente *React* quando utilizamos **JSX**, como no exemplo de *<App />*

O *ReactDOM.render* é utilizado apenas uma vez em toda a nossa aplicação, que tem como objetivo renderizar nosso componente na tela, neste caso o *App.js*.

Utilizando a seguinte linha:

```typescript
ReactDOM.render(<App />, document.getElementById('root'));
```

> Estamos pegando nossa render e jogando na tag *HTML* chamada de **Root** localizada no *index.html*.
