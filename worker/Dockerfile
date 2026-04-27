# Build Stage
FROM --platform=linux/amd64 mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /source

# Copy project file and restore dependencies
COPY *.csproj .
RUN dotnet restore

# Copy remaining files and publish
COPY . .
RUN dotnet publish -c Release -o /app

# Runtime Stage
FROM --platform=linux/amd64 mcr.microsoft.com/dotnet/runtime:7.0
WORKDIR /app

# Copy build output
COPY --from=build /app .

# Run application
ENTRYPOINT ["dotnet", "Worker.dll"]