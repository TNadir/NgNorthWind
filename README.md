# Create project

dotnet new console -o Demo.ConsoleApp

dotnet new classlib -o Demo.Common

cd Demo.ConsoleApp

dotnet add reference ../Demo.Common/Demo.Common.csproj

dotnet add package MyPackage

cd ../

dotnet new webapi -o Demo.Api

cd Demo.Api

dotnet add reference ../Demo.Common/Demo.Common.csproj

cd ../

dotnet new sln -n Demo

dotnet sln add Demo.ConsoleApp/Demo.ConsoleApp.csproj

dotnet sln add Demo.Api/Demo.Api.csproj

dotnet build

