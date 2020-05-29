# Calling an api

- use the HttpClient class to make ASYNC web requests
- `private static readonly HttpClient client = new HttpClient();`
- uses JSON serializer immediately followed by deseralizer to take in and format data
- `var streamTask = client.GetStreamAsync("https://api.github.com/orgs/dotnet/repos");`
  `var repositories = await JsonSerializer.DeserializeAsync<List<Repository>>(await streamTask);`
- serializers looks for property names, use `[JsonPropertyName("name")]`
                                             `public string Name { get; set; }`

**Swagger**
  -  Swagger, also known as OpenAPI, solves the problem of generating useful documentation and help pages for Web APIs.
  - Swagger is a language-agnostic specification for describing REST APIs
  - Swagger UI offers a web-based UI that provides information about the service, using the generated Swagger specification