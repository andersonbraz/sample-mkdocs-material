# sample-mkdocs

Abaixo eu listo todos os procedimentos que eu executei para ter um projeto mkdocs semelhante ao que tenho no meu https://andersonbraz.github.io

Ah! importante lembrar que os comandos foram realizados no sistema operacional Windows.


## Pré-requisitos

- Windows
- Powershell
- Visual Code
- Python
- Git / Github

---

## Criar diretório do projeto

```shell
mkdir sample-mkdocs
```

## Iniciar o projeto com VSCode

```shell
code sample-mkdocs
```

## Criar o ambiente Python do projeto

No terminal do VSCode digite o seguinte comando:

```shell
python -m venv .venv
```

## Ativar o ambiente Python do projeto

Ainda no terminal do VSCode digite o seguinte comando:

```shell
.\.venv\Scripts\Activate.ps1
```

## Atualizar o gerenciador de pacotes do Python

Ainda no terminal do VSCode digite o seguinte comando:

```shell
python -m pip install --upgrade pip
```

## Instalar a biblioteca principal

Ainda no terminal do VSCode digite o seguinte comando:

```shell
pip install mkdocs-material
```

## Instalar outras bibliotecas do projeto

Ainda no terminal do VSCode digite o seguinte comando:

```shell
pip install mkdocs-glightbox
```
_** Veja [aqui](https://blueswen.github.io/mkdocs-glightbox/) qual funcionalidade mkdocs-glightbox entrega._

## Criar um site mkdocs

Ainda no terminal do VSCode digite o seguinte comando:

```shell
mkdocs new .
```

## Executar o site de exemplo para mkdocs

Ainda no terminal do VSCode digite o seguinte comando:

```shell
mkdocs serve
```
Acesse a url: [http://127.0.0.1:8000](http://127.0.0.1:8000) e cada etapa que você for avançando neste procedimento vá acompanhando o que acontece com seu site.


## Mudar título e tema do site

O conteúdo do meu arquivo mkdocs.yml foi alterado para:

```yml
site_name: sample-mkdocs
theme:
  name: material
```

## Incluir texto do copyright

Foi incluído ao conteúdo do arquivo mkdocs.yml a seguinte linha:

```yml
copyright: Copyright &copy; 2024 Anderson Braz de Sousa
```

## Remover o céditos do mkdocs material

Foi incluído ao conteúdo do arquivo mkdocs.yml a seguinte linha:

```yml
extra:
  generator: false
```

## Incluir links para conexão por outras redes

Foi incluído ao conteúdo do arquivo mkdocs.yml as seguintes linhas:

```yaml
  social:
    - icon: fontawesome/brands/linkedin
      link: https://www.linkedin.com/in/anderson-braz/
    - icon: fontawesome/brands/github
      link: https://www.github.com/andersonbraz
    - icon: fontawesome/brands/stack-overflow
      link: "https://stackoverflow.com/users/7976603/anderson-braz"
    - icon: fontawesome/brands/hashnode
      link: https://andersonbraz.com
    - icon: fontawesome/brands/telegram
      link: https://telegram.me/braz_anderson
    - icon: material/email
      link: "mailto:contato@andersonbraz.com"
```

## Alterar paleta de cores e habilitaar função dark mode

Foi incluído ao conteúdo do arquivo mkdocs.yml as seguintes linhas:

```yml
  palette:
    # Palette toggle for automatic mode
    - media: "(prefers-color-scheme)"
      toggle:
        icon: material/brightness-auto
        name: Switch to light mode

    # Palette toggle for light mode
    - media: "(prefers-color-scheme: light)"
      scheme: default 
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode

    # Palette toggle for dark mode
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      toggle:
        icon: material/brightness-4
        name: Switch to system preference
```

## Publicar o site

Ainda no terminal do VSCode digite o seguinte comando:

```shell
mkdocs build
```

_Após a execução deste comando observe que foi criado um diretório chamado "site" que contém todos os arquivos do seu site estático._

## Fontes

- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [MkDocs GLightbox](https://blueswen.github.io/mkdocs-glightbox/)
