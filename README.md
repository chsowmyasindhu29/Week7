import React, { useState } from 'react';

function App() {
const students = [
    { id: 1, name: 'Ravi' },
    { id: 2, name: 'Sita' },
    { id: 3, name: 'Kiran' },
    { id: 4, name: 'Priya' }
  ];

  const [login, setLogin] = useState(false);

  return (
    <div>

       <h2>Student List</h2>

      <ul>
        {students.map((student) => (
          <li key={student.id}>
            {student.name}
          </li>
        ))}
      </ul>

      <h2>Conditional Rendering</h2>

      {login ? (
        <h3>Welcome User!</h3>
      ) : (
        <h3>Please Login</h3>
      )}

      <button onClick={() => setLogin(!login)}>
        {login ? 'Logout' : 'Login'}
      </button>
    </div>
  );
}

export default App;
