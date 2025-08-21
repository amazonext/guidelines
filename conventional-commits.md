# Convenção de Commits

Este documento define um padrão de commits para manter um histórico de commits organizado e compreensível. A convenção de commits garante clareza, rastreabilidade e comunicação eficaz entre desenvolvedores.

## Objetivos

* Facilitar a leitura do histórico de mudanças.
* Permitir geração automatizada de changelogs.
* Ajudar na identificação rápida de correções, novas features e breaking changes.
* Melhorar a comunicação entre times de desenvolvimento.

---

## Estrutura do Commit

Um commit deve seguir o formato:

```text
<tipo>(<escopo>): <descrição breve>
```

* **tipo** → categoria da mudança.
* **escopo** → (opcional) parte do sistema afetada.
* **descrição breve** → explicação curta e direta.

Exemplo:

```text
feat(auth): adiciona fluxo de login com JWT
```

---

## Tipos de Commits

| Tipo         | Uso                                                      |
| ------------ | -------------------------------------------------------- |
| **feat**     | Implementação de nova funcionalidade.                    |
| **fix**      | Correção de bugs.                                        |
| **docs**     | Alterações na documentação.                              |
| **style**    | Ajustes de formatação, sem impacto no código.            |
| **refactor** | Refatoração de código sem alterar comportamento.         |
| **test**     | Adição ou modificação de testes.                         |
| **chore**    | Tarefas auxiliares (build, configs, dependências, etc.). |
| **perf**     | Alterações relacionadas a desempenho.                    |
| **ci**       | Ajustes de integração contínua.                          |

---

## Commits Especiais

* **BREAKING CHANGE** → mudanças que quebram compatibilidade.
  Exemplo:

```
feat(api): altera endpoint de /login para /auth/login

BREAKING CHANGE: clientes devem atualizar a rota de autenticação.
```

* **Revert** → quando um commit desfaz outro.
  Exemplo:

```
revert: "feat(auth): adiciona fluxo de login com JWT"
```

---

## Boas Práticas

* Escreva descrições curtas e objetivas (máx. 72 caracteres).
* Use verbos no **imperativo** (ex: "adiciona", e não "adicionado").
* Commits pequenos e focados em uma única mudança.
