FROM mcr.microsoft.com/dotnet/sdk:5.0
WORKDIR /integration

COPY integration.csproj .
RUN dotnet restore

COPY . .
ENTRYPOINT [ "dotnet", "test" ]