#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

# FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
# WORKDIR /app
# EXPOSE 80

# FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
# WORKDIR /src
# COPY ["DockerWeb/DockerWeb.csproj", "DockerWeb/"]
# RUN dotnet restore "DockerWeb/DockerWeb.csproj"
# COPY . .
# WORKDIR "/src/DockerWeb"
# RUN dotnet build "DockerWeb.csproj" -c Release -o /app/build

# FROM build AS publish
# RUN dotnet publish "DockerWeb.csproj" -c Release -o /app/publish

# FROM base AS final
# WORKDIR /app
# COPY --from=publish /app/publish .
# ENTRYPOINT ["dotnet", "DockerWeb.dll"]

#build stage
FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /generator

#restore
COPY DockerWeb.csproj ./DockerWeb/
RUN dotnet restore DockerWeb.csproj
