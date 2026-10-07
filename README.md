# DotNet8AzureDemo

A simple ASP.NET Core Web API targeting .NET 8, ready for GitHub and Azure App Service deployment.

## Requirements

- .NET 8 SDK
- Visual Studio 2022 (17.8+) or VS Code
- Git

## Run locally

```bash
dotnet restore
dotnet build
dotnet run
```

Open Swagger:

- https://localhost:7080/swagger
- or http://localhost:5080/swagger

## API endpoints

- GET `/api/products`
- GET `/api/products/{id}`
- POST `/api/products`
- PUT `/api/products/{id}`
- DELETE `/api/products/{id}`

The sample uses an in-memory product list, so data resets when the application restarts.

## GitHub

```bash
git init
git add .
git commit -m "Initial .NET 8 API"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/DotNet8AzureDemo.git
git push -u origin main
```

## Azure App Service

Create an Azure App Service using:

- Publish: Code
- Runtime stack: .NET 8
- Operating System: Linux or Windows

Then connect the App Service to the GitHub repository using Deployment Center, or configure GitHub Actions.

For a production application, move secrets and connection strings to Azure App Service Configuration / Key Vault rather than committing them to source control.
