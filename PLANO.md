# Plano: Site Profissional para Psicóloga Clínica

## Visão Geral

Site profissional tipo cartão de visita em Jekyll para uma psicóloga clínica, com design moderno e profissional, preparado para futura integração com CMS.

**Nome fictício**: Dra. Sofia Mendes  
**Especialidade**: Psicologia Clínica - Abordagem Psico-dinâmica  
**Modalidades**: Consultas online e presenciais em Lisboa

---

## Estrutura do Site

### Páginas Principais

1. **Homepage (`index.html`)**
   - Hero section com foto da psicóloga e call-to-action
   - **NOTA**: Foto da Dra. Sofia Mendes incluída no hero (`assets/images/dra-sofia-mendes.jpg`)
   - Resumo dos serviços
   - Últimos artigos do blog
   - Testemunhos (opcional)

2. **Sobre Mim (`pages/sobre.md`)**
   - História profissional
   - Formação académica (Ordem dos Psicólogos Portugueses)
   - Abordagem terapêutica
   - Valores e filosofia de trabalho

3. **Serviços (`pages/servicos.md`)**
   - Metodologia: Psicoterapia Psico-dinâmica
   - Patologias tratadas:
     - Depressão
     - Ansiedade
     - Stress
     - Perturbações do Sono
     - Luto e Perdas
     - Crises de Vida e Transições
   - Processo terapêutico
   - FAQ

4. **Consultas (`pages/consultas.md`)**
   - Modalidades: Online e Presencial
   - Locais fictícios em Lisboa:
     - **Consultório Avenidas**: Av. da República, 1050-123 Lisboa
     - **Consultório Alcântara**: Rua Prior do Crato, 1300-400 Lisboa
   - Horários de atendimento
   - Duração e valores (orientativos)

5. **Blog/Artigos (`pages/blog.html`)**
   - Lista de artigos sobre psicologia
   - Categorias e tags
   - Sistema de posts Jekyll

6. **Contactos (`pages/contactos.md`)**
   - Formulário de contacto simples
   - Telefone, email
   - Moradas dos consultórios
   - Mapa (embed Google Maps - opcional)

---

## Estrutura de Ficheiros Jekyll

```
site-draft/
├── _config.yml                 # Configuração principal
├── Gemfile                     # Dependências Ruby
├── Gemfile.lock               # Lock file (gerado)
├── README.md                  # Documentação do projeto
├── PLANO.md                   # Este ficheiro
│
├── _layouts/                  # Templates HTML
│   ├── default.html          # Layout base
│   ├── page.html             # Layout páginas estáticas
│   └── post.html             # Layout artigos
│
├── _includes/                # Componentes parciais
│   ├── header.html           # Cabeçalho + navegação
│   ├── footer.html           # Rodapé
│   ├── hero.html             # Hero section homepage
│   └── meta.html             # Meta tags SEO
│
├── _sass/                    # Estilos SCSS
│   ├── _base.scss            # Reset, variáveis, cores
│   ├── _layout.scss          # Grid, estrutura, containers
│   ├── _components.scss      # Botões, cards, forms
│   └── _responsive.scss      # Media queries
│
├── assets/
│   ├── css/
│   │   └── main.scss         # Ficheiro principal SCSS
│   ├── js/
│   │   └── main.js           # JavaScript (navegação mobile, etc)
│   └── images/
│       └── (imagens do site)
│
├── _posts/                   # Artigos do blog
│   ├── 2026-01-15-ansiedade-moderna.md
│   ├── 2026-01-22-importancia-sono.md
│   └── 2026-02-05-psicoterapia-psicodinamica.md
│
├── pages/                    # Páginas principais
│   ├── sobre.md
│   ├── servicos.md
│   ├── consultas.md
│   ├── blog.html
│   └── contactos.md
│
└── index.html               # Homepage
```

---

## Design e Estilo

### Paleta de Cores

**NOTA**: Tema acolhedor com cores quentes selecionado

**Primária**: Tons terrosos e quentes (acolhimento, conforto, confiança)
- Principal: `#C97959` (terracota suave)
- Principal escuro: `#A85C3F`
- Accent: `#D4A574` (dourado quente)

**Secundária**: Neutros quentes
- Texto escuro: `#3D2E29`
- Texto médio: `#5C4B43`
- Background: `#FFF9F5` (off-white quente)
- Branco: `#FFFFFF`

**Destaques**:
- Secundário suave: `#E8C5A8` (bege rosado)
- Destaque claro: `#F4E4D7` (creme)

### Tipografia

- **Títulos**: Playfair Display (serif elegante)
- **Corpo**: Inter ou Lato (sans-serif legível)
- **Tamanhos**: Sistema de escala modular (1.25)

### Componentes

- **Hero Section**: Imagem de fundo suave + overlay + texto centrado
- **Cards**: Sombra suave, bordas arredondadas, hover effects
- **Botões**: Call-to-action claros, estados hover/active
- **Navegação**: Sticky header, menu mobile hamburger
- **Footer**: Links úteis, copyright, redes sociais (opcional)

### Responsividade

- **Mobile-first**: Design base para móvel
- **Breakpoints**:
  - Mobile: < 768px
  - Tablet: 768px - 1024px
  - Desktop: > 1024px

---

## Conteúdo Fictício

### Dados da Psicóloga

**Nome**: Dra. Sofia Mendes  
**Cédula Profissional**: OPP nº 12345 (fictício)  
**Especialização**: Psicoterapia Psico-dinâmica  
**Experiência**: 8 anos de prática clínica  

**Formação**:
- Licenciatura em Psicologia - Universidade de Lisboa
- Mestrado em Psicologia Clínica - ISPA
- Pós-graduação em Psicoterapia Psico-dinâmica
- Membro efetivo da Ordem dos Psicólogos Portugueses

### Locais de Consulta

**Consultório Avenidas**  
Av. da República, 2450, 3º andar  
1050-123 Lisboa  
(Perto do Metro Saldanha)

**Consultório Alcântara**  
Rua Prior do Crato, 18, Sala 4  
1300-400 Lisboa  
(Perto do LX Factory)

### Contactos Fictícios

**Telefone**: +351 910 234 567  
**Email**: consultas@sofiamednes.pt (fictício)  
**Horário**: Segunda a Sexta, 9h-20h

---

## Artigos de Exemplo

### 1. "Ansiedade na Sociedade Moderna"
Aborda o aumento da ansiedade no contexto contemporâneo, ritmo acelerado, pressão social e estratégias de gestão.

### 2. "A Importância do Sono na Saúde Mental"
Explica a relação entre sono e bem-estar psicológico, higiene do sono e impacto das perturbações do sono.

### 3. "Psicoterapia Psico-dinâmica: O Que É?"
Introdução acessível à abordagem psico-dinâmica, conceitos principais e como funciona na prática.

---

## Configuração Jekyll

### _config.yml

```yaml
title: Dra. Sofia Mendes - Psicologia Clínica
description: >-
  Psicóloga Clínica em Lisboa. Consultas presenciais e online.
  Especializada em Psicoterapia Psico-dinâmica.
url: ""
baseurl: ""

# Build settings
markdown: kramdown
permalink: /blog/:year/:month/:day/:title/

# Plugins
plugins:
  - jekyll-seo-tag
  - jekyll-sitemap
  - jekyll-feed

# Collections
collections:
  posts:
    output: true
    permalink: /blog/:year/:month/:day/:title/

# Defaults
defaults:
  - scope:
      path: ""
      type: "posts"
    values:
      layout: "post"
  - scope:
      path: "pages"
      type: "pages"
    values:
      layout: "page"

# Navigation
navigation:
  - title: Início
    url: /
  - title: Sobre Mim
    url: /sobre/
  - title: Serviços
    url: /servicos/
  - title: Consultas
    url: /consultas/
  - title: Blog
    url: /blog/
  - title: Contactos
    url: /contactos/

# Contact info
contact:
  phone: "+351 910 234 567"
  email: "consultas@sofiamendes.pt"
  locations:
    - name: "Consultório Avenidas"
      address: "Av. da República, 2450, 3º andar"
      postal: "1050-123 Lisboa"
    - name: "Consultório Alcântara"
      address: "Rua Prior do Crato, 18, Sala 4"
      postal: "1300-400 Lisboa"
```

---

## Como Fazer Build

### Pré-requisitos

1. **Ruby** instalado (versão 2.7 ou superior)
2. **Bundler** instalado: `gem install bundler`

### Instalação

```bash
# 1. Instalar dependências
bundle install

# 2. Servir localmente (com live reload)
bundle exec jekyll serve

# 3. Aceder ao site
# http://localhost:4000
```

### Build para Produção

```bash
# Gerar site estático na pasta _site/
bundle exec jekyll build

# Build com ambiente de produção
JEKYLL_ENV=production bundle exec jekyll build
```

### Deploy

**Opções recomendadas**:

1. **Netlify** (recomendado)
   - Conectar repositório GitHub
   - Build command: `jekyll build`
   - Publish directory: `_site`

2. **GitHub Pages**
   - Push para branch `gh-pages` ou `main`
   - Ativar GitHub Pages nas settings

3. **Vercel**
   - Import do repositório
   - Framework preset: Jekyll
   - Deploy automático

---

## Preparação para CMS

### Estrutura Preparada para:

1. **Netlify CMS**
   - Ficheiro `admin/config.yml` facilmente adicionável
   - Collections já definidas no `_config.yml`
   - Front matter consistente

2. **Forestry.io / TinaCMS**
   - Estrutura de ficheiros compatível
   - Front matter schemas definidos

3. **CloudCannon**
   - Nativamente compatível com Jekyll
   - Edição visual out-of-the-box

### Front Matter Padrão

**Posts**:
```yaml
---
layout: post
title: "Título do Artigo"
date: 2026-02-10
author: "Dra. Sofia Mendes"
categories: [psicologia, saúde-mental]
tags: [ansiedade, bem-estar]
excerpt: "Breve resumo do artigo..."
image: /assets/images/posts/imagem.jpg
---
```

**Páginas**:
```yaml
---
layout: page
title: "Título da Página"
permalink: /url-da-pagina/
description: "Meta description para SEO"
---
```

---

## Otimizações Incluídas

### SEO
- Plugin `jekyll-seo-tag`
- Meta descriptions em todas as páginas
- Open Graph tags
- Structured data (Schema.org)
- Sitemap automático

### Performance
- CSS minificado em produção
- Imagens otimizadas
- Lazy loading (opcional)
- Critical CSS inline (opcional)

### Acessibilidade
- Estrutura HTML semântica
- Contraste de cores adequado (WCAG AA)
- Alt text em imagens
- Navegação por teclado
- ARIA labels onde necessário

---

## Melhorias Futuras (Opcional)

1. **Sistema de Agendamento**
   - Integração com Calendly ou similar
   - Formulário de marcação

2. **Newsletter**
   - Subscrição de email
   - Integração com Mailchimp/Buttondown

3. **Testemunhos**
   - Secção de feedback de clientes
   - Sistema de reviews

4. **Múltiplos Idiomas**
   - Plugin `jekyll-multiple-languages`
   - Versão PT/EN

5. **Blog Avançado**
   - Sistema de comentários (Disqus/Utterances)
   - Pesquisa (Algolia)
   - Categorias e tags expandidas

6. **Analytics**
   - Google Analytics
   - Plausible (privacy-focused)

---

## Notas de Manutenção

### Adicionar Novo Artigo

1. Criar ficheiro em `_posts/` com formato `YYYY-MM-DD-titulo.md`
2. Adicionar front matter completo
3. Escrever conteúdo em Markdown
4. Build e publicar

### Atualizar Conteúdo

1. Editar ficheiro Markdown correspondente
2. Commit e push (deploy automático com Netlify/Vercel)

### Alterar Design

1. Modificar ficheiros em `_sass/`
2. Variáveis de cor em `_sass/_base.scss`
3. Testar localmente antes de deploy

---

## Suporte e Documentação

- **Jekyll**: https://jekyllrb.com/docs/
- **Markdown**: https://www.markdownguide.org/
- **Liquid Templates**: https://shopify.github.io/liquid/

---

**Data de criação**: 10 de Fevereiro de 2026  
**Versão**: 1.0
