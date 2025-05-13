## Contribuyendo

Estamos entusiasmados de que desee contribuir a este proyecto. Su ayuda es esencial para mantenerlo excelente.

Las contribuciones a este proyecto son [liberadas](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#6-contributions-under-repository-license) al público bajo la [licencia de código abierto del proyecto](LICENSE).

Tenga en cuenta que este proyecto se publica con un [Código de Conducta del Contribuyente](CODE_OF_CONDUCT.md). Al participar en este proyecto, usted acepta cumplir con sus términos.

Aquí hay algunas notas útiles sobre cómo contribuir a este proyecto, incluidos detalles sobre cómo comenzar a trabajar con el código.

## Configure su entorno de desarrollo

Para comenzar, necesitará tener [.NET Core 6.0](https://dotnet.microsoft.com/en-us/download) instalado en su máquina local.

La solución puede compilarse usando el siguiente comando:

```bash
$ dotnet build src/ActionsImporter.sln
```

Las pruebas unitarias pueden ejecutarse usando el siguiente comando:

```bash
$ dotnet test src/ActionsImporter.sln
```

El formato del código puede ejecutarse usando el siguiente comando:

```bash
$ dotnet format src/ActionsImporter.sln
``` 