# Pull request e Code review 

**INDIVIDUAL**

**Deadline**: XXXXX

**How to submit**: Pull Request no GitHub

**Value**: 

Você tem que escrever um código que será revisado por um de seus colegas. A tarefa tem três etapas:

1. Escrever o código de acordo com a especificação: Você e seu grupo precisam escolher e implementar _uma das três_ funções exigidas abaixo (numeradas F1, F2, F3). Escreva o código e envie um pull request (consulte **especificações** abaixo). Vou designar o revisor para o código. Você será avaliado pela segunda parte desta tarefa e **você não terá permissão para participar dela se não enviar a primeira parte.** Como parte de sua mensagem de pull request, lembre-se de identificar claramente qual função você implementou e fornecer todos os detalhes que achar necessários para a compreensão do revisor.

2. Revisando o código do seu colega: O foco aqui é **CODE REVIEW**, focando em ajudar a melhorar a qualidade do código em diferentes aspectos, verificando a função, legibilidade, manutenibilidade, etc. A revisão do código deve focar fortemente na clareza, comunicação e colaboração. Esta atribuição **não tem como objetivo avaliar o código que você produz**. O foco é praticar a revisão do código e será avaliado mais como uma redação - o tom e o conteúdo importam mais do que a detecção de bugs lógicos. Lembre-se de que estamos falando em Software Livre, então você precisa ser receptivo, usar o tom apropriado (não sendo rude ou rude) e apontar problemas e soluções potenciais.
3. Ajuste seu código de acordo com a revisão recebida

### Detalhes
Cada um de vocês receberá uma função (veja abaixo). Você deve **implementar e criar o pull request** com sua função até o dia **XXXX**. Em seguida, atribuirei as avaliações àqueles que enviaram pull requests e espero que você prepare sua primeira rodada de avaliações até **XXXXX**. Após a revisão, você receberá uma lista de itens que precisam ser alterados (conforme decidido pelo revisor). A parte final da tarefa é implementar as mudanças até **XXXX**. Se você não tiver seu código no dia definido para envio, ou não entregar seu código atualizado, você não receberá crédito pela tarefa.

## Algumas coisinhas a mais:
1. Quero que você pratique o fluxo de trabalho do GitHub também. Portanto, crie um repo em [UTFPR-SL] (https://www.github.com/UTFPR-SL) (Mesmo que não haja nada lá, basta criar o projeto);
2. Faça um fork do projeto (se você ainda não tiver um em seu perfil);
3. Crie uma pasta chamada "**assignPR**" na raiz do projeto e trabalhe dentro desta pasta;
4. Envie seus arquivos e alterações usando comandos git (commits, pushes) ao seu fork e envie-os ao repositório principal criando um  pull request

## Funções (em inglês)

The application you will be writing for is intended to run on a small, inexpensive embedded device that *does not have a floating point unit*. This means that the processor can only do integer arithmetic. However, the device does have a display and *needs to display the result of floating point* arithmetic to the user. Because this is a small inexpensive processor *there is no support for strings or any mathematical library functions*. You must write all the code yourselves *performing all the floating point math with integers only and no strings!* Character arrays, or C strings, can't tell you their size but  they do end with a '\0' character.

The requirements for the code are to write the presented below. All the functions return a boolean value indicating the success or failure of the operation. Improper data is the most likely cause for a function to fail. You may add your own additional helper functions (I had at least a half dozen) but you must include them for the review. Do not change the interface to these functions.

### Conversion Functions (F1)

The two functions, characteristic() and mantissa(), will break a character array into a characteristic and a mantissa. The characteristic for the number 2.351 is 2 and the mantissa is 351 over 1,000. The characteristic for the number 0.0125 is 0 and the mantissa is 125 over 10,000. The characteristic for the number -4.0 is -4 and the mantissa is 0 over 10. These values should be stored in the reference parameters c, numerator and denominator. The C string may include leading or trailing spaces, unary plus or minus signs, integers, or real numbers. Your functions must handle all of these cases. If an invalid string is passed in your function will return false. If the passed in string was valid return true.

```
bool characteristic(char numString[], int& c);
bool mantissa(char numString[], int& numerator, int& denominator);
...
...
char number[] = "123.456";
int c, n, d;
 
//if the conversion from C string to integers can take place
if(characteristic(number, c) && mantissa(number, n, d))
{
    //do some math with c, n, and d
}
else
{
    //handle the error on input
}
```

### Math Functions (F2)

These two functions take as parameters two sets of mantissa and characteristic and a char array to hold the result of the arithmetic operations. The result of the add or subtract should be converted into char's and placed in the result array. The array must end with a '\0'. The 'len' parameter tells how many characters can be placed on the result array. For these functions to return true you must at a minimum store the characteristic of the result. If the result is a non-integer place as many of the digits as will fit in the result after a decimal point. 

```
bool add(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
bool subtract(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len); 
...
...
 
 
char answer[100];
int c1, n1, d1;
int c2, n2, d2;
 
c1 = 1;
n1 = 1;
d1 = 2;
 
c2 = 2;
n2 = 2;
d2 = 3; 
 
//if the C string could hold at least the characteristic
if(add(c1, n1, d1, c2, n2, d2, answer, 100))
{
    //display string with answer 4.166666666...
}
else
{
    //display error message
}
```

### Math Functions (F3)

These two functions take as parameters two sets of mantissa and characteristic and a char array to hold the result of the arithmetic operations. The result of the multiply or divide should be converted into char's and placed in the result array. The 'len' parameter tells how many characters can be placed on the result array. You cannot assume that any of the functions in this assignment will be available to use in your code. Any code that you submit for review cannot contain a call to someone else's code.

```
bool multiply(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
bool divide(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
...
...
char answer[100];
int c1, n1, d1;
int c2, n2, d2;
 
...
...
 
if(divide(c1, n1, d1, c2, n2, d2, answer, 100))
{
    //display string with answer
}
else
{
    //display error message
}
```
