# Finanças Claras - Educação Financeira

Blog estático com **Netlify CMS** para gerenciamento de conteúdo.

## 🎯 Objetivo

Fornecer educação financeira clara, prática e sem jargão em português.

## 📁 Estrutura do Projeto

```
.
├── admin/                    # Painel de administração
│   └── index.html           # Interface do Netlify CMS
├── conteudo/                # Conteúdo gerenciado pelo CMS
│   ├── artigos/             # Artigos do blog
│   ├── paginas/             # Páginas estáticas
│   └── _dados/              # Configurações JSON
├── public/                  # Arquivos estáticos
│   └── imagens/             # Imagens do site
├── config.yml               # Configuração do Netlify CMS
├── NETLIFY_CMS_SETUP.md     # Guia de configuração completo
├── QUICK_START.md           # Passo a passo rápido
└── CHECKLIST_NETLIFY_CMS.md # Checklist de implementação
```

## 🚀 Como Usar

### 1. Clone e Configure
```bash
git clone https://github.com/seu-usuario/financas-claras.git
cd financas-claras
git checkout main
```

### 2. Faça Deploy no Netlify
- Conecte seu repositório GitHub
- Deploy automático ativado
- Aguarde build (verde = sucesso)

### 3. Ative o CMS
- Vá para Site Settings > Access Control
- Enable Git Gateway
- Configure OAuth com GitHub

### 4. Acesse o Painel
```
https://seu-site.netlify.app/admin
```

## ✍️ Criar Novo Artigo

1. Abra o painel admin
2. Clique em "📝 Artigos"
3. Clique em "New Artigo"
4. Preencha os campos
5. Clique em "Publish"
6. GitHub Pull Request será criado automaticamente

## 📝 Formato de Artigos

Artigos são escritos em **Markdown** com front matter YAML:

```markdown
---
titulo: "Meu Artigo"
data: 2026-05-13T10:00:00Z
categoria: "Finanças Pessoais"
tempo_leitura: 5
descricao: "Resumo do artigo"
tags: ["tag1", "tag2"]
destaque: false
imagem: /imagens/capa.jpg
---

# Conteúdo aqui

Seu texto em markdown...
```

## 🎨 Categorias Disponíveis

- 💰 **Finanças Pessoais** - Orçamento, poupança, planejamento
- 📈 **Investimentos** - Ações, ETFs, renda fixa
- 🔄 **Hábitos** - Comportamento financeiro, mindset

## 🔧 Configuração

### Alterar Título do Site
Edite `/conteudo/_dados/configuracoes.json`

### Alterar Menu
Edite `/conteudo/_dados/menu.json`

### Personalizar CMS
Edite `/config.yml` para mudar campos, coleções, etc.

## 📚 Documentação

- [NETLIFY_CMS_SETUP.md](NETLIFY_CMS_SETUP.md) - Guia completo de configuração
- [QUICK_START.md](QUICK_START.md) - Passo a passo rápido
- [CHECKLIST_NETLIFY_CMS.md](CHECKLIST_NETLIFY_CMS.md) - Checklist de implementação
- [Documentação Netlify CMS](https://www.netlifycms.org/docs/intro/)

## 👥 Colaboradores

Para adicionar um colaborador:

1. No Netlify: Site Settings > Access Control > Authentication
2. Adicione o email do usuário
3. Ele receberá um convite por email

## 🐛 Troubleshooting

### Erro ao fazer login
- Verifique se Git Gateway está ativado
- Limpe cache/cookies
- Tente em modo anônimo

### Imagens não carregam
- Coloque em `public/imagens/`
- Use path `/imagens/arquivo.jpg`

### Mudanças não aparecem
- Verifique o commit no GitHub
- Faça rebuild no Netlify

## 📊 Estatísticas

- **Categorias**: 3
- **Campos por artigo**: 9
- **Idiomas suportados**: 2 (PT-BR, EN)

## 🛠️ Stack Técnico

- **CMS**: Netlify CMS v2.0.0
- **Hospedagem**: Netlify
- **Versionamento**: Git/GitHub
- **Markdown**: YAML Front Matter
- **Media**: Netlify Large Media (opcional)

## 📝 Licença

Este projeto está disponível sob a licença MIT.

## 📧 Suporte

Para dúvidas sobre Netlify CMS, consulte a [documentação oficial](https://www.netlifycms.org/).

---

**Construído com ❤️ para educação financeira em português**
