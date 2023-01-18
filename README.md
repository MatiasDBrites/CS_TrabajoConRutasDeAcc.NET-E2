# CS_TrabajoConRutasDeAcc.NET-E2
Búsqueda de todos los archivos .json

En el bucle `foreach`
 de `foundFiles`
, inserte la línea de código siguiente encima de la instrucción `if`
 para definir una nueva variable `extension`
. En este código se usa el método `Path.GetExtension`
 para obtener la extensión de cada archivo.

```csharp
var extension = Path.GetExtension(file);
```

Cambie la instrucción `if`
 para que se parezca a la siguiente línea de código. Esta instrucción comprueba si la extensión del archivo es igual a .json.

```csharp
if (extension == ".json")
```

El bucle `foreach`
 debe tener un aspecto similar al siguiente:

```csharp
foreach (var file in foundFiles)
{
    var extension = Path.GetExtension(file);
    if (extension == ".json")
    {
        salesFiles.Add(file);
    }
}
```

Guarda, Ejecute el programa desde la línea de comandos:

```bash
dotnet run
```

Ahora, en la salida se muestran todos los archivos .json que están en todos los directorios de id. de tienda:

Resultado

```
/home/username/dotnet-files/stores/sales.json
/home/username/dotnet-files/stores/201/sales.json
/home/username/dotnet-files/stores/201/salestotals.json
/home/username/dotnet-files/stores/202/sales.json
/home/username/dotnet-files/stores/202/salestotals.json
/home/username/dotnet-files/stores/203/sales.json
/home/username/dotnet-files/stores/203/salestotals.json
/home/username/dotnet-files/stores/204/sales.json
/home/username/dotnet-files/stores/204/salestotals.json
```
