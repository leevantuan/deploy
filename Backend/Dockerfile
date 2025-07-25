# Runtime image
# FROM mcr.microsoft.com/dotnet/aspnet:8.0-alpine AS runtime
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime
WORKDIR /app

# Copy all build outputs (DLLs, configs...) into runtime container
COPY ./Backend/Build/ ./

# Expose port 5000 (or 5001 if you enable HTTPS)
EXPOSE 5000

# Entry point
ENTRYPOINT ["dotnet", "CoreProject.API.dll"]
