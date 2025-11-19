# Guia de Contribuição e Padrões do Projeto

---

## Estratégia de Branching  
Usamos uma variação leve do **Git Flow**, organizada da seguinte forma:

- **main** → código estável, pronto para produção  
- **develop** → branch principal de desenvolvimento  
- **feat/** → novas funcionalidades  
- **fix/** → correções de bugs  
- **hotfix/** → correções urgentes aplicadas diretamente na `main`  
- **refactor/** → melhorias internas sem alterar comportamento  
- **docs/** → atualizações na documentação  

---

## Fluxo de Trabalho Padrão

```bash
git checkout develop
git pull origin develop   # Sempre sincronize antes de iniciar

git checkout -b feat/minha-nova-feature
# ... faça seu trabalho com commits pequenos ...

git push origin feat/minha-nova-feature
```

Após finalizar: 
1. Abra um Pull Request. 
2. O PR deve apontar da sua branch → develop.
3. Aguarde revisão.

## Padrão de Mensagens de Commit

Formato recomendado:
```
<tipo>: <descrição curta>
```

### Tipos aceitos
- **feat:** nova funcionalidade  
- **fix:** correção de bug  
- **docs:** documentação  
- **refactor:** melhoria interna sem alterar comportamento  
- **test:** adição/ajuste de testes  
- **style:** formatação/código sem efeito funcional  
- **chore:** tarefas internas, configs, dependências  

### Exemplos
```
feat: adiciona componente de login
fix: corrige erro ao salvar usuário
docs: adiciona seção de instalação no README
refactor: simplifica lógica de autenticação
```
---

## Definition of Done (DoD) — Condições para Aprovar um PR

### Técnicos
- Código compila e executa sem erros  
- Todos os testes existentes passam  
- Novos testes foram incluídos quando necessário  
- Sem `console.log` desnecessário  
- Padrões do projeto respeitados  
- Branch atualizada com `develop`  

### Qualidade
- Código claro, organizado e legível  
- Feature completa conforme solicitado  
- Bons nomes para variáveis e funções  
- Comentários apenas onde realmente necessário  

### Documentação
- README ou documentação atualizada, quando aplicável  
- Descrição do PR explicando:
  - O que foi feito  
  - O motivo  
  - Como testar  

### Revisão
- Ao menos 1 reviewer aprovou  
- Todos os comentários foram resolvidos  

---

## Checklist para o Autor do PR

Antes de enviar:

- [ ] Atualizei minha branch com `develop`  
- [ ] Revisei meus commits  
- [ ] O PR tem título claro  
- [ ] Testei tudo localmente  
- [ ] Expliquei no PR como validar a mudança  
