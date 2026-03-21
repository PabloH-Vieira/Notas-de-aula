---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-1b9fa7f60cd880c9a478ea23cbd908a4?pvs=21
Last Edited: 2025-08-09T11:51
---
Streams é todo o fluxo de comunicação entre o programa e o dispositivo, podendo ser um fluxo de output ou de input.

Em C existem dois tipos de streams: texto (ou string) e binária (uma sequência de bytes).

O arquivo acessado pelo programa pode ser qualquer um presente no dispositivo, o qual é aberto por uma operação de abertura, a partir do qual informações podem ser trocadas entre o arquivo e o programa. A troca de informações é fechada por um processo de fechamento.

Para realizar uma stream, utilizamos uma estrutura de controle fornecida pela biblioteca `stdio.h` , o tipo FILE, que é acessado por meio de um ponteiro: `FILE *p;`

A biblioteca permite utilizar uma série de funções para trocar informações entre o programa e o arquivo:

|**Function**|**Description**|
|---|---|
|[fclose()](https://www.w3schools.com/c/ref_stdio_fclose.php)|Closes a file|
|feof()|Returns a true value when the position indicator has reached the end of the file|
|ferror()|Returns a true value if a recent file operation had an error|
|[fgetc()](https://www.w3schools.com/c/ref_stdio_fgetc.php)|Returns the ASCII value of a character in a file and advances the position indicator|
|[fgets()](https://www.w3schools.com/c/ref_stdio_fgets.php)|Reads a line from a file and advances the position indicator|
|[fopen()](https://www.w3schools.com/c/ref_stdio_fopen.php)|Opens a file and returns a file pointer for use in file handling functions|
|[fprintf()](https://www.w3schools.com/c/ref_stdio_fprintf.php)|Writes a formatted string into a file|
|[fputc()](https://www.w3schools.com/c/ref_stdio_fputc.php)|Writes a character into a file and advances the position indicator|
|[fputs()](https://www.w3schools.com/c/ref_stdio_fputs.php)|Writes a string into a file and advances the position indicator|
|[fread()](https://www.w3schools.com/c/ref_stdio_fread.php)|Reads data from a file and writes it into a block of memory|
|[fscanf()](https://www.w3schools.com/c/ref_stdio_fscanf.php)|Reads formatted data from a file and writes it into a number of memory locations|
|[fseek()](https://www.w3schools.com/c/ref_stdio_fseek.php)|Moves the position indicator of a file pointer|
|[ftell()](https://www.w3schools.com/c/ref_stdio_ftell.php)|Returns the value of the position indicator of a file pointer|
|[fwrite()](https://www.w3schools.com/c/ref_stdio_fwrite.php)|Writes data from a block of memory into a file|
|getc()|The same as [fgetc()](https://www.w3schools.com/c/ref_stdio_fgetc.php)|
|[getchar()](https://www.w3schools.com/c/ref_stdio_getchar.php)|Reads one character of user input and returns its ASCII value|
|[printf()](https://www.w3schools.com/c/ref_stdio_printf.php)|Writes a formatted string to the console|
|putc()|The same as [fputc()](https://www.w3schools.com/c/ref_stdio_fputc.php)|
|[putchar()](https://www.w3schools.com/c/ref_stdio_putchar.php)|Outputs a single character to the console|
|[puts()](https://www.w3schools.com/c/ref_stdio_puts.php)|Outputs a string to the console|
|[remove()](https://www.w3schools.com/c/ref_stdio_remove.php)|Deletes a file|
|[rename()](https://www.w3schools.com/c/ref_stdio_rename.php)|Changes the name of a file|
|[rewind()](https://www.w3schools.com/c/ref_stdio_rewind.php)|Moves the position indicator to the beginning of the file|
|[scanf()](https://www.w3schools.com/c/ref_stdio_scanf.php)|Reads formatted data from user input and writes it into a number of memory locations|
|[snprintf()](https://www.w3schools.com/c/ref_stdio_snprintf.php)|Writes a formatted string into a `char` array (memory-safe)|
|[sprintf()](https://www.w3schools.com/c/ref_stdio_sprintf.php)|Writes a formatted string into a `char` array|
|[sscanf()](https://www.w3schools.com/c/ref_stdio_sscanf.php)|Reads a formatted string from a `char` array and writes it into a number of memory locations|

Para abrir um arquivo, utilizamos a função `fopen()` , que recebe como parâmetros o nome do arquivo e o modo de abertura:

![[image 51.png|image 51.png]]