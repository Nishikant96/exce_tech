// Make a simple todo app with reactJS, just need two features in the app
// To add a todo
// To display all todo

```
import { useState } from "react";
export default function App() {
  const [state, setState] = useState({ todo: [] });
  const [inputState, setInputState] = useState("");

  const handleChange = (e) => {
    setInputState(e.target.value);
  };

  const handleClick = () => {
    let s = [...state.todo, inputState];
    setState({ todo: s });
    setInputState("");
  };
  return (
    <>
      <h1>Please add tasks below</h1>
      {state.todo.map((value, id) => (
        <div key={id}>{value}</div>
      ))}
      <input
        value={inputState}
        onChange={handleChange}
        placeholder="Add Task Here"
      ></input>
      <button onClick={handleClick}>Add Task!</button>
    </>
  );
}
```
