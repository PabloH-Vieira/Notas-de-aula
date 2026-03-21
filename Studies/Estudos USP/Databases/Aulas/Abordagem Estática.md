Na abordagem estática não existe o *shift*, como ocorre na abordagem dinâmica.
Ao invés disso, adicionamos um marcador de que aquele registro foi removido.
Uma característica da abordagem estática é informar, no cabeçalho do registro, o próximo RRN disponível. Assim, sabemos o endereço que o próximo registro vai ocupar e se estamos tentando ler um registro que não existe na memória.
Registros marcados como removidos não são imediatamente sobrescritos, a fim de reutilizar o espaço. Para fazer isso, na verdade realizamos a compactação do arquivo (isso acontece de tempos em tempos, até lá é como se o registro estivesse na "lixeira").



~~~ java
int main (void){

return 0;
}


~~~
