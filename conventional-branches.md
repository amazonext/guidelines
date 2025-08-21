# Convenção de Branches e PRs do Projeto

Este documento define como **criar branches** e **abrir Pull Requests (PRs)** no nosso projeto.
A ideia é simples: todo mundo segue o mesmo padrão → repositório limpo, previsível e fácil de manter.

---

## Objetivo

* Garantir organização e rastreabilidade no código.
* Facilitar integração com o **Jira** ou qualquer outro **Kanban**.
* Evitar conflitos e bagunça nos merges.
* Deixar claro o que cada branch/PR resolve.

---

## Regras para criação de branches

### Estrutura do nome

Sempre use o formato:

```
<tipo>/<ID>-<descrição-curta>
```

### Tipos de branch

* **feature/** → para novas funcionalidades

  * Ex.: `feature/JIRA-1234-login-oauth`
* **fix/** → para correções de bugs não urgentes

  * Ex.: `fix/JIRA-5678-corrigir-layout`
* **hotfix/** → correção urgente em produção

  * Ex.: `hotfix/JIRA-91011-ajuste-autenticacao`
* **chore/** → mudanças não funcionais (dependências, configs, scripts)

  * Ex.: `chore/atualizar-dependencias`
* **docs/** → alterações de documentação

  * Ex.: `docs/adicionar-guia-api`

Importante: sempre inclua o ID da issue do Jira no nome da branch.

---

## Regras para Pull Requests (PRs)

* **Título do PR**:

  ```
  <tipo> | <ID> | <descrição curta>
  ```

  Exemplo: `Feature | JIRA-1234 | Implementar login com OAuth`

* **Descrição do PR** deve conter:

  * Link para a issue do Jira.
  * Resumo do que foi feito.
  * Checklist (quando aplicável).

* **Critérios para merge**:

  1. CI rodou e passou.
  2. Código revisado e aprovado por pelo menos 1 pessoa.
  3. Seguiu a convenção de commits (mensagens claras e padronizadas).

---

## Branches protegidas

* `main` → produção (ninguém faz push direto).
* `release/*` → estabilização de versões.

Merges só via PR aprovado.

---

## Fluxo no dia a dia

1. Pegue a issue no Jira.
2. Crie sua branch a partir da `main` (ou `develop`, se usarmos).

   ```bash
   git checkout -b feature/JIRA-1234-login-oauth
   ```
3. Desenvolva e faça commits claros.
4. Abra o PR com título e descrição corretos.
5. Aguarde revisão → ajustes se necessário.
6. Merge aprovado → branch pode ser apagada.

---

## O que não fazer

* Não criar branch com nomes vagos: `teste`, `nova-branch`, `arrumar`.
* Não abrir PR sem descrição.
* Não fazer push direto em `main`.

---

## Resumo

```
Tipos de branch:
- feature/<ID>-<desc>
- fix/<ID>-<desc>
- hotfix/<ID>-<desc>
- chore/<desc>
- docs/<desc>

PRs:
- Título: <tipo> | <ID> | <descrição curta>
- Link para a issue do Jira
- CI verde + 1 review
```
