
FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /generator

COPY ["api/API/API.csproj", "api/API/"]
RUN dotnet restore "api/API/API.csproj"
COPY ["tests/Tests/Tests.csproj", "tests/Tests/"]
RUN dotnet restore "tests/Tests/Tests.csproj"

#COPY ..

RUN dotnet test tests/tests.csproj