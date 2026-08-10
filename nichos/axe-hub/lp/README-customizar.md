# README — Como customizar a LP do Axé Hub

## Antes de publicar — campos obrigatórios

Busque `[FICTÍCIO` no arquivo `lp.html` para encontrar todos os pontos a substituir:

| Campo | Onde substituir | O que colocar |
|---|---|---|
| Nº de sacerdotes | Hero, linha de prova social | Número real de usuários cadastrados |
| Cases de resultado | Bloco 5 (3 cards) | Depoimento real + número concreto + nome/cidade |
| Preço Expansão Espiritual | Bloco 6, plano pago | Valor real confirmado |
| E-mail de contato | Footer | E-mail real da equipe |
| Screenshot do painel | Hero (mock dashboard) | Screenshot real ou vídeo curto do painel |

---

## Trocar o CTA para WhatsApp ou formulário

O CTA padrão é um âncora `href="#planos"`. Para enviar para WhatsApp:

```html
<!-- Substituir em todos os .btn-gold que vão para #planos: -->
href="https://wa.me/55XXXXXXXXXX?text=Quero%20saber%20mais%20sobre%20o%20Ax%C3%A9%20Hub"
```

Para formulário externo (Typeform, Tally, Google Forms):
```html
href="https://seu-formulario-aqui.com" target="_blank" rel="noopener"
```

---

## Conectar pixel de analytics

Descomente o bloco no `<head>`:
```html
<!-- Pixel placeholder: substitua pelo seu pixel Meta ou Google Tag -->
<!-- <script>/* gtag ou fbq aqui */</script> -->
```

Substitua pelo código do Meta Pixel ou Google Tag Manager.

---

## Ajustar preços

No Bloco 6 (Planos), busque `R$197` e substitua pelo valor real.
Remova o `[FICTÍCIO — confirmar preço real]` após confirmar.

---

## Tokens de design — personalização rápida

Edite o bloco `:root` no `<style>` do HTML:

```css
:root {
  --bg-base:  #0A0804;  /* fundo principal */
  --accent:   #C9A84C;  /* ouro — cor única de destaque */
  --ink-h:    #F7EDCF;  /* títulos */
  --ink-body: #C4B491;  /* parágrafos */
}
```

**Não mude** `--accent` para mais de 1 cor — a efetividade visual depende de 1 acento único.

---

## Fontes (não substituir pelas proibidas)

| Função | Fonte atual | Não substituir por |
|---|---|---|
| Display (H1/H2) | Cormorant Garamond | Inter, Roboto, Arial |
| Labels/kickers | JetBrains Mono | Space Grotesk, Open Sans |
| Body | Geist | Lato, system-ui |

---

## Publicar como página standalone

O arquivo `lp.html` é single-file e funciona abrindo no browser.

**Para publicar no domínio axehub.app.br:**
1. Faça upload do `lp.html` como `index.html` na raiz do servidor
2. Configure o domínio para apontar para o servidor
3. Ative HTTPS

**Para Netlify Drop (mais rápido):**
1. Acesse netlify.app/drop
2. Arraste o `lp.html`
3. Aponte domínio axehub.app.br nas configurações DNS

---

## Próximos passos recomendados

1. Substituir os 3 cases [FICTÍCIO] por cases reais (prioridade alta — conversão depende)
2. Conectar pixel Meta antes de rodar tráfego pago
3. Definir destino do CTA (WhatsApp, formulário ou cadastro direto)
4. Confirmar preço do plano Expansão Espiritual
5. Fotografar ou gravar screenshot real do painel para substituir o mock

---

*Gerado por gos-lp-builder v0.3.0 — dvia.com*
