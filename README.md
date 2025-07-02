# Text-Viewer-24
Text Viewer 
Jsx CopyEdit // App.js
import React, { useState } from 'react';

function App() {const [text, setText] = useState("");

  const handleFile = (e) => {const reader = new FileReader();
    reader.onload = () => setText(reader.result);
    reader.readAsText(e.target.files[0]); };

  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <h1 className="text-2xl font-bold mb-4">Text Viewer</h1>
      <input type="file" accept=".txt" onChange={handleFile} />
      <div className="mt-4 bg-white p-4 rounded shadow">
        <pre className="whitespace-pre-wrap">{text}</pre>
      </div>
    </div> );} export default App;
