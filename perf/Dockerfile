FROM microsoft/aspnetcore-build:2.0.0 AS build-env
WORKDIR /app
RUN dotnet new mvc
RUN dotnet restore
RUN dotnet publish -o /published

FROM microsoft/aspnetcore:2.0.0
COPY --from=build-env /published /published
WORKDIR /published
ENTRYPOINT ["dotnet", "published/app.dll"]
