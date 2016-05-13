---
layout: post
excerpt: o Jekyll é um gerador de sites estáticos que trabalha com Makdown, HTML e CSS em ruby.
title: Primeiros passos com Jekyll
---

![logo jekyll]({{ site.baseurl }}/images/jekyll-logo.png)

o Jekyll é um gerador de sites estáticos que trabalha com Makdown, HTML e CSS em ruby.

### Requisitos

+ [Ruby](https://www.ruby-lang.org/en/downloads/) (including development headers, v1.9.3 or above for Jekyll 2 and v2 or above for Jekyll 3)
+ [RubyGems](https://rubygems.org/pages/download)
+ Linux, Unix, or Mac OS X

```
~ $ gem install jekyll
# este comando cria a pasta myblog iniciar o projeto na pasta
# corrente utilizar "jekyll new ."
# caso o diretório não for vazio utilizar "jekyll new . --force"
~ $ jekyll new myblog
~ $ cd myblog
~/myblog $ jekyll serve
# => Entre em: http://localhost:4000
```

### Comandos Básicos

```
$ jekyll build
# =>  O projeto será compilado dentro de ./_site

$ jekyll build --destination <destination>
# => O projeto será compilado dentro de <destination>

$ jekyll build --source <source> --destination <destination>
# => O código da pasta <source> vai ser compilado na pasta <destination>

$ jekyll build --watch
# => O projeto será compilado dentro de ./_site,
#    observando por mudanças e regerando automáticamente.
```

### Estrutura de diretórios

```
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile
├── _data
|   └── members.yml
├── _site
├── .jekyll-metadata
└── index.html
```

### Principais arquivos e pastas

| Arquivos/pasta | Descrição |
| -------------- | --------- |
| _config.yml | Arquivo que contém dados de configuração |
| _drafts | Nesta pasta devem ficar os posts não publicados, o formato dos nomes dos arquivos não comtem data|
| _includes | Nesta pasta devem ser colocadas as views parciais para facitilar o reuso |
| _layouts | Nesta página ficam os templates das páginas |
| _posts | Seu conteúdo dinâmico, por assim dizer. A convenção de nomenclatura desses arquivos é importante, e deve seguir o formato: **ANO-MÊS-DIA-titulo.MARKUP** |
| _data | Os arquivos de dados que serão usados no site devem ficar aqui, o Jekyll carrega automaticamente os arquivos deste diretórios e aceita os formatos **.yml**, **.yaml**, **.json**, **.csv**, os dados ficam acessiveis via 'site.data'. Se você tiver um arquivo **membros.yml** neste diretorio, você pode acessar seus conteúdos utilizando 'site.data.membros'. |
| _site | Este é o lugar onde o site gerado será colocado (por default). É provavelmente uma boa idéia para adicioná-lo ao seu arquivo **.gitignore**. |
| index.html e outros arquivos HTML, Markdown, Textile | Desde que seja inciado com uma seção YAML o Jekyll vai compliar qualquer **.html**, **.markdown**, **Md, ou arquivo **.textile** no diretório raiz do seu site ou diretórios não listados acima.|
| Outros arquivos e pastas | Todos os demais arquivos e pastas exceto os relacionados anateriormente, como pastas de **css** e **imagens**, arquivo **favicon.ico** |

### Conclusão

O Jekyll é uma ferramenta muito simples e pode ser utilizado para fazer coisas bem interessantes.

Um forte incentivo para utilizar o Jekyll é o próprio Github, que dá suporte a ele sendo possivel utilizar-lo em sua página, ou nas páginas dos seus projetos, Num próximo post irei relatar a experieência de criar este blog utilizando esta ferramenta.

Grande parte desse post teve como base o site oficial que está referenciado abaixo.

### Referências

[Site oficial jekyll](https://jekyllrb.com/)
[Jekyll Now](http://github.com/barryclark/jekyll-now)
