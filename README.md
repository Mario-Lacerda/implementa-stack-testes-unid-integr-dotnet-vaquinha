# Desafio Dio - Implementando sua stack de testes de unidade e integrados em um projeto .NET de Crowdfunding


Para este projeto, vamos usar o Visual Studio 2019 com o pacote NuGet do NUnit.

**Criar um novo projeto .NET Core**

**Projeto de Visual C#**.

Em **Novo Projeto**,  **Aplicativo Web ASP.NET Core** 

**Adicionado o pacote NuGet do NUnit**

 **Gerenciador de Pacotes NuGet** > **Gerenciador de Pacotes**.

No **Gerenciador de Pacotes**,  **Adicionar novo pacote** e pesquisa por **NUnit**.

instala pacote **NUnit** 

## **classe de teste**

Crie uma nova classe de teste chamada **TestesCrowdfunding**.

Na classe de teste, adicione um método de teste chamado **TesteDeposito**.

No método de teste, adicione o código a seguir:

```plaintext
[Test]
public void TestDeposito()
{
    // Cria uma nova conta de crowdfunding.
    CrowdfundingAccount crowdfundingAccount = new CrowdfundingAccount();

    // Deposita 100 reais na conta.
    crowdfundingAccount.Depositar(100);

    // Verifica se o saldo da conta é igual a 100 reais.
    Assert.AreEqual(100, crowdfundingAccount.Saldo);
}
```

## **Executar os testes**



### **Implementando TDD com .NET C# e MVC**

Este artigo descreve como implementar TDD (Test-Driven Development) com .NET C# e MVC.

#### **1. Definição de uma tarefa**

O primeiro passo é definir uma tarefa que deseja implementar. Por exemplo, você pode querer criar um aplicativo web que permita aos usuários criar e gerenciar tarefas.

#### **2. Escreva um teste**

O próximo passo é escrever um teste para verificar a funcionalidade da tarefa que você deseja implementar. O teste deve ser específico, verificável e independente.

#### **3. Implemente o código mínimo para fazer o teste passar**

Nesta etapa, você deve implementar o código mínimo necessário para fazer o teste passar. Não tente implementar todo o código de uma vez. Em vez disso, implemente apenas o código suficiente para fazer o teste funcionar.

#### **4. Refatorar o código**

Depois de fazer o teste passar, você pode refatorar o código para torná-lo mais limpo e fácil de manter.

#### **5. Repetir**

O processo de TDD é iterativo. Depois de implementar um teste, você deve reescrever o teste para torná-lo mais específico e verificável. Você também deve reimplementar o código para garantir que ele ainda funcione corretamente.

### **Aplicação**

Aqui está um exemplo de como implementar TDD com .NET C# e MVC.

- **Definição da tarefa:** Queremos criar um aplicativo web que permita aos usuários criar e gerenciar tarefas.
- **Escrever um teste:** Podemos escrever um teste que verifica se os usuários podem criar uma nova tarefa. O teste deve ser específico, verificável e independente.
- **Implementar o código mínimo para fazer o teste passar:** Nesta etapa, vamos implementar o código mínimo necessário para fazer o teste passar. Vamos criar uma classe de modelo para representar uma tarefa e uma classe de controlador para gerenciar as tarefas.
- **Refatorar o código:** Depois de fazer o teste passar, vamos refatorar o código para torná-lo mais limpo e fácil de manter. Podemos usar o padrão de arquitetura MVC para organizar o código.
- **Repetir:** Vamos repetir o processo de TDD até que todos os testes passem e o código esteja funcionando conforme o esperado.

## **Vantagens do TDD**

O TDD oferece várias vantagens, incluindo:

- Melhor qualidade do código

- Redução de bugs

- Melhor documentação do código

- Maior produtividade

  

##  **Executar Todos os Testes**.

Os testes serão executados e todos eles deverão ser aprovados.

** Implemente a lógica de negócios**

Agora que os testes estão funcionando, podemos implementar a lógica de negócios do aplicativo.

Crie uma nova classe chamada **CrowdfundingAccount**.

Na classe, adicione as propriedades a seguir:

- **Saldo:** O saldo atual da conta.
- **Depósitos:** Uma lista dos depósitos feitos na conta.
- **Saques:** Uma lista dos saques feitos na conta.

**Adicione o método a seguir à classe:**

```plaintext
public void Depositar(double valor)
{
    // Incrementa o saldo da conta.
    Saldo += valor;

    // Adiciona o depósito à lista de depósitos.
    Depositos.Add(valor);
}
```

**Adicione o método a seguir à classe:**

```plaintext
public void Sacar(double valor)
{
    // Decrementa o saldo da conta.
    Saldo -= valor;

    // Adiciona o saque à lista de saques.
    Saques.Add(valor);
}
```

#### **Executar os testes novamente**

Os testes devem ser executados novamente e todos eles deverão ser aprovados.

Test-Driven Development (TDD) é uma abordagem de desenvolvimento de software que começa com a escrita de testes para os requisitos de um sistema. Esses testes são então usados para orientar o desenvolvimento do sistema, garantindo que o código seja escrito de acordo com os requisitos.

.NET C# é uma linguagem de programação de alto nível, orientada a objetos e multiparadigmática. Ela é baseada na linguagem C#, mas adiciona suporte para recursos como herança múltipla, genericidade e varargs.

MVC é um padrão de arquitetura de software que separa as preocupações de apresentação, lógica de negócios e persistência de dados. Isso torna mais fácil para os desenvolvedores trabalharem em projetos de software complexos.

##  Estrutura do projeto

O projeto consiste em três projetos:

- **Projeto de teste:** Este projeto contém os testes de unidade para o sistema.
- **Projeto de modelo:** Este projeto contém as classes de modelo para o sistema.
- **Projeto de controlador:** Este projeto contém os controladores para o sistema.

## a. Testes de unidade

Os testes de unidade são os primeiros testes a serem escritos em um projeto TDD. Eles verificam se as classes de modelo estão funcionando corretamente.

Os testes de unidade são escritos usando o framework de teste NUnit. Os testes são escritos em arquivos de classe com a extensão `.cs`.

O código a seguir mostra um exemplo de teste de unidade para uma classe de modelo:

```plaintext
[Test]
public void TestGetBalance()
{
    // Cria uma instância da classe de modelo.
    Account account = new Account();

    // Define o saldo da conta para 100.
    account.Balance = 100;

    // Verifica se o saldo da conta é 100.
    Assert.AreEqual(100, account.Balance);
}
```

## b. Código de modelo

As classes de modelo são as classes que representam o domínio do problema. Elas são responsáveis por armazenar e manipular os dados do sistema.

O código a seguir mostra um exemplo de classe de modelo:

```plaintext
public class Account
{
    public int Id { get; set; }
    public string Name { get; set; }
    public double Balance { get; set; }
}
```

## c. Controladores

Os controladores são responsáveis por receber as solicitações do usuário e enviá-las para as classes de modelo. Eles também são responsáveis por retornar as respostas do servidor para o usuário.

O código a seguir mostra um exemplo de controlador:

```plaintext
public class AccountController
{
    public async Task<IActionResult> GetAccount(int id)
    {
        // Obtém a conta com o ID especificado.
        Account account = await _accountService.GetAccount(id);

        // Retorna a conta para o usuário.
        return Ok(account);
    }

    public async Task<IActionResult> CreateAccount(Account account)
    {
        // Cria a conta.
        await _accountService.CreateAccount(account);

        // Retorna a conta para o usuário.
        return Ok(account);
    }
}
```

## Executando os testes

Os testes podem ser executados usando o comando `dotnet test` no terminal.

O comando a seguir executa todos os testes no projeto de teste:

```plaintext
dotnet test
```

O comando a seguir executa apenas os testes na classe `AccountTest`:

```plaintext
dotnet test AccountTest.cs
```



## **Conclusões**

Neste artigo, mostramos como implementar uma stack de testes de unidade e integrados em um projeto .NET de Crowdfunding.

Os testes são uma parte importante do desenvolvimento de software, pois ajudam a garantir a qualidade do código.

TDD, .NET C# e MVC são ferramentas poderosas que podem ser usadas para criar aplicativos de software de alta qualidade. Com uma abordagem TDD, você pode garantir que seu código seja escrito de acordo com os requisitos e que seus testes sejam abrangentes. .NET C# é uma linguagem de programação poderosa e flexível que pode ser usada para criar vários tipos de aplicativos de software. MVC é um padrão de arquitetura de software eficaz que pode ajudar a organizar seu código e a melhorar sua produtividade.

Ao implementar testes de unidade e integrados, você pode garantir que seu aplicativo esteja funcionando conforme o esperado e que esteja protegido contra erros.

O TDD é uma abordagem eficaz para o desenvolvimento de software. Ele ajuda a garantir a qualidade do código, reduzir os bugs e aumentar a produtividade. Se você está procurando uma maneira de melhorar sua qualidade de código, vale a pena considerar o TDD.