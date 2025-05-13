# Importador do GitHub Actions

[![.github/workflows/ci.yml](https://github.com/github/gh-actions-importer/actions/workflows/ci.yml/badge.svg)](https://github.com/github/gh-actions-importer/actions/workflows/ci.yml)

*Leia este documento em outros idiomas: [Español](README.es.md)*

[Importador do GitHub Actions](https://docs.github.com/en/actions/migrating-to-github-actions/automating-migration-with-github-actions-importer) ajuda a planejar, testar e automatizar sua migração para o GitHub Actions a partir das seguintes plataformas:

- Azure DevOps
- Bamboo
- Bitbucket
- CircleCI
- GitLab
- Jenkins
- Travis CI

## Como solicitar suporte

Se precisar de assistência, você pode abrir um ticket de suporte [aqui](https://support.github.com).

## Começando

O Importador do GitHub Actions é distribuído como um contêiner Docker e esta extensão para o [GitHub CLI](https://cli.github.com) oficial para interagir com o contêiner Docker.

### Pré-requisitos

Os seguintes requisitos devem ser atendidos para poder usar o Importador do GitHub Actions:

- O CLI do Docker deve estar [instalado](https://docs.docker.com/get-docker/) e em execução.
- O [GitHub CLI](https://cli.github.com) oficial deve estar instalado.
- Você deve ter credenciais para [autenticar](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry) com o GitHub Container Registry.

### Instalação

Em seguida, a extensão CLI do Importador do GitHub Actions pode ser instalada via este comando:

```bash
gh extension install github/gh-actions-importer
```

### Configuração

Novas versões do Importador do GitHub Actions são lançadas regularmente. Para garantir que você esteja atualizado, execute o seguinte comando:

```bash
gh actions-importer update
```

Para que o Importador do GitHub Actions se comunique com seu servidor CI/CD atual e com o GitHub, várias credenciais devem estar disponíveis para o comando. Estas podem ser configuradas usando variáveis de ambiente ou um arquivo `.env.local`. Essas variáveis de ambiente podem ser configuradas em um prompt interativo executando o seguinte comando:

```bash
$ gh actions-importer configure
? Enter value for 'GITHUB_ACCESS_TOKEN' (leave empty to skip):
...
```

Você pode encontrar informações detalhadas sobre o uso de variáveis de ambiente na documentação específica da plataforma.

#### Usando um registro Docker personalizado

Recomendamos fortemente o uso do [GitHub Container Registry oficial para puxar a imagem Docker do Importador do GitHub Actions](https://github.com/actions-importer/preview/pkgs/container/cli/). No entanto, se você precisar usar um registro Docker personalizado, poderá configurar o Importador do GitHub Actions para usar um registro Docker personalizado definindo a variável de ambiente `CONTAINER_REGISTRY` no seu arquivo `.env.local`.

```bash
# .env.local
CONTAINER_REGISTRY=meu-registro-personalizado.com
```

### Documentação

Informações detalhadas sobre como usar o Importador do GitHub Actions podem ser encontradas na [documentação](https://docs.github.com/en/actions/migrating-to-github-actions/automating-migration-with-github-actions-importer).

### Gravações

Você pode acessar demos gravadas do Importador do GitHub Actions realizando migrações para Actions a partir das seguintes plataformas CI/CD:

- [Azure DevOps](https://youtu.be/gG-2bkmBRlI)
- [CircleCI](https://youtu.be/YkFnNEyM9Hg)
- [GitLab](https://youtu.be/3t5ywu0_qk4)
- [Jenkins](https://youtu.be/WqiGP6h4fa0)
- [Travis CI](https://youtu.be/ndc-FNa_X3c)

### Aprendizado autodidata

O repositório de laboratórios do Importador do GitHub Actions contém caminhos de aprendizado específicos da plataforma que ensinam como usar o Importador do GitHub Actions e como abordar migrações para o GitHub Actions. Para saber mais, veja o [repositório de laboratórios do Importador do GitHub Actions](https://github.com/actions/importer-labs/tree/main#readme).

## Roteiro do produto

Para saber sobre novos recursos que estão chegando ao Importador do GitHub Actions, veja o [Roteiro Público do GitHub](https://github.com/orgs/github/projects/4247).

## Como oferecer feedback ou fazer uma solicitação de recurso

Se você gostaria de oferecer feedback ou fazer uma solicitação de recurso, por favor crie uma nova discussão [aqui](https://github.com/github/gh-actions-importer/discussions/new/choose).
