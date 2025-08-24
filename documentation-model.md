# Modelo de Documentação de Tarefas

**Objetivo:** Garantir que todas as tarefas realizadas tenham registro claro, rastreável e padronizado, facilitando análise, revisão e integração no projeto.

---

## 1. Estrutura da Documentação

Cada tarefa deve conter as seguintes informações:

1. **Título da Tarefa**

   - Nome curto e direto da atividade realizada.

2. **Descrição do que foi feito**

   - Explicação detalhada das alterações implementadas ou do recurso desenvolvido.
   - Exemplo:

     > Implementação da tela de login com validação de campos e integração com a API de autenticação.

3. **Como foi feito**

   - Passo a passo técnico resumido do que foi feito.
   - Tecnologias, bibliotecas ou metodologias utilizadas.
   - Exemplo:

     > - Criada a tela de login em React Native
     > - Validação dos campos com Yup
     > - Integração com endpoint `/api/login` usando fetch

4. **IDs de rastreio**

   - **ID da tarefa no Jira:** \[JIRA-123]
   - **ID do commit no GitHub:** \[abc123def456]

5. **PR associado**

   - Link para o Pull Request correspondente.
   - Observação de status: aberto, revisado ou aprovado.

6. **Observações/Comentários**

   - Qualquer detalhe relevante, dúvidas ou melhorias sugeridas.

7. Anexo de template de documentação de tarefas

[**TEMPLATE DE DOCUMENTAÇÃO DE TAREFAS**](./template-documentation.md)

---

## 2. Fluxo de Documentação e Análise

**Passo a passo para cada tarefa:**

1. Desenvolvedor cria o **PR** (Pull Request) no GitHub.
2. Preenche a documentação seguindo o modelo acima.
3. Documento e PR vão para **análise da equipe**.
4. A equipe realiza **testes** e valida se tudo está correto.
5. **Resultado da análise:**

   - **Aprovado:** PR e documentação finalizados.
   - **Pendência:** Comentários no PR explicando o que falta ou sugerindo melhorias.

> 💡 Dica: Mantendo esse fluxo, o projeto ganha **clareza, rastreabilidade e organização**, e revisões futuras ficam muito mais simples.

---

## 3. Exemplo de Documento Preenchido

- **Título da Tarefa:** Implementar Tela de Login
- **Descrição do que foi feito:** Criada tela de login com validação de campos e integração com API.
- **Como foi feito:**

  - Tela desenvolvida em React Native
  - Validação com Yup
  - Requisição POST para `/api/login`

- **ID da tarefa no Jira:** \[JIRA-101]
- **ID do commit no GitHub:** \[abc123def456]
- **PR associado:** \[Link do PR]
- **Observações:** Nenhuma pendência identificada
