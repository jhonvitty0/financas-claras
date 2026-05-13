# Começar com Netlify CMS - Passo a Passo Rápido

## 🚀 Setup Inicial (5 minutos)

### 1. Clone ou Crie o Repositório no GitHub
```bash
# Se for novo repo
git init
git add .
git commit -m "Initial commit with Netlify CMS setup"
git branch -M main
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
git push -u origin main
```

### 2. Acesse Netlify
- Vá para: https://app.netlify.com
- Clique em "New site from Git"
- Conecte com GitHub
- Selecione seu repositório

### 3. Configure o Site
- **Build command**: deixar vazio (ou sua build command se aplicável)
- **Publish directory**: `.` (raiz)
- Clique em "Deploy site"

### 4. Ative a Autenticação GitHub
- Em Site Settings > **Access control** > **Authentication**
- Clique em "Enable Git Gateway"
- Você será redirecionado para o GitHub para criar um OAuth app

### 5. Acesse o Admin
Após o site estar online, acesse:
```
https://seu-site.netlify.app/admin
```

## ✅ Estrutura de Pastas Necessária

Crie localmente estas pastas:

```
seu-projeto/
├── admin/
│   └── index.html (✅ já criado)
├── conteudo/
│   ├── artigos/
│   │   └── (seus artigos em .md)
│   ├── paginas/
│   └── _dados/
│       ├── configuracoes.json
│       ├── sobre.json
│       └── menu.json
├── public/
│   └── imagens/
│       └── (coloque seus logos e imagens aqui)
├── config.yml (✅ já criado)
└── README.md
```

### Criar arquivos JSON de dados:

**conteudo/_dados/configuracoes.json:**
```json
{
  "titulo": "Finanças Claras",
  "subtitulo": "Educação financeira sem jargão",
  "descricao": "Aprenda finanças pessoais, investimentos e hábitos cotidianos",
  "email": "contato@financas-claras.com",
  "autor_padrao": "Equipe Finanças Claras",
  "meta_descricao": "Educação financeira em português, clara e prática"
}
```

**conteudo/_dados/sobre.json:**
```json
{
  "missao": "Democratizar o conhecimento financeiro com conteúdo claro e responsável",
  "autor": "Uma equipe apaixonada por educação financeira",
  "foto_autor": "/imagens/autor.jpg"
}
```

**conteudo/_dados/menu.json:**
```json
{
  "items": [
    { "label": "Início", "url": "/" },
    { "label": "Artigos", "url": "/artigos" },
    { "label": "Sobre", "url": "/sobre" },
    { "label": "Contato", "url": "/contato" }
  ]
}
```

## 📝 Criar Primeiro Artigo

1. Vá para http://seu-site.netlify.app/admin
2. Clique em "📝 Artigos"
3. Clique em "New Artigo"
4. Preencha os campos:
   - Título: "Meu Primeiro Artigo"
   - Data: hoje
   - Slug: meu-primeiro-artigo
   - Categoria: Finanças Pessoais
   - Conteúdo: escreva em Markdown
5. Clique em "Save" (vai criar um Pull Request)
6. Publique o PR no GitHub

## 🔧 Comandos Git Úteis

```bash
# Ver status
git status

# Adicionar alterações
git add .

# Fazer commit
git commit -m "Adicionar novo artigo"

# Enviar para GitHub
git push origin main
```

## 🎨 Customize Seu CMS

No arquivo `config.yml`, você pode:
- Mudar nomes de coleções (exemplo: trocar "Artigos" por "Blog Posts")
- Adicionar/remover campos
- Organizar filtros
- Ajustar media folders

## 📱 Acessar de Qualquer Lugar

A URL é sempre:
```
https://seu-dominio.netlify.app/admin
```

Nada precisa estar instalado localmente para usar o CMS!

## ⚠️ Troubleshooting

### "Erro ao fazer login"
- Verifique se Git Gateway está ativado
- Verifique se o repositório é público
- Limpe cache/cookies

### "Não consigo salvar artigos"
- Verifique as permissões do repositório no GitHub
- Verifique se o branch é "main"
- Verifique os campos obrigatórios

### "Imagens não aparecem"
- Coloque as imagens em `public/imagens/`
- Use o path `/imagens/nome-arquivo.jpg` no CMS

## 🌐 Domínio Customizado (Opcional)

- Em Netlify Settings > Domain Management
- Adicione seu domínio customizado
- Siga as instruções de DNS

## 🎓 Próxima Aula

- Implementar workflows de revisão
- Configurar webhooks
- Conectar forms com Netlify Forms
- Configurar CI/CD pipeline

Boa sorte! 🚀
