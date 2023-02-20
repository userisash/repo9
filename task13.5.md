import React, { useEffect, useRef } from 'react';

function MyForm() {
  const inputRef = useRef(null);

  useEffect(() => {
    inputRef.current.focus();
  }, []);

  return (
    <form>
      <label>
        Name:
        <input type="text" ref={inputRef} />
      </label>
      <input type="submit" value="Submit" />
    </form>
  );
}

export default MyForm;

import { useState } from 'react'
import reactLogo from './assets/react.svg'
import MyForm from './Form'
import './App.css'

function App() {
  const [count, setCount] = useState(0)

  return (
    <div className="App">
     <MyForm/>
    </div>
  )
}

export default App
