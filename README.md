
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/119726639-b72bf980-be47-11eb-8550-758b001ec143.png">
</div>
<br>
<img src="https://img.shields.io/static/v1?label=dart&message=Language&color=blue&style=for-the-badge&logo=Dart"/>


O Dart é uma linguagem de script, type safe, multiparadigma e orienta a objetos, desenvolvida e mantida pela Google. Tem ganhado bastante popularidade por ser utilizada em conjunto com o Flutter, um dos FrameWorks mais populares da atualidade para desenvolver aplicações mobile nativas.

Por ser multeplataformas, o Dart acompanha duas ferramentas, ou soluções, que possibilitam o seu uso: o Dart Native e o Dart Web. Tendo como principal recurso a máquina virtual responsável por compilar a linguagem no Just-in-Time(JIT) process, além do AOT(Ahead-of-Time), este sendo responsável por converter o código escrito em Dart para machine code/código nativo, seja em Android ou IOS, ou para JavaScript, falando específicamente do Dart Web.


<h2>Preparando o Ambiente</h1>


A seguir estão dispostos uma série de passos para a instalação das ferramentas e preparo do ambiente de desenvolvimento. Não sendo cem porcento necessário seguir as intalações para iniciar o estudo da linguagem, mas recomendado. 

Uma forma mais simples de executar códigos dart é ter uma IDE(recomendo o vscode) e plugins que aceitem a sintaxe do dart. Com isso só é preciso criar uma file com a extenção .dark e executá-la com o comando <b><i>dart run</i></b>. Não sendo necessário a criação de um projeto para tal.


<h2>Instalação do Dart-SDK</h1> 


O Dart-SDK é uma biblioteca de ferramentas de linha de comando, comumente utilizada em aplicações Web, Server ou de criação de Script, sendo um ambiente recomendado(não obrigatório) para uso da linguagem.


<h3>Chocolatey</h3>


O Chocolatey é um gerenciador de pacotes para o Windows, necessário no processo de instalação do Dart Software Development Kit. O link a seguir indica o passo a passo pra obter a ferramenta: <i>[Instalar Chocolatey](https://chocolatey.org/install)</i>.

  
Verificar instalação


    choco -v


Instalar Dart-SDK 


    choco install dart-sdk


<h2>App Dart-SDK</h1> 


A partir deste ponto, é possível utilizar os comandos Chocolatey para executar uma aplicação Dart-SDK. Sendo assim, acesse um diretório desejado através do cmd e execute:


    dart create -t console-full cli


<h2>Extensão Dart</h2>


Antes de executar o app criado, é importante ter instalado um editor de código(sendo o vscode o mais recomendado) e a extensão da linguagem utilizada:

<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/120421361-844c9e80-c33c-11eb-9507-c10fa62f84f7.png">
</div>


Com os pacotes e o ambiente devidamente definidos e intalados, execute os comandos a seguir para rodar a aplicação:


    cd cli
    dart run


<h2>Hello World</h2>


Uma forma prática de entender a estrutura mais básica de uma linguagem de programação é o popular Hello World, sendo este executado da seguinte forma no Dart:


      void main() 
    {
      print('Hello World');
    }


<h3>Explicando</h3>


<h3>void</h3> 

Por ser uma linguagem fortemente tipada a definição de tipos se aplica inclusive aos métodos, sendo um método void definido por não retornar valor;<br>

<h3>main()</h3>

Método de execução padrão do arquivo, sendo o primeiro a ser chamado no run time;<br>

<h3>print()</h3>

Método padrão de impressão de valor;<br>

<h3>;</h3>

Um detalhe muito importante da linguagem Dart é a presença constante do ponto e vírgula após o fim de um bloco de execução, do contrário é retornado um erro de sintaxe;


<h2>Conceitos</h2>


Nesse ponto iremos entender as estruturas e os aspectos que compõem a linguagem Dart, seus tipos e variações. É bastante importante manter esses aspectos em mente durenate o decorrer da leitura:


 Tudo o que pode ser acoplado a uma variável é um objeto, e todo objeto é uma instância de uma classe, mesmo números, funções e null são objetos;

 Apesar de ser fortemente tipada, a definição de tipos é opcional no Dart, já que a linguagem pode inferir tipos a partir dos dados recebidos;

 É possível tornar uma variável nullable usando o marcador (?) no fim da sua definição de tipo. O oposto disso é definir o marcador (!). Por exemplo: int? (integers ou nullable)  /  int x = nullableButNotNullInt!;

 O Dart suporta tipagem genérica, como List<int>(uma lista de integers) ou List<Object>(uma lista de objetos de qualquer tipo);

 O Dart suporta funções de alto nível(como main()), assim como funções amarradas a classes ou objetos(static e instâncias de métodos, respectivamente). Também é possível criar funções dentro de funções(funções aninhadas ou locais);

 Da mesma forma, o Dart suporta variáveis de alto nível, assim como variáveis amarradas a uma classe ou objeto(static e variáveis instanciadas). Variáveis intanciadas são muitas vezes conhecidas como fields ou propriedades;

 Diferente da linguagem Java, o Dart não possui as palavras-chave public, protected e private. Se um identificador inicia com uma underline(_), ele passa a ser private;

 Identificadores podem iniciar com uma letra ou underline(_), seguida de qualquer combinação de caracteres e dígitos; 


<h2>Built-in Types</h2>


O Dart possui os seguintes tipos internos:


<h3>Number</h3>


int - Valores inteiros não maiores que 64 bits, dependendo da plataforma:


    int x = 1;
    int hex = 0xDEADBEEF;
    int exponent = 8e5;


double - Valores decimais:


    double y = 1.1;
    double exponents = 1.42e5;


<h3>String</h3>


Uma string Dart (object String) contém uma sequência de unidades de código UTF-16:


    string s1 = 'Single quotes work well for string literals.';
    string s2 = "Double quotes work just as well.";
    string s3 = 'It\'s easy to escape the string delimiter.';
    string s4 = "It's even easier to use the other delimiter.";


<h3>Interpolação de String</h3> 


A interpolação permite acessar valores identificados por unidades de armazenamento dentro de um string type:


    string greeting = "String";
    string person = "Interpolation";
    
    print('${greeting}, ${person}!');
    
    //Output: String Interpolation


 <div align="center">
  Obs: a interpolação é feita tanto entre aspas simples quanto entre aspas duplas
 </div>


<h3>Booleans</h3>


Para representar valores boolean o Dart possui o marcador bool, com dois tipos definidos: true e false. Exemplos de definição de um bool:


    // Verifica string vazio

    var fullName = '';
    assert(fullName.isEmpty);
    
    // Verifica valor menor ou igual a 0

    var hitPoints = 0;
    assert(hitPoints <= 0);
    
    // Verifica valor null

    var unicorn;
    assert(unicorn == null);
    
    // Verifica NaN
    
    var iMeantToDoThis = 0 / 0;
    assert(iMeantToDoThis.isNaN);


<h3>Runes</h3>


Em Dart as Runes expõem o código unicode de uma string. O unicode define um valor numérico único para cada letra, dígito e símbolo usado em todo o sistema de escrita. Um unicode é normalmente representado da seguinte forma:


    \uXXXX


Onde XXXX é um valor hexadecimal de 4 dígitos. Por exemplo: \u{1f606}, que respesenta o seguinte emoji :satisfied:. O Dart possui um módulo específico para trabalhar esse tipo de dado, sendo definido abaixo:


    import 'package:characters/characters.dart'; <==
    ...
    var hi = 'Hi 🇩🇰';
    print(hi);
    print('The end of the string: ${hi.substring(hi.length - 1)}');
    print('The last character: ${hi.characters.last}\n');

    //Console

    $ dart bin/main.dart
    Hi 🇩🇰
    The end of the string: ???
    The last character: 🇩🇰


<h3>Symbols</h3>


Um objeto Symbol representa um operador ou idetificador declarado em um programa Dart, dificilmente utilizados fora de contextos específicos de desenvolvimento. Para definir um Symbol como identificador usa-se # seguido do identificador:


    #radix
    #bar


<h3>Null</h3>


O Dart possui um recurso chamado de Null Safety, o qual define que as variáveis de um código Dart são non-nullable, ou não anuláveis, a menos que sejam definidas como tal.

Com o Null safety todas as variáveis do código a seguir são non-nullable:


    // Com o Null-safe, nenhum destes podem ser null

    var i = 42;
    String name = getFileName();
    final b = Foo();

Para indicar que uma variável aceita um nullable usa-se o marcador ? em conjunto com a declaração do seu tipo:


    int? aNullableInt = null;


<h3>Dynamic</h3>


O tipo dynamic define a aceitação de todos os demais tipos a uma variável, dando a linguagem Dart a característica de dinamicidade:


    dynamic nome = "Caio Rolla";
    
    dynamic idade = 22;
    
    print(nome); // Caio Rolla
    
    print(idade); // 22
    
    idade = "22 anos";
    
    print(idade); // 22 anos


<h2>Operadores Aritméticos</h2>


O Dart suporta os operadores aritméticos usuais, como mostrado abaixo:


<h3>Adição + </h3>


    //Soma os operandos

    assert(2 + 3 == 5);
 

<h3>Subtração - </h3>


    //Subtrai os operandos

    assert(2 - 3 == -1);


<h3>-expr</h3>


    //Inverte o sinal da expressão


<h3>Multiplicação * </h3>


    //Multiplica os operandos

    assert(2 * 3 == 6);


<h3>Divisão / </h3>


    //Divide os operandos

    assert(5 / 2 == 2.5); // Resulta em um double


<h3>Divisão Inteira ~/ </h3>


    //Retorna um integer

    assert(5 ~/ 2 == 2); // Resulta em um int


<h3>Resto % </h3>


    //Retorna o resto da operação

    assert(5 % 2 == 1); // Resto


<h2>Incremento</h2>


O operador de incremento incrementa seu operando em 1. O operador de incremento é suportado em duas formas: 


<h3>Pré Fixado ++X</h3>


O resultado de ++ x é o valor de x após a operação, como mostra o exemplo a seguir:


    var a, b;
    
    a = 0;
    b = ++a; 
    assert(a == b); // 1 == 1


<h3>Pós Fixado X++</h3>


O resultado de x ++ é o valor de x antes da operação, como mostra o exemplo a seguir:


    var a, b;

    a = 0;
    b = a++; 
    assert(a != b); // 1 != 0


<h2>Decremento</h2>


O operador de decremento diminui seu operando em 1. O operador de decremento é suportado em duas formas: 


<h3>Pré Fixado --X</h3>


O resultado de --x é o valor de x após a operação, como mostra o exemplo a seguir:


    a = 0;
    b = --a; 
    assert(a == b); // -1 == -1
    

<h3>Pós Fixado X--</h3>


O resultado de x-- é o valor de x antes da operação, como mostra o exemplo a seguir:


    a = 0;
    b = a--; 
    assert(a != b); // -1 != 0


<h2>Operadores Relacionais</h2>


Relacionam operandos tendo como retorno um boolean, sendo true caso a operação seja verdadeira e false caso seja falsa. Eles são:


<h3> Igualdade == </h3>


Retorna true caso o valor numérico dos operandos seja igual:


    assert(2 == 2); //output: true


<h3> Diferença != </h3>


Retorna true caso o valor numérico dos operandos for diferente:


    assert(3 != 3); //output: false 


<h3> Maior que > </h3>


Retorna true caso o valor numérico do operando da esquerda seja maior que o da direita:


    assert(3 > 2); //output: true


<h3> Menor que < </h3>


Retorna true caso o valor numérico do operando da esquerda seja menor que o da direita:


     assert(4 < 3); //output: false


<h3> Maior ou igual >= </h3>


Retorna true caso o valor numérico do operando da esquerda seja maior ou igual ao do operando da direita:


     assert(3 >= 3); //output: true


<h3>Menor ou igual <= </h3>


Retorna true caso o valor numérico do operando da esquerda seja menor ou igual ao do operando da direita:


     assert(4 <= 3); //output: false


<h2>Operadores de Teste</h2>


Os operadores type test definem tipos no processo compilação. Eles são definidos em três:


<h3>as</h3>


    //Typecast

    (employee as Person).firstName = 'Bob';


<h3>is</h3>


    //Retorna true caso o objeto tenha o tipo especificado

    if (employee is Person) {
      // Type check
      employee.firstName = 'Bob';
    }


<h3>is!</h3>


    //Retorna true caso o objeto tenha o tipo diferente do especificado

    if (employee is! Person) {
      // Type check
      employee.firstName = 'Bob';
    }


<h2>Operadores de Auto Atribuição</h2>

Operações que relacionam dois operandos de forma que o primeiro operando recebe o valor da operação entre seu valor e o de um segundo operando:


     x  =   y | O operando x recebe o operando y
     x  -=  y | O operando x recebe a subtração entre os operandos x e y
     x  /=  y | O operando x recebe a divisão entre os operandos x e y
     x  %=  y | O operando x recebe o resto da divisão entre os operandos x e y
     x  +=  y | O operando x recebe a soma entre os operandos x e y
     x  *=  y | O operando x recebe a multiplicação entre os operandos x e y
     x  ~/= y | O operando x recebe um int da divisão entre os operandos x e y
 

<h2>Operadores Lógicos</h2>


Os operadores lógicos definem um valor boolean como o retorno entre uma operação entre dois operandos, sempre retornando true ou false:


<h3>Negação !</h3>


    if(!data) {
        ...
    }


Se o valor chamado data for definido como true, ele passa a ser false, e vice versa. 


<h3>Disjução ||</h3>


    if(!data || value) {
        ...
    }


Chamado de OR lógico, só retorna true caso um dos operandos corresponda ao valor boolean true.


<h3>Conjunção &&</h3>


    if(!data && value) {
          ...
      }


O operador de conjunção, também chamado de AND lógico define que o resultado de uma operação como true se ambos os operandos forem verdadeiros.


<div align="center">
  <h1>Unidades de Armazenamento</h1>
</div>


<h2>Variáveis</h2>


Assim como em qualquer linguagem de programação, as variáveis em Dart são uma unidade de armazenamento e de referência de dados, tendo aqui algumas características importantes a serem mencionadas.


<h2>Declarando Variáveis</h2>


A variável a seguir é inicializada com a palavra-chave var(reservada para essa função), um identificador e um valor inicial. Esta comtém uma referência ao valor que carrega:


    var data = 'Dart';


A definição do tipo dessa variável é inferida pelo valor que ela carrega, sendo nesse caso um string. Por possuir uma tipagem forte, o Dart permite a definição de tipos de forma implícita e explícita. Sendo a variável acima um exemplo da tipagem explícita. A seguir estão alguns exemplos de variáveis com um tipo pré definido:


    // O tipo Object não possui tipagem restrita, aceitando qualquer tipo

    Object data = 'Dart';

    // String

    String data = 'Dart';

    // Double

    Double data = 1.78;

    // Int

    Int data = 1;

    // O tipo num define que a variável aceita qualquer valor numérico, seja int ou double

    num pi = 3;
    pi = 3.14;


<h2>Variáveis não Iniciadas</h2>


Uma variável não iniciada é definida por uma unidade de armazenamento e referência cujo espaço na memória não foi ocupado no momendo da declaração, sendo possível oculpar este valor posteriormente:


    int empty;

    empty = 1938;


<h2>Variáveis Late</h2>


O Dart possui, desde a versão 2.12, o modificador Late, que é usado em dois casos: 

- Declaração de variáveis non-nullable que são iniciadas após sua delcaração;
- Lazily initializing de uma variável;

Normalmente o controle de análise de fluxo do Dart detecta quando uma variável é definida com valor non-nullable antes de ser utilizada, mas esse processo nem sempre é eficaz. Isso noramalmente ocorre com variáveis de alto nível e vaiáveis instanciadas.

Caso o desenvolvedor esteja seguro de que a variável foi definida antes de ser usada, tendo a discordância do Dart, é possível corrigir o erro definindo a variável como late. Exemplo:


    late String description;
    
    void main() {
      description = 'Feijoada!';
      print(description);
    }


<h2>Const</h2>


Definir um valor como fixo ou constante demanda o uso da palavra chave const, dando à unidade de armazenamento e referência a característica de imutabilidade do seu valor em tempo de compilação:


    // Sem definição de tipo

    const name = 'Bob';

    // Com definição de tipo

    const String nickname = 'Bobby';


<h1>Functions</h1>


Por ter uma forte presença da orientação a objetos, mesmo as funções são objetos possuidoras de tipos. Isso torna possível a atribuir funções a variáveis ou torná-las argumentos em outras funções. Abaixo segue a estrutura básica de uma função no Dart:


    type functionName(arguments) {
      return value;
    }


Um ponto a se ater é que funções tipadas sempre devem possuir um valor equivalente a seu tipo como retorno. Além disso, funções podem ser definidas como type annotation ou void no Dart, podendo ser escritas de forma mais encurtada, caso possuam apenas uma expressão:


<h3>Type Annotation</h3>


    //Omite o tipo de retorno

    functionName(arguments) {
      return value;
    }


<h3>Void Functions</h3>


    //Não possui retorno

    void functionName(arguments) {
        ...
    }


<h3>Shorthand Syntaxs</h3>


    //Caso a função tenha apenas uma expressão 

    type functionName(arguments) => value;


<h2>Parameters</h2>


Uma função pode ter qualquer número de required positional parameters. Estes ainda podem ser seguidos de named parameters ou por optional positional parameters (mas não ambos):


<h3>Named Parameters</h3>


Named Parameters são opcionais a não ser que sejam definidos como required. Abaixo há a definição da sintaxe de uma função com Named Functions:


    void functionName({type <paramName>, type <paramName>}) {

      ...    
        
    }


Ao instânciar uma função que recebe parâmetros opcionais, usa-se o identificar do parâmetro e o valor a ser passado:


    functionName(paramName: value, paramName: value);


<h3>Required Parameters</h3>


São definados quando o valor recebido via parâmetro é obrigatório, gerando um issue caso não seja disponibilizado:


    type functionName({Key? key, required Widget child})


<h3>A Função main()</h3>


Todas as aplicações devem conter a já mencionada função de alto-nível do tipo main(), cuja função é agir como o entrypoint do app. Retornando void, a função main também possui um parâmetro opcional do tipo List<String> como argumento:


    void main() {
      print('Hello, World!');
    }


<h3>Funções Anônimas</h3>


Boa parte das funções são definidas como named, ou nomeadas, como a própria main(). Uma froma alternativa de criação de funções é omitindo seu nome ou identificador, sendo assim chamada de anonymous function, lambda ou closure. 


    ([[Type] param1[, …]]) {

      ...

    };


O exemplo abaixo define uma função anônima com um parâmetro de tipo anônimo. A função, invocada para cada item da lista, printa uma string incluindo o valor no index especificado:


    const list = ['apples', 'bananas', 'oranges'];
    list.forEach((item) {
      print('${list.indexOf(item)}: $item');
    });

    //Output:

    0: apples
    1: bananas
    2: oranges


<h3>Lexical scope</h3>


O Dart é uma linguagem com escopo léxico, o que significa que o escopo das variáveis é determinado estaticamente, seguindo o layout do código escrito. Basicamente, as variáveis declaradas anteriormente, ou dentro das chaves de uma estrutura de código, são definidas como parte do escopo:


    bool topLevel = true;
    
    void main() {
      var insideMain = true;
    
      void myFunction() {
        var insideFunction = true;
    
        void nestedFunction() {
          var insideNestedFunction = true;
    
          assert(topLevel);
          assert(insideMain);
          assert(insideFunction);
          assert(insideNestedFunction);
        }
      }
    }


<h1>Declarações de Controle de Fluxo</h1>


O controle do fluxo de dados é, em suma, um dos aspectos mais importantes da programação. O Dart possui as seguintes estruturas para controle de fluxo de dados:


<h2>If-else</h2>


    if ( booleanExpression ) {
      
      ...
      
    } else if ( anotherBooleanExpression ) {
      
      ...


    } else {
      
      ...

    }


<h2>Exepressões Condicionais</h2>


Além dos expressões padrão if-else o Dart conta com dois operadores lógicos que exercem a mesma função, substituindo-as em determinadas situações:


<h3>condition ? expr1 : expr2</h3>


Se condition tiver true como valor, o valor de expr1 é retornado, de outra forma, o valor de expr2 é retornado:


    var visibility = isPublic ? 'public' : 'private';


<h3>expr1 ?? expr2</h3>


O valor de expr1 é retornado caso ele seja diferente de null, de outra forma, o valor de expr2 é retornado:


    String playerName(String? name) => name ?? 'Guest';


<h2>For Loops</h2>


    var message = StringBuffer('Dart is fun');
    for (var i = 0; i < 5; i++) {
      message.write('!');
    }


Os fechamentos dentro dos loops for do DART capturam o valor do índice, evitando uma armadilha comum encontrada no JavaScript:


    var callbacks = [];
    for (var i = 0; i < 2; i++) {
      callbacks.add(() => print(i));
    }
    callbacks.forEach((c) => c());


O output seria 0 e depois 1, como esperado. Em contraste, se o exemplo fosse feito em JavaScript, o retorno seria 2 e depois 2.


<h3>For-in</h3>


Se o objeto de interação for um iterable(como um List ou Set), e se não é preciso saber o contador de interação atual, é possível utilizar o for-in:


    for (var varName in iterable) {
      
      ...

    } 


<h2>While e do-while</h2>


Um loop while avalia a condição antes do loop:


    while (booleanExpression) {

      ...

    }


Um do-while avalia a condição depois do loop:


    do {
      
      ...

    } while (booleanExpression);


<h3>Break e continue</h3>


O <b><i>break</i></b> é utilizado para quebrar um loop em execução quando o valor definido em uma condicional é encrontrado:


    while (true) {
      if (booleanExpression) break;
      
      ...

    }


O <b><i>continue</i></b> é utilizado para pular para o próximo loop quando o valor definido em uma condicional é encrontrado:


    for (int i = 0; i < candidates.length; i++) {
      var candidate = candidates[i];
      if (booleanExpression) {

        continue;

      }
      candidate.interview();


<h2>Switch-case</h2>


O Switch no Dart compara integers, strings ou constantes de tempo de compilação usando o operador de igualdade(==). Todos os objetos comparados devem ser instâncias da mesma classe(e não de qualquer um de seus subtipos), e a classe não pode sobrepor o operador. 

Qualquer uma das clausulas <b><i>case non-empty</i></b> têm como regra terminar com um <b><i>break</i></b>. Outros meios válidos para termiar um non-empty case é usando o <b><i>continue</i></b>, o <b><i>throw</i></b> ou um <b><i>return</i></b>.

Caso nenhum case combine com o valor de comparação, é executada uma clausula <b><i>default</i></b>:


    var command = 'OPEN';
    switch (command) {
      case 'CLOSED':
        executeClosed();
        break;
      case 'PENDING':
        executePending();
        break;
      case 'APPROVED':
        executeApproved();
        break;
      case 'DENIED':
        executeDenied();
        break;
      case 'OPEN':
        executeOpen();
        break;
      default:
        executeUnknown();
    }


<h2>Try-Catch</h2>


O Catch captura uma exceção e impede que ela se propague, a menos que ela seja relançada. Capturar essa exceção permite que ela seja tratada:


    try {
      
      ...

    } on Exception {
     
      ...
     
    }


Para tratar um código que pode lançar mais de um tipo de exceção, é possível especificar múltiplas clausulas catch. A primeira clausula que combinar com o tipo de objeto lançado trata a exceção. Se a clausula catch não especificar um tipo, qualquer objeto lançado pode ser tratado por ela:


    try {
      
      ...

    } on Exception {

      // Uma exceção expecífica

      ...

    } on Exception catch (e) {

      // Qualque outra exceção

      print(e);

    } catch (e) {

      // Clausula de tipo não especificado, trata todos

      print(e);

    }


<h3>Finally</h3>


Para garantir que o trecho de código será executado mesmo se uma exceção for lançada, usa-se a clausula finally. Se a exceção não combinar com a nenhum dos cases, a exceção é propagada depois que a clausula finilly for executada:


    try {
      
      ...

    } finally {

      // Sempre ocorre, mesmo se uma exceção for lançada
      
      ...

    }
    

<h1>Collections</h1>

Collections são implementações de estruturas de dados, normalmente associadas ao armazenamento de informações. Cada collection possui um tipo associado e define um tipo, sendo possível agrupa-los gerando collections que armazenam collections por exemplo. O Dart possui os collections a seguir:


<h2>List</h2>


A definição para uma List é uma coleção indexável de objetos com um length, basicamente um Array, cujos principais tipos são:

- Lists de Comprimentos Fixos;
- Lists de Comprimento Cultivaveis ou de Tamanho não Fixo;

Um array, vetor ou variável composta em Dart é definido como uma lista de objetos, portanto, recebendo da linguagem o identificador <b><i>List</i></b>, que pode agrupar basicamente qualquer built-in type do Dart. Há formas distintas de declarar um List em Dart:


    // Sem definição de tipo

    List numbers = [1, 2, 3];

<br>

    // Com definição de tipo

    List <num> numbers = [1, 2, 3];

    List<int> numbers = [1, 2, 3];

    List<String> names = ["Victor", "Carla", "Pedro"];

<br>

    // List de collections

    List<Map> employees = [

      {'Nome': 'Victor Santos', 'idade': 20, 'Profissao': 'Dev'},
      {'Nome': 'Felipe Maia', 'idade': 38, 'Profissao': 'Líder Técnico'},
      {'Nome': 'Luana Martins', 'idade': 21, 'Profissao': 'UI/UX Designer'}

    ];

<br>

    // List de Objetos

    class Products {
      String nome;
      double preco;
    
      Products(this.nome, this.preco);
    }
    
    List<Products> listaDeCompras = [
    
    // Products(item, preco)
    
      Products("Feijão", 7.80),
      Products("Arroz", 4.50),
      Products("Macarrão", 3.45),
      Products("Frango", 8.90)
    ];


<h3>Spread Operator</h3>


O Spread define uma associação entre lists, tendo como resultado um liste apenas. O length dessa associação é equivalente aos indices de ambas as listas somados:


    List name = ['Victor'];
    List names = ['Maria', 'Marcos', ...name];

    void main() {

      print(names.length); // Spread Operator

    }

    //OutPut: 

    3


<h3>Trantando Lists</h3>


Assim como em boa parte das linguagens que tratam de vetores, o dart conta com uma série de métodos e atributos para tratar essas estruturas. Abaixo estão listados alguns dos quais se relacionam com o tipos de list:


<h3>Constructors</h3>


Estruturas de criação de um List com diferentes restrições:

|        Constructor                                      |                                   Descrição                                     |
| ------------------------------------------------------- | ------------------------------------------------------------------------------- |
|  List[ type length ]                                    |  Cria um List de comprimento definido                                           | 
|  List.empty()                                           |  Cria uma nova lista vazia de tamnho fixo                                       |
|  List.filled( type length value )                       |  Cria um List de tamanho fixo com comprimento definido e preenche cada posição  |
|  List.from( iterables elements )                        |  Cria um List de tamanho cultivável contendo todos os elements                  |
|  List.generate( type length, E generator(type index) )  |  Gera uma lista de tamanho cultivável com valores                               |
|  List.of( iterable <E> elements )                       |  Cria um List de tamanho cultivável a partir de elements                        |
|  List.unmodifiable( iterable elements )                 |  Cria um List inalterável contendo todos os elements                            |


<h3>Proprieties</h3>


Atributos de consulta dos lists:

|       Proprieties       |    Valor de Retorno    |                                   Descrição                                      |
| ----------------------  | ---------------------- | -------------------------------------------------------------------------------- |
|  .first                 |  E                     |  Retorna o primeiro elemento                                                     | 
|  .hashCode              |  int                   |  Retorna um intenger que representa o código hash para o objeto list em questão  |
|  .isEmpty               |  bool                  |  Retorna um boolean true se não houver elementos nesta conllection               |
|  .isNotEmpty            |  bool                  |  Retorna um boolean true se houver amenos um elemento do collection              |
|  .iterator              |  iterator              |  Retorna um novo Iterator que permite iterar os elementos do Iterable            |
|  .last                  |  E                     |  Retorna o último elemento                                                       |
|  .length                |  int                   |  Retorna um intenger que representa o número de objetos no List                  |
|  .reversed              |  iterable<E>           |  Um Iterable do objeto List na ordem reversa                                     |
|  .single                |  E                     |  Verifica se há apenas um elemento no Iterable e retorna esse elemento           |
 

<h3>Methods</h3>

Métodos de execução de um List:

|         Methods         |                                    Descrição                                            |
| ----------------------  |  -------------------------------------------------------------------------------------- |
|  add(value)             |   Adiciona um valor ao final do List, extendendo o tamanho em 1                         | 
|  addAll(Interable)      |   Adiciona todos os objetos de um interable ao fim de uma list, extendendo seu tamanho  |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |
|                         |                                      |


<h2>Map</h2>


Em geral um map é um objeto que associa chaves e valores, ambos podendo ser de qualquer tipo. Bastente parecido com um List, o Map possui a propriedade de ter indices customizaveis únicos, o que os diferencia. A seguir há exemplos de declarações de Maps:


    var movies = {

    // Chave: Valor
    
      'first': 'The God Father',
      'second': 'Good Fellas',
      'third': 'The Irishman'
    };
    
    var characters = {
      1: 'Vito Corleone',
      2: 'Jimmy Conway',
      3: 'Frank Sheeran',
    };
    
    void main() {
      print(movies['first']);
      print(characters[1]);
    }

    //OutPut:

    The God Father
    Vito Corleone


<h2>Set</h2>


Um set é uma coleção não ordenada de itens únicos, semelhante a um array ou objeto, com métodos e atributos próprios. Estes usados para adicionar, excluir e alterar elementos. A seguir há exemplos de declarações do Set type:
    
    
    //Set vazio

    Set<String> names = {}; 
    var names = <String>{};

    //Set preenchido

    var halogens = {'fluorine', 'chlorine', 'bromine', 'iodine', 'astatine'};


<div align="center">
  <h1>Orientação a Objetos</h1>
</div>

<!-- <div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/129132771-db53a2d1-9b16-4370-bf68-b762da33799d.png">
</div> -->


<h2>Classes</h2>


Por ser uma linguagem orintada a objetos, o Dart conta com todos os recursos padrões do paradigma, como Classes, Constructors, herança baseada em hierarquia, além de muitos outros conceitos. Sendo uma classe a matriz de criação de um objeto, pode-se dizer que os objetos possuem membros, sendo estes os métodos ou funções, e os dados ou atributos que a classe permite. A declaração de uma classe no Dart se dá pelo modelo a seguir


    class ClasseName {
      
     //Attributes

     ...

     //Methods
     
     ...
    
    }


Ao definir uma classe e seus membros, é possível utilizá-la como a definição de tipo de um novo objeto. Com isso, os atributos e métodos da classe são herdados por esse objeto. Para gerar um objeto com base em determinada classe no Dart, se faz uso do identificador dessa classe seguido de um identificar para o objeto em si. E, opcionalmente, usa-se a keyword <strong>new</strong>, sendo seguida do tipo recebido pelo objto, este sendo obrigatório:


    class ClasseName {

      //Attributes

      String identifire;

      //Methods

      ...

    }

    ClassName objectName = <new> ClassName();
    objectName.identifire = 'Some data';


Um padrão da orintação a objetos em muitas linguagens de programação é a herança por instanciação, ou uso do (.) para acessar membros da classe, esta sendo usada como matriz de criação do objeto. Este recurso é usado acima de forma bastante simples, onde o objeto(objectName) herda o atributo(identifire) da classe(ClassName). O mesmo conceito pode ser aplicado a um método ou subclasse, mas não a um constructor.


<h2>Membros de Uma Classe</h2>


Os membros de uma classe são os já citados métodos e atributos, respectivamente responsáveis por definir o comportamento dos objetos criados, armazenar e referênciar os atributos dos mesmos, ou mais específicamente dos dados correspondentes aos atributos desses objetos. Estes possuem um nível de acesso distinto de métodos ou variáveis que não compõem o escopo de uma classe. Diferente do padrão de instanciação, dentro de uma classe um membro só pode ser instanciado se este estiver dentro do escopo, sendo precedido da keyword <b><i>this</i></b>. A keyword this define que um membro da própria classe é quem está sofrendo a instância:


    class ClasseName {

      //Attributes

      String identifire;

      //Methods

      void classMethod() {

      this.anotherClassMethod();

      }

      void anotherClassMethod() {

        this.identifire = 'text';

      }

    }


<h2>Métodos e Atributos Estáticos</h2>


Para fazer uso de um membro de uma classe é preciso, antes de mais nada, criar uma instância da classe a qual ele pertence. Isso se o membro em questão for definido como não estático. Um atributo ou método estático, precedido da palavra-chave <strong>static</strong>, descarta a necessidade de uma instanciação da classe de origem. Exemplo:


    class ClassName {
    
    static String identifire = 'Static';
    static method() {
      print('Modifier');
    }

    }
    
    void main() {
    
      print(ClassName.identifire);
      ClassName.method();
    }
    
    //OutPut:
    
    Static
    Modifier


<div align="center">
 Com o a definição de tipo static, a única referência necessária é ao nome da classe.
</div>


<h2>Final</h2>


O modificador final define um valor fixo para determinada unidade de código, não permitindo a redefinição desse valor após sua declaração. Tomando como exemplo um atributo de uma classe, pode-se definir que o modificador final age da seguinte forma:


    class Filme {
      final String title = 'O Poderoso Chafão II';
    }
    
    void main() {
      final Filme filme = new Filme();
      filme.title = 'O Poderoso Chafão III'; //Erro
    
    }

    //Erro

    "'title' can't be used as a setter because it's final.
    Try finding a different setter, or making 'title' non-final."


O final é utilizado como mecanismo de alerta ao desenvolvedor, definindo que o valor correspondente a um final é imutável, sendo o valor final daquela unidade de código


<h2>Usando Constructors</h2>


Um constructor é definido por inicializar um objeto no processo de criação do mesmo, definindo valores, carregando informações que possuem devida importancia, etc. Um constructor também é definido como o primeiro método a ser chamado quando uma classe é instanciada, não sendo obrigatoriamente necessário criá-lo, já que, por padrão, classes já possuem um constructor mesmo que ele não seja definido. Um constructor possui o ClasseName como seu identificador:


    class ClasseName {

      //Attributes

        ...

      //Constructor

      ClassName() {

        ...

      }

      //Methods

        ...

    }

    ClassName objectName = <new> ClassName();


<h2>Exemplo de Uso de Um Constructors</h2>


    class Usuarios {
      // Atributos
    
      var usuario;
      var password;
    
      // Constructor
    
      Usuarios(String usuario, String password) {
        this.usuario = usuario;
        this.password = password;
      }

      ------------------- ou -------------------
    
       Usuarios(this.usuario, this.password)

      // Método
    
      authentication() {
        if (this.usuario == usuario && this.password == password) {
          return true;
        } else {
          return false;
        }
      }
    }
    
    void main() {
      Usuarios auth = new Usuarios('Victor', '123456');
    
      if (auth.authentication()) {
        print('Usuário Autenticado');
      } else {
        print('Usuário não Autenticado');
      }
    }


No exemplo acima o cronstructor recebe via parâmetro os valores correspondentes a senha e ao nome do usuário em uma tela de login. Aqui os valores só são passados dessa maneira com o propósito explicativo. Perceba que os valores citados são passados no momento em que o objeto é criado, ou seja, no momento em que um constructor é definido, a declaração de um objeto passa a referencia-lo e não mais à classe.


<h2>Named Constructor</h2>


Um named constructor é uma definição de identificador para o constructor de uma class, não possuindo diferenças diretas na sua função ou forma de execução, normalmente utilizado quando uma classe precisa de múltiplos constructors. Exemplo:


    class ClassName {

      //Attributes

        ...

      //Constructor

      ClassName.ConstructorName() {

        ...

      }

      //Methods

        ...

    }


<h2>Getter e Setter</h2>


O Dart, assim como muitas linguagens de programação modernas possui um recurso de nivelamento de acesso, podendo restringir o contato entre partes do código, deixando o mesmo mais seguro. Uma dessas restrições é tornar um atributo privado, só permitindo seu acesso no escopo da classe que o contém. O getter e o setter executam respectivamente as funções de obter e configurar essas partes, permitindo seu acesso de forma segura:


    class ClassName {

      String _attributeName // Atributo privado
    
      // Getter

      Type get attribute {
        return _attributeName;
      }
      
      ------------------ ou -------------------

      Type get atribute => _attributeName;

      set attributeName(type attributeName) {

            ...

      }

    }


Com isso é possível acessar o atributo _attributeName por meio da variável get, que assume para si o papel de referenciar o atributo privado. E por sua vez, o set configura o que acontece com o atributo em questão, gerando um processo de validação para o mesmo. A seguir há um exemplo mais detalhado:


    class Banco {
    double saldo = 100;
    double _saque = 0;
  
    // Getter
  
    double get saque {
      return _saque;
    }
  
    // Setter
  
    set saque(double saque) {
      if (saque <= 500 || saque < saldo) {
        this.saldo = saldo - saque;
        print('\n Valor sacado: $saque\n');
        print(' -------------------\n');
        print(' Saldo atual:  $saldo');
      } else {
        print('O valor máximo de saque é 500');
      }
    }

    }
    
    void main() {
      Banco conta = Banco();
      conta.saque = 10;
    }


O exemplo acima usa os conceitos de Getter e Setter para simular um saque em uma conta bancária, tendo como private o valor a ser sacado. Este passa a ser acessível através de um get, sendo posteriormente configurado através de um set.


<h2>Herança</h2>


A herança é um dos pilares da orientação a objetos. Desenvolver visando o reaproveitamento de código é extremamente recomendado no contexo da POO, e o Dart possui seu meio para tornar isso possível. Com isso, tendo em mente como as classes são criadas e cosumidas para criar objetos, a seguir veremos como classes filhas podem herdar membros de classes pais aplicando o conseito de herança:


<h3>Extends</h3>


O extends cria uma relação entre duas classes distintas, sendo uma chamada de classe SuperClasse(doadora), e outra chamada de subClasse(herdeira):


    class SuperClasse {
    
      ...
    
    }
    
    class SubClasse extends SuperClasse {
    
      ...
      
    }


Isso estabelece que cada método ou atributo definido como parte da SuperClasse será herdado pela subClasse. A seguir há um exemplo mais detalhado da herança entre classes:


    class Parent {
      String name = 'Vito';
      String surname = 'Corleone';
    }
    
    class Child extends Parent {
      String name = 'Michael';
    }
    
    void main() {
      Child child = new Child();
      print('Nome: ${child.name}');
      print('Sobrenome: ${child.surname}');
    }


    //OutPut:

    Nome: Michael
    Sobrenome: Corleone


Perceba que mesmo sendo uma classe herdeira, a subClasse possui um atributo próprio. Isso permite criar um maior nível de abstração e aproveitamento de um código já criado, não sendo necessário criar os mesmos atributos em classe relacionadas.


<h2>@override</h2>


O @override é um recurso ligado diretamente com classes e a herança de seus membros por outras classes. Com o processo de desenvolvimento de um código há uma série de problemas que surgem, como repetição de identificadores por exemplo, ou a redefinição de um método específico. O @override é responsável por sobrescrever um método, definindo uma nova função para o mesmo. Exemplo:


    class SuperClasse {
    
       void method() {
         print('Something');
       }
    
    }
    
    class SubClasse extends SuperClasse {
      
       @override
       void method() {
         print('Something new');
       }
    }


Quando a subClasse for intanciada, o método herdado será sobrescrito pelo método precedido do @override. A seguir há um exemplo mais detalhado da @override de um método herdado:


    class Food {
      definition() {
        print('Something edible');
      }
    }
    
    class Apple extends Food {
      @override
      definition() {
        print('A fruit');
      }
    }

    void main() {
      Apple apple = new Apple();
      apple.definition();
    }

    //OutPut:

    A fruit


<h2>super.method()</h2>


Em contraponto ao @override, o super é utilizado para tornar acessível um método sobrescrito de uma SuperClasse. Tendo o mesmo princípio, porém, aplicado de forma invertida. Exemplo:


    class SuperClasse {
    
       void method() {
         print('Something');
       }
    
    }
    
    class SubClasse extends SuperClasse {
      
       @override
       void method() {
         super.method();
         print('Something new');
       }
    }


Um <b><i>super</i></b> deve ser declarado dentro de um membro da classe herdeira, específicamente em um método. A seguir há um exemplo mais detalhado do uso do super:


    class Food {
      definition() {
        print('Something edible');
      }
    }
    
    class Apple extends Food {
      @override
      definition() {
        super.definition();
        print('A fruit');
      }
    }
    
    class HotDog extends Food {
      @override
      definition() {
        print('A fastfood');
      }
    }
    
    void main() {
      Apple apple = new Apple();
      apple.definition();
      HotDog hotDog = new HotDog();
      hotDog.definition();
    }

    //OutPut:

    Something edible
    A fruit
    A fastfood


<h2>constructor() : super()</h2>


O super também pode definir uma relação entre classes atráves dos constructors, definindo a passagem de dados de uma subClasse para uma SuperClasse. Exemplo:


    class Pizza {
      String sabor;
    
      Pizza(this.sabor);

      definition() {
        print(this.sabor);
      }
    }
    
    class Margherita extends Pizza {
      String sabor;
    
      Margherita(this.sabor) : super(sabor);

    }
    
    void main() {
      Margherita margherita = new Margherita('Margherita');
      margherita.definition();
    }

    //OutPut:

    Margherita


Isso se dá quando uma subClasse é instanciada tendo um valor recebito em seu constructor, sendo necessário ter este mesmo valor na SuperClasse. No caso acima essa informação é o sabor da pizza criada.


<h2>Classes Abstratas</h2>


Uma classe abstrata é precedida do modificador abstract, este impede a instanciação de membros e da própria classe. Observe um exemplo estrutural de classe abstrata:

 
    abstract class ClassName {
 
      String identifire;
 
      void method() {
 
        ...
        
      }
 
    }


Um detalhe importante sobre classes abstratas é que seus membros também passam a ser abstratos. Um método abstrato, diferente de um método concreto, quando declarado, depende de um @override para poder ser mantido. Do contrario é gerado um erro, exigindo que o método seja sobrescrito:


    abstract class Lapis {
      void escrever();
    }
    
    class Caneta extends Lapis { //Erro
    
    }

    //Erro

    "Missing concrete implementation of 'Lapis.escrever'.
    Try implementing the missing method, or make the class"


Perceba que um método abstrato pode ser declarado sem corpo. Isso ocorre graças a natureza abstrata do mesmo, pois ele sempre vai sofrer um @override. 


<h3>Corrigindo o Erro</h3>


    abstract class Lapis {
      void escrever();
    }
    
    class Caneta extends Lapis {
      @override
      void escrever() {
        print('Texto');
      }
    }
    
    void main() {
      Caneta caneta = new Caneta();
      caneta.escrever();
    }
  
    //OutPut:

    Texto


<h2>Interfaces</h2>


Um interface por definição é uma SuperClasse abstrata cujos membros só são herdados por subClasses concretas que os implementem; como um contrato que deve ter seus termos aceitos após a assinatura. Os métodos ou atributos de uma interface devem sofrer um @override na subClasse que os implementa, do contrário não podem ser utilizados. Para uma melhor definição observe:

   
    abstract class Machine {
      write();
      read();
    }
    
    class SoftwareEngineer implements Machine {
      @override
      write() {
        print('Dart');
      }
    
      @override
      read() {
        print('Machine Code');
      }
    }
    
    class DataAnalyst implements Machine {
      @override
      write() {
        print('Pyton');
      }
    
      @override
      read() {
        print('Machine Code');
      }
    }
    
    void main() {
      SoftwareEngineer softwareEngineer = new SoftwareEngineer();
      softwareEngineer.write();
      DataAnalyst dataAnalyst = new DataAnalyst();
      dataAnalyst.write();
    }


Perceba que não há uma relação direta de herança entre as classes, o que ocorre é a implementação de um modelo de classe(Machine) nos demais. Isso ocorre porquê muitas vezes um trecho de código é definido como estrutura padrão de um sistema(não necessariamente sendo utilizado da mesma forma). O interface evita a repetição desnecessária de código.

Um outro ponto é que uma classe pode tanto implementar quando herdar de classes distintas sem mais problemas, sendo uma alternativa a impossibilidade de herança múltipla


<h2>Mixin</h2>


O mixin é um método de definição de acesso a recursos de uma classe de forma restrita. Assim como um interface, só é possível acessar um mixin caso a relação entre ele e uma classe for explícita, esta sendo declarada pela keyword <b><i>with</i></b>:


    abstract class Cash {
      balance();
    }
    
    class Bank extends Cash {
      @override
      balance() {
        print('Cash');
      }
    }
    
    mixin Score {
      void credit() {
        print('Credit');
      }
    }
    
    class PremiumCustomer extends Bank with Score {}
    
    class CommonCustomer extends Bank {}
    
    void main() {
      print('\nO Cliente Premium tem: \n');
      PremiumCustomer premium = new PremiumCustomer();
      premium.balance();
      premium.credit();
      print('\nO Cliente Common tem: \n');
      CommonCustomer common = new CommonCustomer();
      common.balance();
    }

    //OutPut:

    O Cliente Premium tem: 

    Cash
    Credit
    
    O Cliente Common tem: 
    
    Cash


O exemplo define dois tipos de clientes, um Premium e um Common. Por possuir mais privilégios, um cliente Premium possuiria acesso ao mixin Score, tendo acesso exclusivo ao método credit. O mixin é extremamente importante no processo de declaração de relações e acesso a informação entre classes, tornando o código ainda mais seguro.


<h1>Programação Assíncrona</h1>


Com a necessidade de acesso a recursos externos, os modelos de comunicação e execução visando performance se tornaram cada vez mais importantes para os desenvolvedores. Termos como Threads são bastentes conhecidos dos que já possuem certa experiência, porém, os modelos que envolvem single-thread, multi-thread e outros, ainda são desconhecidos por muitos. Os modelos síncronos e assíncronos possibilitam o uso de diferentes meios para criar um sistema que se comunique, trate e use as informações obtidas.


<h2>Por que o código assíncrono é importante</h2>


O modelo assíncrono, associado ao multi-thread, conta com a vantegem de permitir a execução de uma tarefa enquanto aguarda a finalização de outra. Esta que pode estar buscando ou respondendo uma aplicação externa, sendo mantida em hold enquanto não há uma resposta. Quando há um retorno, a tarefa é retomada do ponto em que havia sido suspensa, permitindo um processo de execução muito mais fluido e eficaz do que o modelo single-thread ofereceria.

Por ser uma linguagem moderna, o Dart conta com um modelo de execução que suporta a programação assíncrona, permitindo que o desenvolvedor trate com muito mais eficácia suas requisições e possíveis erros no processo de consumo de API's exeternas.
A seguir iremos abordar os mecanismos que a linguagem provê na prática:


<h2>O que é uma Future ?</h2>


Uma <b><i>Future</i></b> é a representação do resultado de uma operação assícrona, podendo ter dois estados: uncompleted e completed.


<h3>Uncompleted</h3>


Quando uma chamada em uma função assíncrona é feita, seu resultado é retornado como uma <b><i>uncompleted</i></b> future. Essa future passa a esperar o fim da operação ou lança um erro.


<h3>Completed</h3>


Se a operação assíncrona for bem sucedida, a future resulta em um valor de retorno, caso contrário, resulta em um erro.


<h3>Retornando um Valor</h3>


Uma future de tipo resulta em um valor do tipo <b>T</b>. Por exemplo, uma future de tipo <b><i>Future String </i></b> porduz uma string como valor. Caso uma future não retorne um valor utilizável, esta pode ser declarada como <b><i>Future void </i></b>. 

A seguir temos um exemplo de declaração e uso de uma função Future que retorna um valor:


    Future<void> fetchUserOrder() {

      // Imagine que esta função está buscando informações de um usuário de um service ou base de dados

      return Future.delayed(const Duration(seconds: 2), 
      
      () => print('Café'));
    }
    
    void main() {
      fetchUserOrder();
      print('Buscando o pedido do usuário...');
    }

    // OutPut: 

    Buscando o pedido do usuário...
    //seconds: 2
    Café  


Por possuir um delay proposital, o método <b><i>fetchUserOrde()</i></b> é declarado como uma Future, indicando que essa função pode ser executada em segundo plano e que as demais não precisam esperá-la terminar para serem executadas.


<h3>Retornando um Erro</h3>


Se por alguma razão uma operação assíncrona cair ou achar uma exception, a future irá completar a execução com um erro. A seguir temos um exemplo de declaração de uma Future que completa a execução com uma exception:


    Future<void> fetchUserOrder() {

    // Imagine que esta função está buscando informações de um usuário mas encontrou um bug

      return Future.delayed(const Duration(seconds: 2),
          () => throw Exception('Logout failed: user ID is invalid'));
    }
    
    void main() {
      fetchUserOrder();
      print('Buscando o pedido do usuário...');
    }

    //Output:

    Buscando o pedido do usuário...
    //seconds: 2
    Unhandled exception:
    Exception: Logout failed: user ID is invalid


 A função indica que o ID do usuário é invalido, portanto, há uma exception.


 <h2>async e await</h2>


 As palavras-chave <b><i>async</i></b> e <b><i>await</i></b> fornecem um meio declarativo de definição de funções assíncronas e de uso de seus resultados. É importante se ater às seguintes regras ao fazer uso de async e await:

 * Para definir uma função async, adicione async antes do corpo da função.
 * A palavra-chave await só funciona em funções async.

 A seguir temos um exemplo de declaração de função async:


    void myMethod() async { ... }


Caso a função criada possua uma declaração de tipo, ou seja, um retorno, declare a função como Future T , onde T é o tipo correspondente a seu valor de retorno. Caso o valor de retorno não seja explícito, defina a função como Future void :


    Future<void> myMethod() async { ··· }


Uma função async passa a aceitar a declaração de um await quando definida. O exemplo a seguir mostra como declarar um await:


    Future<void> myMethod() async { 
      print( await createMessage());
    }

    String createMessage() {
      return 'Go learn some code';
    }

    main() {
      myMethod();
    }
    
    //Output:
  
    Go lurn some code


O exemplo a seguir compara as declarções de uma série de funções síncronas e seu resultado com as mesmas funções, porém, declaradas como assíncronas:


<h3>Exemplo de Função Síncrona</h3>


    String createOrderMessage() {
      var order = fetchUserOrder();
      return 'Seu pedido é: $order';
    }
    
    Future<String> fetchUserOrder() =>

       // Imagine uma função mais complexa e lenta

        Future.delayed(
          const Duration(seconds: 2),
          () => 'Café',
        );
    
    void main() {
      print('Buscando o pedido do usuário...');
      print(createOrderMessage());
    }

    //Output:

    Buscando o pedido do usuário...
    //seconds: 2
    Seu pedido é: Instance of 'Future<String>'

  
 <h3>Exemplo de Função Assíncrona com async e await</h3>


    Future<String> createOrderMessage() async {
      var order = await fetchUserOrder();
      return 'Seu pedido é: $order';
    }
    
    Future<String> fetchUserOrder() =>

        // Imagine uma função mais complexa e lenta

        Future.delayed(
          const Duration(seconds: 2),
          () => 'Café',
        );
    
    Future<void> main() async {
      print('Buscando o pedido do usuário...');
      print(await createOrderMessage());
    }

    //Output:

    Buscando o pedido do usuário...
    //seconds: 2
    Seu pedido é: Café


O exemplo assíncrono é diferente de três formas:

* O tipo de retorno para createOrderMessage() muda de um simple String para um Future do tipo String.
* A palavra-chave async aparece antes dos corpos das funções createOrderMessage() e main().
* A palavra-chave await aparece antes da chamada das funções assíncronas fetchUserOrder() and createOrderMessage().


<h3>Fluxo de Execução com async e await</h3>


Uma função async roda sincronicamente até o primeiro await. Isso significa que dentro de um corpo de função assíncrona, todo o código síncrono antes da primeira palavra-chave await é executado imediatamente. A seguir há um exemplo com o qual é possível entender melhor o fluxo de execução assíncrono:


    Future<void> printOrderMessage() async {
      print('Aguardando pedido do usuário...');
      var order = await fetchUserOrder();
      print('Seu pedido é: $order');
    }
    
    Future<String> fetchUserOrder() {
      return Future.delayed(const Duration(seconds: 4), () => 'Café');
    }
    
    Future<void> main() async {
      countSeconds(4);
      await printOrderMessage();
    }
    
    // Você pode ignorar esse método - Sua função é todar o delay visível
    void countSeconds(int s) {
      for (var i = 1; i <= s; i++) {
        Future.delayed(Duration(seconds: i), () => print(i));
      }
    }


Aqui temos basicamente quatro métodos. Três deles, incluindo o main method, são de execução assícrona, ou seja, são Futures que executam ações de acordo com o tempo de retorno das chamadas. O quarto método torna visível o delay de quatro segundos que cada await demora para retornar um valor.


    //Output:

    Aguardando pedido do usuário...
    1
    2
    3
    4
    Seu pedido é: Café


O run inicia no main method, cuja função aqui é executar as demais Futures. Com isso, perceba que por mais que a função print('Aguardando pedido do usuário...') esteja dentro de uma função assíncrona, ela é executado imediatamente após a chamada do método printOrderMessage(). Isso ocorre graças a natureza síncrona da print() function. Já na chamada do método fetchUserOrder(), que também é definido como await, há um delay proposital que demostra sua natureza assíncrona.


<h2>Tratando Erros</h2>


O meio mais utilizado e recomendado para tratar erros em funções async é utilizando o try-catch, graças a possibilidade de tratar erros distintos de diferentes formas. A seguir há um exemplo de uso do try-catch em uma operação assíncrona:


    Future<String> fetchUserOrder() {
       return Future.delayed(const Duration(seconds: 4), () => 'Café');
    }
     
    Future<void> main() async {
     try {
       print('Aguardando pedido do usuário...');
       var order = await fetchUserOrder();
       print(order);
     
     } catch (err) {
       print('Caught error: $err');
     }
    }

    //Output:
    
    Aguardando pedido do usuário...
    //seconds: 4
    Café

