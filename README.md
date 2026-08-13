# Mapa do Evento — Horizonte IFMA 2026

Página web do Mapa do Evento do **Horizonte IFMA 2026**, realizado de 19 a 21 de agosto de 2026 no Campus Barreirinhas do IFMA (Barreirinhas - MA).

A imagem do mapa funciona como menu principal: cada um dos quatro itens é uma área clicável que abre o material correspondente.

## Estrutura

| Arquivo | Função |
| --- | --- |
| `index.html` | Menu principal, com as áreas clicáveis sobre a imagem do mapa |
| `1-programacao.html` | 1 · Rota do Conhecimento — Programação Oficial (PDF) |
| `2-restaurantes.html` | 2 · Parada dos Sabores — Restaurantes em Barreirinhas |
| `3-o-que-fazer.html` | 3 · Trilha Barreirinhas Viva — Dicas do que fazer |
| `4-bem-viver.html` | 4 · Estação Bem-Viver — Atividades fora das palestras |
| `visualizador.css` | Estilo compartilhado das páginas de visualização |
| `gerar-qrcode.html` | Utilitário para gerar o QR code de acesso ao mapa |

Cada página de material tem um botão fixo **Voltar ao menu principal**.

## Como rodar localmente

O projeto é estático, sem dependências ou etapa de build. Para testar em um servidor local, o que reproduz melhor o comportamento da hospedagem:

```bash
python -m http.server 8000
```

Depois abra <http://localhost:8000>.

Abrir o `index.html` direto pelo sistema de arquivos também funciona, mas alguns navegadores baixam o PDF em vez de exibi-lo embutido na página 1.

## Ajuste das áreas clicáveis

As áreas do menu são posicionadas em porcentagem, então acompanham qualquer tamanho de tela. Para reposicioná-las, abra o `index.html` e pressione <kbd>E</kbd>: arraste cada retângulo para mover, use o quadradinho do canto para redimensionar e clique em **Copiar coordenadas** para colar os valores de volta nos atributos `style` do HTML.

## QR code

Abra o `gerar-qrcode.html`, cole o endereço publicado e baixe o código em PNG (1200px) ou SVG (vetorial, para gráfica). O código é gerado no próprio navegador.
