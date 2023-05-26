---
title: Tutorial para membros do GEAR
subtitle:
date: 2023-05-24T17:22:34-04:00
draft: false
author:
  name: Fulano
  link: fulano.com
  email: fulano@gmail.com
  avatar:
description:
keywords:
license:
comment: false
weight: 1
tags:
  - tutorial
categories:
  - Documentação
hiddenFromHomePage: false
hiddenFromSearch: false
summary:
resources:
  - name: featured-image
    src: featured-image.jpg
  - name: featured-image-preview
    src: featured-image-preview.jpg
toc: true
math: false
lightgallery: false
password:
message:
repost:
  enable: false
  url:

# See details front matter: https://fixit.lruihao.cn/documentation/content-management/introduction/#front-matter
---

A proposta do hugo.io é criar sites estásticos. O que isso significa? Que não é preciso preocupar-se com banco de dados, API, etc. pois não é um sistema _real time_. A cada modificação do repositório Git, o .html e .css serão criados automaticamente e o site será atualizado.




# Primeiros passos 

Para criar um novo post, clone o repositório com o seguinte comando:

```bash
git clone https://github.com/GEAR-UEA/gear-uea.github.io.git --recursive
```
Cuidado para não esquecer o ```recursive```. 

Os posts podem ser criados de três maneiras: 
- Na raiz de content/posts 
- Dentro de uma pasta (recomendável)
- Via linha de comando

## Na raiz 

É possível realizar esse método pelo próprio site do GitHub, uma vez que há a opção "add file". O arquivo deve ser em formato .md (Markdown) com o cabeçalho padrão que pode ser encontrado no markdown desse próprio post. Dessa maneira não é possível adicionar featured-image (a capa do post).

## Dentro de uma pasta

Essa é a maneira mais adequada porque isola os componentes daquele post. Isso é, se você quiser adicionar imagens, vídeos ou arquivos de áudio, o Markdown vai entender e os arquivos não ficarão misturados com os arquivos de outros posts. 

**Atenção: é obrigatório que, dentro de uma pasta, o nome do arquivo Markdown seja ```index.md``` e a imagem de capa deve se chamar ```featured-image```.**

## Via linha de comando 

Para esse método, é necessário ter Hugo instalado. Caso dê algum erro, pode ser que sua versão esteja desatualizada. 
Dentro do terminal, use o comando:
```bash
hugo new posts/post.md
```
O Hugo automaticamente criará o template para seu post. Por default, o arquivo vem com "draft" como "true", ou seja, não aparecerá no site a não ser que você altere para "false". 


# Teste 

Caso você queira testar se está tudo certo antes de subir para o git, pode usar a seguinte linha de comando:

```bash
hugo server
```
E depois entrar no "site" ```http://localhost:1313```, sendo que "1313" pode mudar. Atente-se à porta correta. 

Caso você queira criar o .html e .css, o comando é:
```bash
hugo
```
As pastas /public e /resources serão atualizadas automaticamente. 

# Atualização 

Criado o arquivo .md no repositório, é hora de subir para o git. Como boa prática, use o comando: ```git status``` para certificar-se que o arquivo foi criado. 

...
