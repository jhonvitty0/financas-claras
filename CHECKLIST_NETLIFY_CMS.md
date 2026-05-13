# Checklist Netlify CMS - Finanças Claras

## ✅ Arquivos Criados

- [x] `/admin/index.html` - Painel de administração
- [x] `/config.yml` - Configuração do CMS
- [x] `/conteudo/artigos/exemplo-artigo.md` - Exemplo de artigo
- [x] `/conteudo/_dados/configuracoes.json` - Dados do site
- [x] `/conteudo/_dados/sobre.json` - Página sobre
- [x] `/conteudo/_dados/menu.json` - Menu de navegação

## 🔧 Próximos Passos (Em Ordem)

### Etapa 1: Configuração Inicial
- [ ] 1. Criar repositório GitHub (ou inicializar git local)
- [ ] 2. Fazer commit de todos os arquivos do CMS
- [ ] 3. Fazer push para GitHub (`git push`)

### Etapa 2: Deploy no Netlify
- [ ] 4. Fazer login em https://app.netlify.com
- [ ] 5. Conectar repositório GitHub
- [ ] 6. Fazer deploy automático
- [ ] 7. Aguardar build (verde = sucesso)

### Etapa 3: Ativar Autenticação
- [ ] 8. Em Site Settings > Access Control > Authentication
- [ ] 9. Clique em "Enable Git Gateway"
- [ ] 10. Autorize no GitHub (criar OAuth app)
- [ ] 11. Adicione usuários colaboradores (se necessário)

### Etapa 4: Testar o CMS
- [ ] 12. Acesse https://seu-site.netlify.app/admin
- [ ] 13. Faça login com sua conta GitHub
- [ ] 14. Verifique se todas as seções carregam
- [ ] 15. Teste criar um novo artigo (modo preview)
- [ ] 16. Publish e verifique o commit no GitHub

## 📋 Atualizações Necessárias no config.yml

Substitua os valores abaixo com seus dados:

```yaml
backend:
  name: github
  repo: SEU_USUARIO/NOME_REPOSITORIO
  # Exemplo: joaovitor/financas-claras
```

```yaml
site_url: https://seu-site.netlify.app
# Exemplo: https://financas-claras.netlify.app
```

```yaml
logo_url: https://seu-site.netlify.app/seu-logo.png
# Exemplo: https://financas-claras.netlify.app/logo.png
```

## 🎨 Estrutura de Pastas Verificada

```
✓ admin/
  └── index.html
✓ conteudo/
  ├── artigos/
  │   └── exemplo-artigo.md
  ├── _dados/
  │   ├── configuracoes.json
  │   ├── sobre.json
  │   └── menu.json
  └── paginas/
✓ config.yml
```

## 🔐 Segurança

- [x] `config.yml` não contém tokens/senhas
- [x] `admin/index.html` usa Netlify Identity
- [x] Git Gateway fornece segurança OAuth
- [x] Apenas usuários autorizados podem editar

## 📚 Documentação de Referência

- [Netlify CMS Docs](https://www.netlifycms.org/docs/intro/)
- [GitHub Configuration](https://www.netlifycms.org/docs/backends/github/)
- [Netlify Getting Started](https://docs.netlify.com/get-started/overview/)

## 🚀 Após Configurar

1. **Criar mais artigos** via painel do CMS
2. **Implementar formulários** com Netlify Forms
3. **Configurar webhooks** para automações
4. **Adicionar CI/CD pipeline** para testes
5. **Personalizar estilos** do editor

## 📞 Suporte

Algo não funcionou? Verifique:
- [ ] Repositório é público
- [ ] Branch é "main"
- [ ] Git Gateway está ativado
- [ ] Você tem permissão no repositório
- [ ] Cache do navegador está limpo

---

**Data de início**: 13/05/2026
**Status**: ✅ Pronto para deploy

Boa sorte! 🎉
