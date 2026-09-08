
Преобразование типов данных:
```mermaid
graph TD;
	A[byte] --> B[short];
	B --> C[int];
	C --> D[long];
	F[char] --> C;
	C --> E[float];
```

Scanner  scanner = new Scanner (System(in))