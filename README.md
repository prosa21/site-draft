# Site Profissional - Dra. Sofia Mendes | Psicologia Clínica

Site profissional em Jekyll para psicóloga clínica, com design moderno e preparado para integração futura com CMS.

## 📋 Sobre o Projeto

Este é um site tipo "cartão de visita profissional" desenvolvido em Jekyll, com:

- Design moderno e responsivo
- Páginas informativas sobre serviços de psicologia
- Blog para artigos sobre saúde mental
- Estrutura preparada para futura integração com CMS headless
- SEO otimizado
- Performance otimizada

## 🚀 Começar

### Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- **Ruby** (versão 2.7 ou superior)
- **Bundler** - Instalar com: `gem install bundler`
- **Git** (para controlo de versão)

### Instalação

1. Clone o repositório ou navegue até a pasta do projeto:

```bash
cd site-draft
```

2. Instale as dependências:

```bash
bundle install
```

3. Inicie o servidor de desenvolvimento:

```bash
bundle exec jekyll serve
```

4. Abra o browser em: **http://localhost:4000**

O site será recarregado automaticamente quando fizer alterações aos ficheiros.

## 📁 Estrutura do Projeto

```
site-draft/
├── _config.yml              # Configuração principal do Jekyll
├── Gemfile                  # Dependências Ruby
├── index.html              # Homepage
│
├── _layouts/               # Templates HTML
│   ├── default.html       # Layout base
│   ├── page.html          # Layout páginas estáticas
│   └── post.html          # Layout artigos blog
│
├── _includes/             # Componentes parciais
│   ├── header.html       # Cabeçalho + navegação
│   ├── footer.html       # Rodapé
│   ├── hero.html         # Hero section
│   └── meta.html         # Meta tags SEO
│
├── _sass/                # Estilos SCSS
│   ├── _base.scss        # Variáveis, reset, tipografia
│   ├── _layout.scss      # Estrutura e layouts
│   ├── _components.scss  # Componentes (botões, cards, etc)
│   └── _responsive.scss  # Utilitários responsivos
│
├── assets/
│   ├── css/
│   │   └── main.scss     # Ficheiro principal de estilos
│   ├── js/
│   │   └── main.js       # JavaScript
│   └── images/           # Imagens do site
│
├── _posts/               # Artigos do blog
│   └── YYYY-MM-DD-titulo.md
│
├── pages/                # Páginas principais
│   ├── sobre.md
│   ├── servicos.md
│   ├── consultas.md
│   ├── blog.html
│   └── contactos.md
│
├── PLANO.md             # Plano detalhado do projeto
└── README.md            # Este ficheiro
```

## ✏️ Editar Conteúdo

### Informações Gerais

Edite o ficheiro `_config.yml` para alterar:
- Nome, título, descrição do site
- Dados de contacto (telefone, email)
- Locais de consulta
- Navegação
- Áreas de intervenção

### Páginas

As páginas estão em formato Markdown na pasta `pages/`:

- `pages/sobre.md` - Página "Sobre Mim"
- `pages/servicos.md` - Serviços e metodologia
- `pages/consultas.md` - Informações práticas
- `pages/contactos.md` - Contactos

Para editar, abra o ficheiro e modifique o conteúdo em Markdown.

### Homepage

A homepage está em `index.html` e usa HTML/Liquid. Pode personalizar:
- Secções
- Conteúdo dos cards
- Links e botões

### Adicionar Artigos ao Blog

1. Crie um ficheiro em `_posts/` com o formato:
   ```
   YYYY-MM-DD-titulo-do-artigo.md
   ```

2. Adicione o front matter no início:
   ```yaml
   ---
   layout: post
   title: "Título do Artigo"
   date: 2026-02-10 10:00:00 +0000
   author: "Dra. Sofia Mendes"
   categories: [categoria1, categoria2]
   tags: [tag1, tag2, tag3]
   excerpt: "Breve resumo do artigo..."
   ---
   ```

3. Escreva o conteúdo em Markdown abaixo do front matter

4. O artigo aparecerá automaticamente na página do blog

## 🎨 Personalizar Design

### Cores

Edite as variáveis no ficheiro `_sass/_base.scss`:

```scss
$primary-color: #2C5F6F;      // Cor principal
$primary-light: #4A7C7E;      // Variante clara
$accent-color: #7FA89B;       // Cor de destaque
$text-dark: #2D3748;          // Texto escuro
$background: #F7FAFC;         // Fundo
```

### Tipografia

No mesmo ficheiro, altere as fontes:

```scss
$font-heading: 'Playfair Display', serif;
$font-body: 'Inter', sans-serif;
```

### Espaçamentos e Outros Estilos

- `_sass/_layout.scss` - Estrutura, header, footer, hero
- `_sass/_components.scss` - Botões, cards, componentes
- `_sass/_responsive.scss` - Utilitários e breakpoints

## 🚀 Build e Deployment

### Build Local

Para gerar o site estático:

```bash
bundle exec jekyll build
```

Os ficheiros gerados estarão na pasta `_site/`

### Build para Produção

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

### Deploy

#### Opção 1: Netlify (Recomendado)

1. Crie conta em [netlify.com](https://netlify.com)
2. Conecte o repositório GitHub
3. Configure build:
   - Build command: `jekyll build`
   - Publish directory: `_site`
4. Deploy automático!

**Domínio personalizado**: Configure nas settings do Netlify

#### Opção 2: GitHub Pages

1. Push para repositório GitHub
2. Vá a Settings > Pages
3. Selecione branch (main ou gh-pages)
4. O site ficará em: `https://username.github.io/repo-name`

#### Opção 3: Vercel

1. Importe o repositório em [vercel.com](https://vercel.com)
2. Vercel detecta automaticamente Jekyll
3. Deploy com um clique

### Domínio Personalizado

Após deploy, pode configurar um domínio personalizado:

1. Compre domínio (ex: sofiamendes.pt)
2. Configure DNS records:
   - Para Netlify/Vercel: Siga instruções da plataforma
   - Para GitHub Pages: CNAME record
3. Configure em `_config.yml`:
   ```yaml
   url: "https://www.sofiamendes.pt"
   ```

## 🔧 Integração com CMS

O site está preparado para integração futura com CMS headless:

### Netlify CMS

1. Adicione ficheiro `admin/config.yml`:
   ```yaml
   backend:
     name: git-gateway
     branch: main
   
   collections:
     - name: "posts"
       label: "Artigos"
       folder: "_posts"
       create: true
       fields:
         - {label: "Título", name: "title", widget: "string"}
         - {label: "Data", name: "date", widget: "datetime"}
         - {label: "Conteúdo", name: "body", widget: "markdown"}
   ```

2. Ative Git Gateway no Netlify
3. Aceda a: `https://seusite.com/admin`

### Forestry.io

1. Importe o site em [forestry.io](https://forestry.io)
2. Configure front matter templates
3. Edite conteúdo visualmente

### CloudCannon

1. Conecte repositório em [cloudcannon.com](https://cloudcannon.com)
2. Jekyll é suportado nativamente
3. Editor visual out-of-the-box

## 📱 Responsividade

O site é totalmente responsivo com breakpoints:

- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

Teste em diferentes dispositivos ou use DevTools do browser.

## ♿ Acessibilidade

O site segue boas práticas de acessibilidade:

- Estrutura HTML semântica
- Contraste de cores adequado (WCAG AA)
- Navegação por teclado
- ARIA labels
- Alt text em imagens (adicione quando usar imagens reais)

## 🔍 SEO

SEO otimizado através de:

- Plugin `jekyll-seo-tag` (meta tags automáticas)
- `jekyll-sitemap` (sitemap.xml gerado automaticamente)
- `jekyll-feed` (RSS feed)
- Meta descriptions em todas as páginas
- URLs amigáveis

**Dica**: Adicione Google Analytics editando `_includes/meta.html`

## 📝 Manutenção

### Atualizar Conteúdo

- **Páginas**: Edite ficheiros `.md` em `pages/`
- **Artigos**: Adicione ficheiros em `_posts/`
- **Dados**: Edite `_config.yml`

### Atualizar Dependências

```bash
bundle update
```

### Backup

Recomendo:
- Git para controlo de versão
- Repositório remoto (GitHub, GitLab, Bitbucket)
- Backups regulares da base de código

## 🐛 Resolução de Problemas

### Erro ao instalar gems

```bash
bundle update --bundler
bundle install
```

### Site não carrega estilos

Verifique se o servidor está a correr:
```bash
bundle exec jekyll serve
```

### Erro 404 em páginas

Verifique o `permalink` no front matter das páginas

### Mudanças não aparecem

1. Pare o servidor (Ctrl+C)
2. Limpe cache: `bundle exec jekyll clean`
3. Reinicie: `bundle exec jekyll serve`

## 📚 Recursos Úteis

- **Jekyll Docs**: https://jekyllrb.com/docs/
- **Liquid Syntax**: https://shopify.github.io/liquid/
- **Markdown Guide**: https://www.markdownguide.org/
- **SCSS Guide**: https://sass-lang.com/guide

## 🔐 Privacidade e RGPD

Lembre-se de:
- Adicionar página de Política de Privacidade
- Configurar cookies consent (se usar analytics/cookies)
- Implementar formulário de contacto conforme RGPD
- Informar sobre tratamento de dados pessoais

## 📞 Suporte

Para questões sobre Jekyll:
- Documentação oficial: https://jekyllrb.com
- Stack Overflow: Tag `jekyll`

## 📄 Licença

Este projeto é para uso pessoal/profissional. Adapte conforme necessário.

---

**Desenvolvido com Jekyll** | Última atualização: Fevereiro 2026

Para mais detalhes sobre o projeto, consulte `PLANO.md`
