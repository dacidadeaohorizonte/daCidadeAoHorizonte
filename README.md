# Cidade ao Horizonte

Portal estático e responsivo do projeto interdisciplinar do Hub de Aprendizagem.

## Como visualizar

Abra `index.html` no navegador. Para testes locais mais completos, execute `python -m http.server 8000` nesta pasta e abra `http://localhost:8000`.

## Como editar os clubes e os trabalhos

Edite `js/data.js`. Cada objeto é um clube; `id` identifica a URL (`clube.html?id=linguagens`), `nome`, `espaco`, `tipo`, `cor` e `descricao` controlam a apresentação. `trabalhos` é uma lista ilimitada de objetos.

Exemplo de um novo trabalho dentro da lista `trabalhos` de um clube:

```js
{
  titulo: 'Nome do trabalho',
  descricao: 'Descrição escrita pelos estudantes.',
  imagens: [
    {src: 'assets/images/foto1.jpg', alt: 'Descrição visual da fotografia', legenda: 'Legenda da fotografia'},
    {src: 'assets/images/foto2.jpg', alt: 'Descrição da segunda foto', legenda: 'Outra legenda'}
  ],
  videos: [
    {titulo: 'Vídeo do projeto', src: 'assets/videos/video1.mp4'},
    {titulo: 'Vídeo externo', url: 'https://exemplo.org/video'}
  ],
  links: [{titulo: 'Material complementar', url: 'https://exemplo.org'}]
}
```

Para adicionar mais trabalhos, separe os objetos com vírgula. Para não exibir vídeos, use `videos: []`. Os caminhos são relativos à pasta raiz. Prefira imagens JPG/WebP comprimidas e vídeos MP4; vídeos externos aparecem como links, não como incorporação automática. Não use dados pessoais de estudantes sem autorização.

## Arquivos

- `index.html`: página inicial, mapa conceitual e cartões.
- `clube.html`: modelo compartilhado para os sete espaços editoriais (seis esquinas de visitação e Programação).
- `js/data.js`: conteúdo editável.
- `js/main.js`: geração dos cartões, mapa e páginas dos clubes.
- `css/style.css`: identidade visual e responsividade.
- `css/responsive.css`: espaço para ajustes adicionais.
- `assets/images`, `assets/videos`, `assets/icons`: mídias do projeto.

## Publicação no GitHub Pages

1. Crie um repositório público no GitHub, por exemplo `cidade-ao-horizonte`.
2. Envie **o conteúdo desta pasta** para a raiz do repositório (incluindo `index.html`).
3. Abra **Settings → Pages → Build and deployment**.
4. Escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`; salve.
5. Aguarde a publicação e abra a URL informada pelo GitHub Pages.

O site não usa backend nem build. A tipografia carrega do Google Fonts quando houver internet; fontes alternativas locais são utilizadas sem conexão.

## Verificações recomendadas antes do evento

- Conferir todos os títulos, legendas e textos.
- Testar o menu em celular, a rolagem horizontal do mapa e os links de cada esquina.
- Verificar contraste, navegação por teclado e texto alternativo das imagens.
- Testar a reprodução dos arquivos MP4 nos equipamentos da instalação.
- Verificar direitos de imagem, créditos e consentimentos.
