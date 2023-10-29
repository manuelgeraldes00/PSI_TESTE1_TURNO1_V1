# Teste de PSI 1 - Turno 1 - Versão 1

## Informação do aluno

    Nome: ...

Teste termina às 10:45.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    int i = 5 / 2;
    Console.WriteLine($"*\t{i}");

P1 - Resposta

    É impresso: *    2

    Definimos que o valor da variável i equivale à divisão de 5 por 2, cujo resultado é 2,5. 
    Visto que esta é uma variável do tipo int, apenas pode conter números inteiros. 
    O resultado é arredondado para baixo, para o número inteiro mais próximo. Assim sendo, i = 2;
    O método Console.WriteLine é responsável por imprimir uma string. 
    Esta string é contida entre parênteses depois do nome do método.
    O caracter '$' indica que a string contida entre aspas é interpolada. 
    Assim sendo, o valor entre chavetas 'i' corresponde ao valor da variável de mesmo nome.
    A sequência '\t' é uma sequência de escape, que corresponde a um 'tab', ou quatro espaços.
    Considerando tudo isto, é impressa a mensagem entre aspas.
    Esta começa com um asterisco, seguido de um 'tab', e terminando com o valor da variável 'i'.

### P2. Considera o seguinte código com um *bug*

    string s = "2.5";
    int i = Convert.ToInt32(s);

    Console.WriteLine(i);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    Uma possível correção: float i = Convert.ToSingle(s);

    Apesar de ser possível converter strings para números inteiros,
    o valor da variável 's' não pode ser contido numa variável do tipo int.
    O valor '2.5' tem uma casa decimal, logo, é um número real.
    O tipo 'int' apenas contém números inteiros.
    Não é possível esta conversão ocorrer implicitamente, gerando umm erro
    que indica que a string não está no formato correto.
    A correção indicada acima altera o tipo da variável 'i' para 'float'.
    Este tipo real consegue conter o valor da string, sendo apenas necessário
    convertê-lo com o método Convert.ToSingle().

### P3. Escreve um programa que solicite ao utilizador dois números inteiros e apresente a sua soma. Caso o resultado seja um número divisível por 3, deve também ser impressa a mensagem "Múltiplo de 3!"

P3 - Resposta

    // Variáveis para guardar números inteiros e soma de ambos
    int i, j, soma;

    // Pedir o primeiro número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o primeiro número inteiro: ");
    i = Convert.ToInt32(Console.ReadLine());

    // Pedir o segundo número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o segundo número inteiro: ");
    j = Convert.ToInt32(Console.ReadLine());

    // Guardar a soma dos dois valores anteriores na variável correspondente
    soma = i + j;

    // Imprimir resultado da soma
    Console.WriteLine($"{i} + {j} = {soma}");

    // Verificar se soma corresponde a um número divisível por 3
    if (soma % 3 == 0)
    {
      // Imprimir mensagem adicional
      Console.WriteLine("Múltiplo de 3!");
    }

### P4. Tens um repositório git criado localmente, onde estás no ramo **master**. Queres associá-lo ao repositório remoto contido no url 'https://github.com/PSI/OMeuRepositorioRemoto'. Queres também alterar o nome do ramo atual para **main**. Deverás enviar os *commits* já feitos localmente para o repositório remoto. Indica os comandos necessários

P4 - Resposta

    1. Adicionar repositório remoto no URL indicado ao repositório local:
        git remote add origin https://github.com/PSI/OMeuRepositorioRemoto

    2. Alterar o nome do ramo atual para 'main'
        git branch -M main

    3. Enviar commits locais para o repositório remoto
        git push -u origin main
