# ByteForge

[![Deploy Hugo site to Pages](https://github.com/imfing/hextra-starter-template/actions/workflows/pages.yaml/badge.svg)](https://github.com/imfing/hextra-starter-template/actions/workflows/pages.yaml)


🐣 Minimal template for getting started with [Hextra](https://github.com/imfing/hextra)

[🌐 Demo ↗](https://andrew1988123123.github.io/ByteForge/)

## Quick Start

Use this template to create your own repository:

<img src="https://docs.github.com/assets/cb-77734/mw-1440/images/help/repository/use-this-template-button.webp" width=400 />

You can also quickly start developing using the following online development environment:

- [GitHub Codespaces](https://github.com/codespaces) 
    
    [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/imfing/hextra-starter-template)

    Create a new codespace and follow the [Local Development](#local-development) to launch the preview

- [Gitpod](https://gitpod.io)

    [![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/imfing/hextra-starter-template)


## Deployment

### GitHub Pages

A GitHub Actions workflow is provided in [`.github/workflows/pages.yaml`](./.github/workflows/pages.yaml) to [publish to GitHub Pages](https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/) for free. 

For details, see [Publishing with a custom GitHub Actions workflow](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow).

Note: in the settings, make sure to set the Pages deployment source to **GitHub Actions**:

<img src="https://github.com/imfing/hextra-starter-template/assets/5097752/99676430-884e-42ab-b901-f6534a0d6eee" width=600 />

[Run the workflow manually](https://docs.github.com/en/actions/using-workflows/manually-running-a-workflow) if it's not triggered automatically.


## Local Development

Pre-requisites: [Hugo](https://gohugo.io/getting-started/installing/), [Go](https://golang.org/doc/install) and [Git](https://git-scm.com)

```shell
# Clone the repo
git clone https://github.com/Andrew1988123123/ByteForge

# Change directory
cd ByteForge

# Start the server
hugo mod tidy
hugo server --logLevel debug --disableFastRender -p 1313
```

### Update theme

```shell
hugo mod get -u
hugo mod tidy
```

See [Update modules](https://gohugo.io/hugo-modules/use-modules/#update-modules) for more details.

