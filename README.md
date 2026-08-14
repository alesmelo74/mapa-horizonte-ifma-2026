# Mapa do Evento — Horizonte IFMA 2026

Página web do Mapa do Evento do **Horizonte IFMA 2026**, realizado de 19 a 21 de agosto de 2026 no Campus Barreirinhas do IFMA (Barreirinhas - MA).

A imagem do mapa funciona como menu principal: cada um dos quatro itens é uma área clicável que abre o material correspondente.

## Estrutura

| Arquivo | Função |
| --- | --- |
| `index.html` | Menu principal |
| `1-programacao.html` | 1 · Rota do Conhecimento — Programação, grade por eixo temático |
| `2-restaurantes.html` | 2 · Parada dos Sabores — Restaurantes em Barreirinhas |
| `3-o-que-fazer.html` | 3 · Trilha Barreirinhas Viva — Dicas do que fazer |
| `4-bem-viver.html` | 4 · Estação Bem-Viver — Atividades fora das palestras |
| `base.css` | Paleta, cabeçalho e rodapé compartilhados |
| `mapa.css` | Estilo específico do menu principal |
| `paginas.css` | Estilo específico das páginas 1 a 4 |
| `gerar-qrcode.html` | Utilitário para gerar o QR code de acesso ao mapa |

Cada página tem uma barra fixa com o botão **Voltar ao menu principal**.

## Conteúdo em HTML, não em imagem

Nenhuma página usa os PNGs originais como layout. Todo o conteúdo foi transcrito para HTML e CSS, com texto real que reflui conforme a largura da tela, sem proporção travada e sem distorção. As cores foram amostradas dos materiais originais e os ícones são SVG embutidos.

As fotos da página 3 foram recortadas do PNG correspondente e são exibidas com `aspect-ratio` e `object-fit: cover`, o que normaliza o enquadramento sem esticar a imagem.

Os arquivos originais seguem no repositório e podem ser baixados a partir das próprias páginas.

## Como rodar localmente

O projeto é estático, sem dependências ou etapa de build. Para testar em um servidor local, o que reproduz melhor o comportamento da hospedagem:

```bash
python -m http.server 8000
```

Depois abra <http://localhost:8000>.

Abrir o `index.html` direto pelo sistema de arquivos também funciona.

## Fonte do conteúdo

| Página | Material de origem |
| --- | --- |
| `index.html` | `0.Mapa do Evento.png` |
| `1-programacao.html` | `1.Programacao_Horizonte_IFMA_2026.pptx` |
| `2-restaurantes.html` | `2.Restaurantes.png` |
| `3-o-que-fazer.html` | `3.O que fazer.png` |
| `4-bem-viver.html` | atividades anunciadas no Mapa do Evento |

Ao receber uma versão nova de qualquer material, atualize a página correspondente e confira se o link de download no fim da página ainda aponta para o arquivo certo.

## QR code

Abra o `gerar-qrcode.html`, cole o endereço publicado e baixe o código em PNG (1200px) ou SVG (vetorial, para gráfica). O código é gerado no próprio navegador.
