# Cadastro de Associados — WinForms (VB.NET)

Aplicação desktop em **VB.NET + Windows Forms** sobre **.NET 6**, com cadastro de associados e empresas persistidos em SQL Server via `System.Data.SqlClient` puro (sem ORM).

> **Nota sobre o nome:** o repositório chama-se `CadastroAssociadoWebForms` por razões históricas, mas o projeto é **Windows Forms** (`<UseWindowsForms>true</UseWindowsForms>` / `OutputType=WinExe`), não ASP.NET WebForms.

![VB.NET](https://img.shields.io/badge/VB.NET-.NET%206-512BD4?logo=dotnet&logoColor=white)
![WinForms](https://img.shields.io/badge/UI-Windows%20Forms-0078D4)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?logo=microsoftsqlserver&logoColor=white)

## Stack

- **VB.NET** sobre **.NET 6 (net6.0-windows)**
- **Windows Forms** (`WindowsForms` / MyType `WindowsForms`)
- **System.Data.SqlClient 4.8.5** — acesso ADO.NET direto (sem ORM)

## Telas

| Form | Responsabilidade |
|---|---|
| `PrincipalForm` | Menu principal / navegação |
| `AssociadoForm` | CRUD de associados |
| `EmpresaForm` | CRUD de empresas |

Entidades em `Entidades/Associado.vb` e `Entidades/Empresa.vb`.

## Como rodar

Requer **Windows** (é uma app Windows Forms) e **.NET 6 SDK**.

```bash
dotnet restore
dotnet build
dotnet run --project "Projeto Cadastro Associado WebFormsVB"
```

Configure a connection string antes de executar (o projeto usa SqlClient direto — ajuste o host/database/credenciais no código de conexão).

## Projetos relacionados (mesmo domínio, stacks diferentes)

- **[Cadastro-Associados-API](https://github.com/gustavograciano/Cadastro-Associados-API)** — API REST em .NET 7 + EF Core
- **[Projeto-Cadastro-Associado-VB.NET](https://github.com/gustavograciano/Projeto-Cadastro-Associado-VB.NET)** — versão console VB.NET legacy (.NET 4.7.2 + EF 6)

## Status

Projeto de estudo que explora o mesmo domínio (associados/empresas) em diferentes stacks: desktop WinForms, console legacy e REST API. Útil para comparar trade-offs entre UI desktop, ADO.NET puro e abordagens modernas com EF Core.
