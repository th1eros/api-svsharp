# api-svsharp
📌 API SVsharp

API REST desenvolvida em .NET, com arquitetura em camadas, foco em boas práticas, auditoria automática e soft delete.

O sistema gerencia: 
Assets (Ativos) /Vulnerabilidades
Relacionamento entre Assets e Vulnerabilidades
Controle por ambiente (DEV / HML / PROD)
Auditoria automática (CreatedAt, UpdatedAt, DeletedAt)
Exclusão lógica (Soft Delete)

🏗 Arquitetura
O projeto segue uma estrutura baseada em separação de responsabilidades:
Controllers → Camada de entrada (HTTP)
Services → Regras de negócio
Data (DbContext) → Persistência
DTOs → Transferência de dados
Entities → Modelo de domínio

Princípios aplicados:
Injeção de Dependência
Soft Delete
Auditoria automática
Enum serializado como string
Filtros globais
Separação entre entidade e DTO

⚙ Tecnologias Utilizadas
.NET
ASP.NET Core Web API
Entity Framework Core
SQL Server
Swagger (OpenAPI)
CORS configurado para integração com front-end

🔐 Funcionalidades
Assets - Criar - Listar - Buscar por ID - Editar - Arquivar - Restaurar - Relacionar com Vulnerabilidades

Vulnerabilidades - Criar - Listar - Editar - Arquivar - Restaurar. 

Controle de:
Nível (Baixa, Média, Alta, Crítica)
Status (Ativa, Resolvida, Arquivada)
Ambiente
Auditoria Automática
CreatedAt
UpdatedAt
DeletedAt
Soft Delete
Exclusão lógica
Registro permanece no banco
Ocultação via filtro global
_____________________________________________
🚀 Como Executar o Projeto
1️⃣ Clonar o repositório
git clone <url-do-repositorio>

2️⃣ Configurar a Connection String

Editar appsettings.json:
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=SVsharp;Trusted_Connection=True;TrustServerCertificate=True;"
}

3️⃣ Aplicar Migrations
dotnet ef database update
4️⃣ Executar a API
dotnet run
📖 Documentação da API

Swagger disponível(pelo powershell) em:
http://localhost:5073/swagger/index.html

🌐 Integração com Front-End
CORS configurado para:
http://localhost:5173

📌 Status do Projeto
Backend funcional
Auditoria implementada
Soft delete implementado
Enum tratado como string
Estrutura preparada para autenticação futura
Pronto para:
Implementação de JWT
Front-end
Deploy em ambiente de produção
