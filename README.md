# Aprender C# 14 con .NET 10

📖 **Lea el tutorial: [https://stahe.github.io/ales-csharp-oct-2026/](https://stahe.github.io/ales-csharp-oct-2026/)**

Este curso enseña el lenguaje [C#](https://learn.microsoft.com/fr-fr/dotnet/csharp/) 14 y la plataforma [.NET](https://dotnet.microsoft.com) 10 **mediante ejemplos prácticos**: más de doscientos programas (casi 300 archivos C#), comentados línea por línea, con sus resultados de ejecución reproducidos. Parte de los fundamentos del lenguaje y abarca el acceso a bases de datos, la programación de red y los servicios web.

Es una reescritura, para C# 14 y .NET 10, del curso [Aprendizaje del lenguaje C#, versión 3.0, con el framework .NET 3.5](https://stahe.github.io/ales-csharp-mai-2008/) (2008): mismo esquema, mismos ejemplos, mismo hilo conductor, pero con código actualizado. Todos los programas se compilan **sin errores ni advertencias** con el SDK de .NET 10 y han sido ejecutados; los resultados mostrados en el curso son los de esas ejecuciones.

| Curso C# 3.0 (2008) | Curso C# 14 (2026) |
|---|---|
| C# 3.0, framework .NET 3.5, solo Windows | C# 14, .NET 10 (LTS), Windows, Linux, macOS |
| Visual C# 2008 Express | VS Code + C# Dev Kit o Visual Studio 2026, comando `dotnet` |
| proyectos y soluciones `.sln` | aplicaciones de un solo archivo (`dotnet run prog.cs`), soluciones `.slnx` |
| interfaces gráficas Windows Forms | capítulo eliminado (hoy las interfaces son web) |
| LINQ “no tratado” | LINQ tratado en detalle |
| `ArrayList`, `Hashtable`, `BinaryFormatter` | colecciones genéricas, `System.Text.Json` |
| NUnit 2.4, Spring.NET | MSTest 4, Microsoft.Extensions.DependencyInjection |
| `BackgroundWorker`, patrón `BeginXxx` / `EndXxx` | `Task`, `async` / `await`, cancelación, `IAsyncEnumerable` |
| SQL Server 2005, ODBC, OLE DB | MySQL 8 (Laragon), MySqlConnector, Entity Framework Core |
| `WebClient`, `WebRequest` | `HttpClient` asíncrono, `TcpClient` / `TcpListener` |
| servicios web SOAP ASMX | servicios web REST / JSON con ASP.NET Core Minimal API |

## Esquema del curso

| Capítulo | Contenido |
|---|---|
| Instalación | SDK de .NET 10, VS Code / Visual Studio 2026, el comando `dotnet`, aplicaciones de un solo archivo, proyectos, soluciones `.slnx` |
| Fundamentos del lenguaje | tipos, literales, tipos que admiten valores nulos, conversiones, arreglos, índices y rangos, operadores (`??`, `??=`), expresiones `switch` y coincidencia de patrones, excepciones, enumeraciones, paso de parámetros, funciones locales, tuplas |
| Clases, estructuras, interfaces | propiedades (`init`, `required`, la palabra clave `field` de C# 14), herencia, polimorfismo, operadores, indexadores, estructuras, interfaces, genéricos, records, constructores primarios, miembros de extensión de C# 14, tipos de referencia que admiten valores nulos |
| Clases de .NET de uso frecuente | cadenas, arreglos, colecciones, **LINQ**, archivos de texto y binarios, JSON, expresiones regulares (`[GeneratedRegex]`) |
| Arquitecturas en capas | capas [DAO] / [negocio] / [UI], pruebas unitarias con **MSTest**, **inyección de dependencias** |
| Delegados, lambdas y eventos | `Func`, `Action`, expresiones lambda, closures, eventos, árboles de expresión |
| Hilos de ejecución | `Thread`, sincronización (`Lock` de C# 13, `Monitor`, `Interlocked`…), colecciones concurrentes, `Parallel` |
| **Programación asíncrona** (nuevo) | `Task`, `async` / `await`, `WhenAll`, cancelación, progreso, flujos asíncronos, `Parallel.ForEachAsync`, `Channel<T>` |
| Acceso a bases de datos con ADO.NET | MySQL, `MySqlConnector`, consultas parametrizadas e inyección SQL, transacciones, métodos asíncronos, `DbProviderFactory` |
| **Entity Framework Core** (nuevo) | modelo, CRUD, LINQ a SQL, relaciones, migraciones, concurrencia optimista, SQL sin procesar, inyección de dependencias |
| Programación web | TCP/IP, IPv6, clientes y servidores TCP asíncronos, HTTP, `HttpClient`, SMTP |
| Servicios web | REST / JSON con ASP.NET Core Minimal API, clientes de consola, cliente web JavaScript |

## El hilo conductor: un calculador del impuesto sobre la renta en 9 versiones

A lo largo del curso, versión tras versión, se construye una aplicación de **cálculo del impuesto sobre la renta**:

- **versión 1**: un único programa; **versión 2**: clases e interfaces; **versión 3**: datos leídos desde un archivo de texto o JSON;
- **versiones 4 y 5**: una arquitectura en capas, probada con MSTest e integrada mediante inyección de dependencias;
- **versiones 6 y 7**: datos en una base de datos MySQL, leídos con ADO.NET y luego con Entity Framework Core;
- **versión 8**: un servidor TCP para el cálculo del impuesto y su cliente;
- **versión 9**: un servicio web REST, su cliente de consola y su cliente web.

## Tecnologías

C# 14 · .NET 10 · VS Code · Visual Studio 2026 · MSTest 4 · Microsoft.Extensions.DependencyInjection · System.Text.Json · MySQL 8 · MySqlConnector · Entity Framework Core 9 · Pomelo.EntityFrameworkCore.MySql · ASP.NET Core 10 · Laragon

## Requisitos previos

- Experiencia previa de programación en cualquier lenguaje.
- El [SDK de .NET 10](https://dotnet.microsoft.com/download/dotnet/10.0) y un editor de código ([VS Code](https://code.visualstudio.com) con la extensión C# Dev Kit, o Visual Studio 2026); [Laragon](https://laragon.org) para MySQL (capítulos sobre bases de datos). Las instrucciones de instalación se proporcionan en el curso.

## Autor

Este curso y su código fueron escritos por **Claude**, la IA de [Anthropic](https://www.anthropic.com) (octubre de 2026), a petición de Serge Tahé, a partir de su curso de C# de 2008.

Revisor: [Serge Tahé](https://stahe.github.io)
