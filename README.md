# Biblioteca

Bem-vindo ao repositório do projeto **Biblioteca**, uma aplicação web desenvolvida com a arquitetura Model-View-Controller (MVC) utilizando as mais recentes tecnologias do ecossistema .NET.

Este projeto tem como objetivo simular um catálogo de biblioteca clássica, unindo o poder do backend em C# com a dinamicidade e a fluidez de uma Single Page Application (SPA) no lado do cliente (via JavaScript e LocalStorage).

---

##  Tecnologias e Ferramentas Utilizadas

*   **Backend:** C#, .NET Core 10.0, ASP.NET Core MVC
*   **Frontend:** HTML5, CSS3, JavaScript (ES6), Bootstrap 5, jQuery
*   **Banco de Dados:** MySQL (integrado via Entity Framework Core - Pomelo)
*   **Testes e Automação:** Playwright (utilizado para gerar capturas visuais da aplicação)

---

## ⚙️ Pré-requisitos

Antes de iniciar a configuração e execução do projeto, certifique-se de que sua máquina atende aos seguintes requisitos:

1.  **.NET SDK 10.0** ou superior. Você pode baixá-lo no [site oficial da Microsoft](https://dotnet.microsoft.com/download).
2.  **Servidor MySQL** instalado e rodando localmente, ou acesso a uma instância remota do MySQL.
3.  **Git** (para clonar o repositório).
4.  Um IDE de sua preferência. Recomendamos o [Visual Studio 2022](https://visualstudio.microsoft.com/) ou o [Visual Studio Code](https://code.visualstudio.com/) (com as extensões para C# instaladas).

---

##  Como Executar o Projeto Localmente

Siga o passo a passo abaixo para compilar e executar o projeto em seu ambiente de desenvolvimento local:

### 1. Clone o repositório

Abra o seu terminal ou prompt de comando e execute:

```bash
git clone https://github.com/seu-usuario/biblioteca.git
cd biblioteca
```

*(Se você já possuir os arquivos do projeto localmente, basta navegar até o diretório raiz onde se encontra a pasta `Biblioteca`).*

### 2. Configuração do Banco de Dados

A aplicação utiliza o MySQL como provedor de banco de dados, integrado através do Entity Framework Core. O banco deve ser instanciado para o completo funcionamento do sistema.

1.  **Criação do Banco de Dados**: Você pode importar o modelo estrutural do banco usando o arquivo `BibliotecaDb.mwb` fornecido na raiz da pasta da aplicação (abre no MySQL Workbench), ou deixar o Entity Framework criar o banco utilizando migrations, caso aplicável.
2.  **String de Conexão**: Localize o arquivo `appsettings.json` ou `appsettings.Development.json` dentro da pasta principal (`Biblioteca/`).
3.  Abra o arquivo e altere a chave `DefaultConnection` para refletir as credenciais do seu servidor MySQL local (usuário, senha e nome do banco):

    ```json
    "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Database=biblioteca_db;Uid=seu_usuario;Pwd=sua_senha;"
    }
    ```

### 3. Restauração de Dependências

Com o terminal aberto dentro da pasta principal do projeto (`/Biblioteca` onde está o arquivo `Biblioteca.csproj`), restaure todas as dependências do NuGet necessárias executando:

```bash
dotnet restore
```

### 4. Compilação do Projeto (Build)

Para garantir que o código não apresenta erros e que os pacotes foram instalados corretamente, compile a aplicação com o comando:

```bash
dotnet build
```

*(Dica: Caso encontre erros relacionados a arquivos de cache travados por processos em segundo plano, experimente rodar `dotnet clean` ou reiniciar os processos do dotnet com `pkill dotnet` no Linux/Mac e tentar novamente).*

### 5. Executando a Aplicação

Inicie o servidor de desenvolvimento local utilizando o comando padrão da CLI do .NET:

```bash
dotnet run
```

O terminal começará a compilar e em breve exibirá logs indicando que a aplicação foi iniciada com sucesso. Você verá as informações com os endereços nos quais a aplicação está escutando (geralmente `http://localhost:5239` ou portas similares configuradas no arquivo `Properties/launchSettings.json`).

### 6. Acessando a Interface Web

*   Abra o seu navegador web de preferência.
*   Acesse a URL informada no terminal, por exemplo: [http://localhost:5239](http://localhost:5239)
*   Aproveite e navegue pelo catálogo completo de nossa Biblioteca!

---

##  Documentação Detalhada

Para informações aprofundadas sobre arquitetura, decisões técnicas, protótipos visuais e explicações sobre a fluidez de nossas páginas, consulte o nosso relatório.

O arquivo completo pode ser encontrado na pasta do repositório:
`documentação/relatorio.txt`

 Contribuindo: Levi Borges, Leticia Borges, Livia Borges.
