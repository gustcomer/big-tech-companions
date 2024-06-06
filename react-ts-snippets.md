# React with Typescript Snippets

### Using Props #props

```typescript
// Greeting.tsx
import React from 'react';

// Define the type for the props
interface GreetingProps {
  name: string;
}

// Define the component
const Greeting: React.FC<GreetingProps> = ({ name }) => {
  return <h1>Hello, {name}!</h1>;
};

export default Greeting;

// App.tsx
import React from 'react';
import Greeting from './Greeting';

// Define the parent component
const App: React.FC = () => {
  return (
    <div>
      <Greeting name="Alice" />
      <Greeting name="Bob" />
    </div>
  );
};

export default App;
```