---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-08-24T22:36
---
Para executar um arquivo de especificação do TAD, o `.h` criamos um outro arquivo que o implemente, isto é, que descreva os atributos e métodos.

O arquivo que utiliza o nosso TAD será executado da seguinte forma:

```PowerShell
    g++ lista.c main.cpp -o meu_programa
    ./meuprograma
```

Sendo que:

- `lista.c` é o arquivo de implementação do TAD.

- `main.cpp` é o arquivo que utiliza o TAD.

- `-o` cria o executável e o nome depois é dado a esse programa.