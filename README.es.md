# Importador de GitHub Actions

[![.github/workflows/ci.yml](https://github.com/github/gh-actions-importer/actions/workflows/ci.yml/badge.svg)](https://github.com/github/gh-actions-importer/actions/workflows/ci.yml)

[Importador de GitHub Actions](https://docs.github.com/en/actions/migrating-to-github-actions/automating-migration-with-github-actions-importer) ayuda a planificar, probar y automatizar su migración a GitHub Actions desde las siguientes plataformas:

- Azure DevOps
- Bamboo
- Bitbucket
- CircleCI
- GitLab
- Jenkins
- Travis CI

## Cómo solicitar soporte

Si necesita asistencia, puede abrir un ticket de soporte [aquí](https://support.github.com).

## Primeros pasos

El Importador de GitHub Actions se distribuye como un contenedor Docker y esta extensión para el [GitHub CLI](https://cli.github.com) oficial para interactuar con el contenedor Docker.

### Prerrequisitos

Se deben cumplir los siguientes requisitos para poder utilizar el Importador de GitHub Actions:

- El CLI de Docker debe estar [instalado](https://docs.docker.com/get-docker/) y en ejecución.
- El [GitHub CLI](https://cli.github.com) oficial debe estar instalado.
- Debe tener credenciales para [autenticarse](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry) con el GitHub Container Registry.

### Instalación

A continuación, la extensión CLI del Importador de GitHub Actions puede ser instalada a través de este comando:

```bash
gh extension install github/gh-actions-importer
```

### Configuración

Nuevas versiones del Importador de GitHub Actions se lanzan regularmente. Para asegurarse de que está actualizado, ejecute el siguiente comando:

```bash
gh actions-importer update
```

Para que el Importador de GitHub Actions se comunique con su servidor CI/CD actual y con GitHub, varias credenciales deben estar disponibles para el comando. Estas pueden configurarse usando variables de entorno o un archivo `.env.local`. Estas variables de entorno pueden configurarse en un prompt interactivo ejecutando el siguiente comando:

```bash
$ gh actions-importer configure
? Enter value for 'GITHUB_ACCESS_TOKEN' (leave empty to skip):
...
```

Puede encontrar información detallada sobre el uso de variables de entorno en la documentación específica de la plataforma.

#### Usando un registro Docker personalizado

Recomendamos encarecidamente el uso del [GitHub Container Registry oficial para extraer la imagen Docker del Importador de GitHub Actions](https://github.com/actions-importer/preview/pkgs/container/cli/). Sin embargo, si necesita usar un registro Docker personalizado, puede configurar el Importador de GitHub Actions para usar un registro Docker personalizado estableciendo la variable de entorno `CONTAINER_REGISTRY` en su archivo `.env.local`.

```bash
# .env.local
CONTAINER_REGISTRY=mi-registro-personalizado.com
```

### Documentación

Puede encontrar información detallada sobre cómo usar el Importador de GitHub Actions en la [documentación](https://docs.github.com/en/actions/migrating-to-github-actions/automating-migration-with-github-actions-importer).

### Grabaciones

Puede acceder a demos grabadas del Importador de GitHub Actions realizando migraciones a Actions desde las siguientes plataformas CI/CD:

- [Azure DevOps](https://youtu.be/gG-2bkmBRlI)
- [CircleCI](https://youtu.be/YkFnNEyM9Hg)
- [GitLab](https://youtu.be/3t5ywu0_qk4)
- [Jenkins](https://youtu.be/WqiGP6h4fa0)
- [Travis CI](https://youtu.be/ndc-FNa_X3c)

### Aprendizaje autodirigido

El repositorio de laboratorios del Importador de GitHub Actions contiene rutas de aprendizaje específicas para cada plataforma que enseñan cómo usar el Importador de GitHub Actions y cómo abordar migraciones a GitHub Actions. Para saber más, consulte el [repositorio de laboratorios del Importador de GitHub Actions](https://github.com/actions/importer-labs/tree/main#readme).

## Hoja de ruta del producto

Para conocer las nuevas funcionalidades que llegarán al Importador de GitHub Actions, consulte la [Hoja de Ruta Pública de GitHub](https://github.com/orgs/github/projects/4247).

## Cómo ofrecer feedback o hacer una solicitud de función

Si desea ofrecer feedback o hacer una solicitud de función, por favor cree una nueva discusión [aquí](https://github.com/github/gh-actions-importer/discussions/new/choose). 