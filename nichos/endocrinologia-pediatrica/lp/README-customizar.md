# Como customizar a LP — PediEndoCare™

## Substituições obrigatórias antes de publicar

### 1. Depoimentos reais
Buscar nos arquivos HTML os comentários `[FICTÍCIO — substituir por depoimento real]`.
Substituir os 3 blockquotes com depoimentos reais de famílias (com autorização por escrito — LGPD).

### 2. Formulário de triagem
O form atual é visual (sem backend). Substituir o `<button>` por:
- **Typeform embed:** `<div class="tf-widget" data-url="https://form.typeform.com/to/XXXXX">`
- **Calendly:** substituir form por `<div class="calendly-inline-widget" data-url="https://calendly.com/XXXXX">`
- **WhatsApp Business:** `<a href="https://wa.me/55XXXXXXXXXXX?text=Olá, quero fazer a triagem gratuita do PediEndoCare™">`

### 3. Foto do médico
Adicionar na seção de prova social (ou criar nova seção com foto + credenciais):
```html
<img src="foto-medico.jpg" alt="Dr. [Nome] — Endocrinologista Pediátrico" class="rounded-sm">
```

### 4. Domínio e tracking
- Atualizar `<title>` e `<meta>` com URL real
- Adicionar pixel Meta: colar no `<head>` antes do `</head>`
- Adicionar Google Analytics: colar snippet GA4 no `<head>`

### 5. Cor de marca
Se o médico tiver cor de marca diferente do azul cobalto `#1B6CA8`:
- Editar a variável `accent: '#1B6CA8'` no `tailwind.config` no `<script>`
- Trocar também todas as ocorrências de `text-accent`, `border-accent`, `bg-accent`, `text-blue-*` para a nova cor

---

## Publicação

### Opção A — GitHub Pages (gratuito)
1. Criar repositório público no GitHub
2. Fazer upload do `lp.html` como `index.html`
3. Ativar GitHub Pages em Settings → Pages → Branch: main

### Opção B — Vercel (gratuito, domínio próprio)
1. Criar conta em vercel.com
2. Drag & drop do arquivo `lp.html` renomeado para `index.html`
3. Conectar domínio em Settings → Domains

### Opção C — Hospedagem do consultório
Enviar o arquivo `lp.html` para o desenvolvedor da hospedagem atual.

---

## Compliance obrigatória antes de publicar

- [ ] Verificar que nenhum texto promete "tratamento" ou "cura" (CFM 1974/2011)
- [ ] Incluir link para Política de Privacidade (LGPD — dados sensíveis de menores)
- [ ] Confirmar com advogado de saúde o texto do disclaimer no rodapé
- [ ] Obter autorização escrita dos pais para uso de depoimentos com identificação

---

*Powered by Accelera 360*
