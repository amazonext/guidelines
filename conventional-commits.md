# Convenção de commit

Este documento define um padrão de commits para manter um histórico de commits organizado e compreensível.

## Convenção de Commits

Os commits devem seguir a seguinte estrutura:

```
tipo(escopo): mensagem
```

- **tipo**: Define o tipo da alteração.
- **escopo** (opcional): Indica a parte do sistema afetada.
- **mensagem**: Breve descrição da alteração.

### Tipos de Commits

Os commits devem ser classificados de acordo com o tipo da alteração:

- **feat**: Adiciona uma nova funcionalidade.
- **fix**: Corrige um bug.
- **docs**: Atualizações na documentação.
- **style**: Mudanças que não afetam a lógica (espaçamento, formatação, etc.).
- **refactor**: Refatoração do código sem alterar funcionalidade.
- **perf**: Melhoria de desempenho.
- **test**: Adiciona ou modifica testes.
- **chore**: Tarefas gerais (builds, dependências, scripts, etc.).
- **revert**: Reverte um commit anterior.
- **build**: Mudanças que afetam o sistema de build ou dependências externas.
- **ci**: Mudanças nos processos de integração contínua.
- **security**: Correções e melhorias relacionadas à segurança.
- **deploy**: Mudanças relacionadas a processos de deploy.

### Exemplos de Commits

``` bash
git commit -m "feat(auth): adicionar login com Google"
git commit -m "fix(api): corrigir erro ao buscar usuário"
git commit -m "docs(readme): adicionar guia de instalação"
git commit -m "style(css): ajustar espaçamento de botoes"
git commit -m "refactor(database): otimizar consulta de usuários"
git commit -m "test(api): adicionar testes para rota de login"
git commit -m "chore(deps): atualizar dependências"
git commit -m "revert: reverter commit 123abc"
git commit -m "build(webpack): atualizar configuração do Webpack"
git commit -m "ci(actions): adicionar workflow de testes automatizados"
git commit -m "wip(dashboard): iniciar desenvolvimento do painel de controle"
git commit -m "hotfix(login): corrigir falha crítica na autenticação"
git commit -m "security(api): corrigir vulnerabilidade de injeção de SQL"
git commit -m "deploy(server): configurar variáveis de ambiente para produção"
```

### Regras Adicionais

- A mensagem deve ser escrita no **imperativo** (ex.: "adicionar" ao invés de "adicionado").
- O escopo é opcional, mas recomendável para maior clareza.
- Commits devem ser pequenos e focados em uma única mudança.

## Links
1. [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)
2. [Conventional Commits Pattern](https://medium.com/linkapi-solutions/conventional-commits-pattern-3778d1a1e657)
