# Guia de Configuração do Netlify CMS - Finanças Claras

## 📋 Passos para Ativar o Netlify CMS

### 1. **Repositório GitHub**
Certifique-se de que seu site está em um repositório GitHub público:
- Acesse: https://github.com/new
- Crie um repositório com o nome desejado
- Faça upload dos arquivos para o repositório

### 2. **Conectar ao Netlify**
1. Faça login em https://app.netlify.com
2. Clique em "Add new site" > "Import an existing project"
3. Selecione GitHub e autorize
4. Escolha seu repositório
5. Configure as variáveis de build se necessário

### 3. **Configurar o config.yml**
Atualize o arquivo `config.yml` com:

```yaml
backend:
  name: github
  repo: SEU_USUARIO/NOME_REPOSITORIO  # Ex: joaovitor/financas-claras
  branch: main
  auth_endpoint: /auth

media_folder: public/imagens
public_folder: /imagens

site_url: https://seu-dominio.netlify.app
logo_url: https://seu-dominio.netlify.app/logo.png

collections:
  - name: "artigos"
    label: "Artigos"
    folder: "conteudo/artigos"
    create: true
    slug: "{{slug}}"
    editor:
      preview: true
    fields:
      - { label: "Título", name: "titulo", widget: "string" }
      - { label: "Data", name: "data", widget: "datetime" }
      - { label: "Categoria", name: "categoria", widget: "select", options: ["Finanças Pessoais", "Investimentos", "Hábitos"] }
      - { label: "Tempo de Leitura", name: "tempo_leitura", widget: "number" }
      - { label: "Conteúdo", name: "body", widget: "markdown" }
```

### 4. **Usar o Painel de Admin**
Acesse: `https://seu-dominio.netlify.app/admin`

### 5. **Autenticação**
- Clique em "Login com GitHub"
- Autorize a aplicação Netlify
- Comece a gerenciar conteúdo!

## 🔐 Configuração de Acesso

### Adicionar Múltiplos Usuários
No Netlify:
1. Site Settings > Access Control > Authentication
2. Clique em "Enable Git Gateway"
3. Convide colaboradores via email

### Variáveis de Ambiente
Se necessário, adicione no Netlify:
- `GITHUB_TOKEN`: seu token GitHub pessoal

## 📁 Estrutura de Pastas Recomendada

```
project/
├── admin/
│   └── index.html
├── public/
│   ├── imagens/
│   └── index.html
├── conteudo/
│   ├── artigos/
│   │   └── exemplo-artigo.md
│   └── configuracoes.json
├── config.yml
└── package.json
```

## ✅ Checklist de Configuração

- [ ] Repositório criado no GitHub
- [ ] Código enviado (git push)
- [ ] Site conectado ao Netlify
- [ ] config.yml atualizado com dados corretos
- [ ] Pasta `/admin` criada
- [ ] Identity widget adicionado ao HTML
- [ ] Git Gateway ativado
- [ ] Testado login em `/admin`

## 🚀 Próximos Passos

1. **Criar estrutura de conteúdo**: Organize seus artigos em arquivos Markdown
2. **Configurar workflows**: Implemente revisão antes de publicação
3. **Personalizar UI**: Customize o logo e cores do CMS
4. **Backup automático**: Configure backups dos seus artigos

## 📖 Documentação Oficial

- Netlify CMS: https://www.netlifycms.org/docs/intro/
- Guia de Configuração: https://www.netlifycms.org/docs/backends/github/
- Documentação Completa: https://www.netlifycms.org/docs/

## 💡 Dicas

- Use o modo de prévia para ver como fica antes de publicar
- Organize artigos por pasta de ano/mês para fácil manutenção
- Configure webhooks para notificações de mudanças
- Mantenha backups locais dos arquivos de conteúdo
