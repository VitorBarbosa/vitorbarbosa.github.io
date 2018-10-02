---
layout: post
title: .NET Core com testes e cobertura no VS Code (Parte 1)
---

Essa é para quem sempre achou que para ter testes rodando automaticamente e cobertura de código na sua IDE você precisaria de ferramentas caras como o Visual Studio, Resharper, IntelliJ, etc. Não é que essas IDEs e ferramentas não tenham vantagens, mas nesse guia eu queria demonstrar como você pode conseguir coisas muito bacanas sem gastar um centavo. Eu vou fazer esse guia utilizando o Windows, mas todas as ferramentas também estão disponíveis para Linux e Mac OS, e poderá ser seguido nesses sistemas operacionais com poucas adaptações.

O primeiro passo é instalar o [Visual Studio Code](https://code.visualstudio.com/), já muito conhecido entre o pessoal que trabalha com *front-end*, mas ele também possui plugins para trabalhar com muitas linguagens utilizadas no *back-end*.  
Como esse é um projeto .NET Core, o [SDK](https://www.microsoft.com/net/download) também é necessário. Para fazer esse post, eu utilizarei a versão 2.1 do SDK, mas versões posteriores também devem funcionar sem problemas. A sua versão instalada pode ser verificada com `dotnet --version`.
Você vai precisar das seguintes extensões no seu VS Code:
* [C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp) - extensão base para dar suporte mais completo à linguagem no VS Code.
* [Coverage Gutters](https://marketplace.visualstudio.com/items?itemName=ryanluker.vscode-coverage-gutters) - lê o arquivo com a cobertura de código e mostra no canto das linhas se elas estão cobertas por testes ou não.
* [.NET Core Test Explorer](https://marketplace.visualstudio.com/items?itemName=formulahendry.dotnet-test-explorer) - mostra todos os seus testes em um só lugar.

Você também vai precisar do [Coverlet](https://github.com/tonerdo/coverlet/), que irá gerar os arquivos com a informação sobre a cobertura de código.  

O objetivo aqui é ter o feedback instantâneo de enquanto você está escrevendo o código, o projeto será construído, os testes rodados e a cobertura de código atualizada automaticamente.
Para exemplificar, vamos criar um novo projeto de teste.
Crie uma pasta vazia, com o nome do seu projeto, navegue até ela num prompt de comando e digite:
`dotnet new console`
Para criar um novo projeto de linha de comando. Você pode testar o seu projeto digitando `dotnet run`, o que deve mostrar "Hello World!" no console.

Continua no próximo post
<!-- mkdir test
cd test
dotnet new xunit
Depois, digite `dotnet new sln` para criar um arquivo de solução. -->