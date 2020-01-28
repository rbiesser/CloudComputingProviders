Cloud Computing Providers
---
Just a little project playing around with the Azure CLI and Mapbox that plots Microsoft's Azure Data Centers on a map.

Created by following the tutorial located at:

https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start?view=aspnetcore-3.1&tabs=visual-studio-code

# Prerequisites
- [Visual Studio Code](https://code.visualstudio.com/Download)
- [C# Extension for Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)
- [.NET CORE 3.1 SDK or later](https://dotnet.microsoft.com/download)
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)

# Create a Razor Pages web app
- Create a new folder to contain the project
```
dotnet new webapp
```

# Run the app
- Trust the HTTPS development certificate
```
dotnet dev-certs https --trust
```
- Run from the Terminal
```
dotnet run
```
- Or use the Debug menu, which uses .vscode/launch.json configuration

# Create new pages
- See [dotnet new Reference](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-new)
```
dotnet new page --output Pages --name Map --dry-run
```

# Azure CLI
- Install [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) for your OS
- [Install Azure CLI Tools Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)
- Create Azure/example.azcli for usage or terminal
- See [Azure CLI Reference](https://docs.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest)
- If Microsoft adds new regions or you belong to a different subscription level (ie. DOD), you can generate a new listing with this command. 
```
az account list-locations
```

# Mapbox GL JS
- [Mapbox GL JS API Reference](https://docs.mapbox.com/mapbox-gl-js/api/)
- [How Mapbox works, web applications](https://docs.mapbox.com/help/how-mapbox-works/web-apps/)
- Their documentation doesn't describe the functions very well, so use the Help page for descriptions and then the API Reference for details.

# JSON Serialization
- [JSON Serialization .NET Guide](https://docs.microsoft.com/en-us/dotnet/standard/serialization/system-text-json-overview)
- .NET has adopted the [Newtonsoft Json.NET](https://www.newtonsoft.com/json) project into the Core Framework

# Razor Pages
- Why is the concept of ViewData and ViewBags not documented better? [Learn Razor Pages Article](https://www.learnrazorpages.com/razor-pages/viewdata) is the first I found to discuss it.
- And then I found it buried here in the [ASP.NET Core Documentation](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-2.1&tabs=visual-studio#viewdata-attribute-1)
- Use the `[ViewData]` annotation on class properties to pass data from the controller to the view or use the `ViewData` dictionary.
- [WebApps Razor Syntax](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-3.1) shows how to use C# in the view.

# Other Resources
- [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/)
- [NuGet Package Manager](https://www.nuget.org/)
- [GeoJson Specification RFC 7946](https://geojson.org/)