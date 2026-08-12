# Como Customizar — LP R Freitas Seguros

## Arquivo principal
`lp.html` — single-file, zero dependências além de Google Fonts (carregado online).

---

## Trocar textos

Abra o arquivo em qualquer editor de texto (VSCode, Notepad++, etc.) e faça busca (`Ctrl+F`) pelos textos que quer trocar.

### Campos mais comuns para trocar
| O que trocar | Buscar por | Substituir por |
|---|---|---|
| Número de WhatsApp | `5585987715347` | Seu número no formato DDI+DDD+número sem espaços |
| Telefone fixo | `(85) 3063-9474` | Seu telefone atual |
| Email | `rfseguros87@gmail.com` | Seu email atual |
| Endereço | `Av. Mozart Pinheiro de Lucena, 696` | Endereço atualizado |
| Instagram | `@rfreitasseguros` | Handle atualizado |

---

## Trocar cores

No bloco `<style>`, localizar `:root {` e alterar os tokens:

```css
--accent: #2E7D32;     /* cor principal dos botões e destaques — trocar aqui */
--bg-dark: #1A3A5C;    /* azul escuro do header/hero/footer */
--accent-h: #1B5E20;   /* cor do botão ao passar o mouse (hover) */
```

---

## Adicionar depoimentos reais

Localizar o comentário `<!-- BLOCO 5 — NÚMEROS -->` e substituir os cards de estatísticas por depoimentos reais no formato:

```html
<div class="prova-card">
  <p>"Depoimento real do cliente aqui."</p>
  <span class="prova-meta">Nome do Cliente · Produto contratado</span>
</div>
```

---

## Conectar pixel Meta / Google Analytics

No `<head>`, há um comentário:
```html
<!-- Pixel/Analytics: inserir aqui -->
```
Cole o código do pixel Meta ou tag Google Analytics exatamente aí.

---

## Adicionar logo

No header, substituir o texto `.nav-logo` por uma tag `<img>`:

```html
<a href="#topo" class="nav-logo">
  <img src="URL_DO_LOGO.png" alt="R Freitas Seguros" height="36">
</a>
```

---

## Hospedar a LP

Opções gratuitas ou baratas:
1. **GitHub Pages** — grátis, arrasta o arquivo
2. **Netlify Drop** — netlify.com/drop, arrasta o arquivo
3. **Google Drive** — compartilha com "anyone with the link"
4. **Domínio próprio** — qualquer hospedagem que aceite HTML estático

---

*Powered by Accelera 360*
