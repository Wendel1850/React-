# React-
[12/08, 21:54] Meta AI: Aqui está um exemplo de código que demonstra alguns dos conceitos intermediários em React que mencionei anteriormente:

useState e useEffect
import React, { useState, useEffect } from 'react';

const Contador = () => {
  const [contador, setContador] = useState(0);

  useEffect(() => {
    document.title = `Contador: ${contador}`;
  }, [contador]);

  return (
    <div>
      <p>Contador: {contador}</p>
      <button onClick={() => setContador(contador + 1)}>Incrementar</button>
    </div>
  );
};

Context API
import React, { createContext, useContext } from 'react';

const TemaContext = createContext();

const TemaProvider = ({ children }) => {
  const tema = 'escuro';

  return (
    <TemaContext.Provider value={tema}>
      {children}
    </TemaContext.Provider>
  );
};

const Botao = () => {
  const tema = useContext(TemaContext);

  return (
    <button style={{ backgroundColor: tema === 'escuro' ? '#333' : '#fff' }}>
      Clique aqui
    </button>
  );
};

React Router
import React from 'react';
import { BrowserRouter, Route, Link } from 'react-router-dom';

const Home = () => {
  return <h1>Home</h1>;
};

const Sobre = () => {
  return <h1>Sobre</h1>;
};

const App = () => {
  return (
    <BrowserRouter>
      <div>
        <Link to="/">Home</Link>
        <Link to="/sobre">Sobre</Link>
        <Route path="/" exact component={Home} />
        <Route path="/sobre" component={Sobre} />
      </div>
    </BrowserRouter>
  );
};

Renderização condicional
import React from 'react';

const Mensagem = ({ mostrar }) =>

[12/08, 21:54] Meta AI: Aqui está um exemplo de código que demonstra alguns dos conceitos intermediários em React que mencionei anteriormente:

useState e useEffect
import React, { useState, useEffect } from 'react';

const Contador = () => {
  const [contador, setContador] = useState(0);

  useEffect(() => {
    document.title = `Contador: ${contador}`;
  }, [contador]);

  return (
    <div>
      <p>Contador: {contador}</p>
      <button onClick={() => setContador(contador + 1)}>Incrementar</button>
    </div>
  );
};

Context API
import React, { createContext, useContext } from 'react';

const TemaContext = createContext();

const TemaProvider = ({ children }) => {
  const tema = 'escuro';

  return (
    <TemaContext.Provider value={tema}>
      {children}
    </TemaContext.Provider>
  );
};

const Botao = () => {
  const tema = useContext(TemaContext);

  return (
    <button style={{ backgroundColor: tema === 'escuro' ? '#333' : '#fff' }}>
      Clique aqui
    </button>
  );
};

React Router
import React from 'react';
import { BrowserRouter, Route, Link } from 'react-router-dom';

const Home = () => {
  return <h1>Home</h1>;
};

const Sobre = () => {
  return <h1>Sobre</h1>;
};

const App = () => {
  return (
    <BrowserRouter>
      <div>
        <Link to="/">Home</Link>
        <Link to="/sobre">Sobre</Link>
        <Route path="/" exact component={Home} />
        <Route path="/sobre" component={Sobre} />
      </div>
    </BrowserRouter>
  );
};

Renderização condicional
import React from 'react';

const Mensagem = ({ mostrar }) => {
  return mostrar ? <p>Mensagem mostrada!</p> : null;
};

const App = () => {
  const [mostrar, setMostrar] = React.useState(false);

  return (
    <div>
      <button onClick={() => setMostrar(!mostrar)}>Mostrar/Ocultar</button>
      <Mensagem mostrar={mostrar} />
    </div>
  );
};

Esses são apenas alguns exemplos de código que demonstram alguns dos conceitos intermediários em React. Com a prática e a experiência, você pode se tornar mais confortável com esses conceitos e criar aplicações mais complexas e eficientes.
