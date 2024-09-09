# CURSO: APRENDE BLAZOR

# LECCIÓN 27: Captura de resto de parámetros con el símbolo * (Catch All Parameters)

1. Abrir la aplicación con Visual Studio 2022 o VSCode

2. Añadimos el siguiente código al componente Home.razor

```razor
@page "/"

@page "/home/{*everything}"

@page "/home/{id:int}/{*everything}"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<p>Remaining URL: @Everything</p>

<p>Parameter Id: @Id</p>

@code {
    [Parameter]
    public string? Everything { get; set; }

    [Parameter]
    public int Id { get; set; }
}
```
