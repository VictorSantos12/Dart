
<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/119726639-b72bf980-be47-11eb-8550-758b001ec143.png">
</div>
<br>
<img src="https://img.shields.io/static/v1?label=dart&message=Language&color=blue&style=for-the-badge&logo=Dart"/>


O Dart é uma linguagem de script, type safe, multiparadigma e orienta a objetos, desenvolvida e mantida pela Google. Utilizada em diversas stacks do desenvolvimento de aplicações, sendo mais assossiada ao Flutter, um de seus frameworks mais populares, e por consequência ao desenvolvimento mobile. Por ser multeplataformas, o Dart acompanha duas ferramentas, ou soluções, que possibilitam o seu uso: o Dart Native e o Dart Web. Tendo como principal recurso a máquina virtual responsável por compilar a linguagem no Just-in-Time(JIT) process, além do AOT(Ahead-of-Time), esta sendo responsável por converter o código escrito em Dart para machine code/código nativo, seja em Android ou IOS, ou para JavaScript, falando específicamente do Dart Web.


<h2>Preparando Ambiente</h1>


Antes de abortar a sintaxe da linguagem de forma aprofundada é preciso criar um ambiente propício para tal. A seguir estão dispostos uma série de passos para a instalação das ferramentas e preparo do ambiente de desenvolvimento.


<h2>Instalação do Dart-SDK</h1> 


O Dart-SDK é uma biblioteca de ferramentas de linha de comando, comumente utilizada em aplicações Web, Server ou de criação de Script, sendo o ambiente mínimo para uso da linguagem. Os comandos a seguir devem ser executados no PowerShell com permição de administrador:


[Instalar Chocolatey](https://chocolatey.org/) - gerenciador de pacotes para o Windows:

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]  ::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

Verificar instalação

    choco -v

Instalar Dart-SDK 

    choco install dart-sdk


<h2>App Dart-SDK</h1> 


A partir deste ponto é possível utilizar os comandos Chocolatey para executar uma aplicação Dart-SDK. Acesse um diretório desejado através do cmd e execute:

    dart create -t console-full cli


<h2>Extenção Dart</h2>


Antes de executar o app criado, é importante ter instalado um editor de código, sendo o vscode o mais recomendado, e a extenção da linguagem utilizada:

<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/119747559-5f9e8580-be69-11eb-94dd-10999257f7c9.png">
</div>


Com os pacotes e o ambiente devidamente definidos e intalados, execute a comando a seguir para rodar a aplicação:

    cd cli
    dart run


<h2>Hello World</h1>


Uma forma prática de entender a estrutura mais básica de uma linguagem de programação é o popular Hello World, sendo este executado da seguinte forma em Dart:


      void main() 
    {
      print('Hello World');
    }





