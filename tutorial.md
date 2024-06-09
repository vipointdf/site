# Como adicionar novas páginas

Para adicionar novas páginas, siga os passos abaixo:

1. Dentro da pasta `src/pages/`, crie um novo arquivo com o nome da página em minúsculo e separado por hífen, caso tenha algum espaço, com a extensão `.astro` no final, como no exemplo a seguir: `src/pages/pagina.astro`.
2. Vá no arquivo `nova-pagina.astro` e copie todo o conteúdo para o arquivo da nova página.
3. Agora, abra o arquivo `src/components/Nav.astro` e logo no começo do arquivo, onde existe `const Paginas`, copie um dos códigos entre chaves {} já existentes e coloque-o na ordem que desejar. Lembre-se que o item `diretorio` deve ter o mesmo nome do arquivo criado na pasta `src/pages/`. Não se esqueça das vírgulas entre os itens, como no exemplo: `{nome: "Nova Página", diretorio: "/nova-pagina/"},`.
4. Pronto! Agora é só rodar o projeto e acessar a nova página criada.

# Como adicionar novos Cards

Para adicionar novos cards, siga os passos abaixo:

1. Adicione a imagem desejada dentro da pasta `public`. 
2. No arquivo `src/pages/{pagina-que-deseja-adicionar-cards}.astro`, escreva o seguinte código:
```astro
<Card
  imagem="/caminho-para-imagem.jpg"
  titulo="Título do Card"
  descricao="Descrição do Card">
<Card/>
```
 
Lembre-se que o caminho da imagem deve ser o caminho relativo a pasta `public`, ou seja, o caminho deve ser `/nome-da-imagem.jpg`, ou `/pasta/nome-da-imagem.jpg`, caso esteja em uma pasta.

# Como abrir o terminal no Visual Studio Code

Para abrir o terminal, vá em "View -> Terminal", no canto superior direito. Caso queira um shortcut pelo teclado, aperte Ctrl + '.


# Atualizando o site

Antes de atualizar as informações, verifique se todos os arquivos estão salvos.
Para enviar as alterações feitas, copie o seguinte comando para o terminal:
```
git add .
git commit -m "site atualizado"
git push
```

# Atualizando o diretório local

Para atualizar o diretório local, copie o seguinte comando para o terminal:
```
git stash
git pull --rebase
git stash pop
```
