# Padrões de Commit

Esta organização segue as boas práticas do [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/).

### Por que utilizar Conventional Commits?

1. **Padronização e Clareza:**&#x20;

   O Conventional Commits define um formato claro e consistente para as mensagens, o que facilita a compreensão das mudanças no código por toda a equipe. Isso reduz ambiguidades e melhora a comunicação no time.

2. **Ferramentas e Automação:**&#x20;

   O uso de Conventional Commits habilita:

   - **Geração automática de changelogs:** Ferramentas como `standard-version` criam listas detalhadas de alterações.
   - **Validação de commits:** Ferramentas como `commitlint` garantem que as mensagens sigam o padrão.
   - **Pipeline CI/CD mais eficiente:** É possível disparar ações específicas no pipeline com base no tipo de commit.

3. **Melhora a Colaboração**

   Desenvolvedores, revisores e gerentes de projeto conseguem entender as alterações sem precisar abrir detalhes de cada commit.

   Novos membros do time podem se adaptar mais rapidamente ao fluxo de trabalho.

Abaixo estão as diretrizes para criar mensagens de commit claras e consistentes.

---

## Índice

1. [Estrutura da Mensagem](#estrutura-da-mensagem)
2. [Tipos Comuns de Commits](#tipos-comuns-de-commits)
3. [Mensagens de Corpo e Rodapé](#mensagens-de-corpo-e-rodapé)
4. [Dicas Úteis](#dicas-úteis)

---

## Estrutura da Mensagem

Cada commit deve seguir a seguinte estrutura:

```plaintext
<tipo>(escopo opcional): <descrição>

[corpo opcional]

[rodapé opcional]
```

### Exemplos:

```plaintext
feat: adicionar funcionalidade de login
fix(cadastro): corrigir erro no campo de e-mail
docs: atualizar README com instruções de instalação
chore: atualizar dependências
refactor(usuario): reorganizar lógica de validação
test: adicionar testes para a função X
```

---

## Tipos Comuns de Commits

### `feat`

Adição de uma nova funcionalidade ao projeto.\
**Exemplo:**

```plaintext
feat: implementar sistema de notificações
```

### `fix`

Correção de um bug ou problema no projeto.\
**Exemplo:**

```plaintext
fix(auth): corrigir erro na autenticação de usuários
```

### `docs`

Alterações na documentação, como README ou outros arquivos `.md`.\
**Exemplo:**

```plaintext
docs: criar guia de contribuição
```

### `style`

Alterações de estilo que não afetam o funcionamento do código (espaços, formatação, etc.).\
**Exemplo:**

```plaintext
style: ajustar indentação no arquivo main.js
```

### `refactor`

Refatoração de código sem alteração na funcionalidade.\
**Exemplo:**

```plaintext
refactor(carrinho): melhorar organização de métodos
```

### `test`

Adição ou modificação de testes automatizados.\
**Exemplo:**

```plaintext
test: adicionar teste para função de cálculo de preço
```

### `chore`

Tarefas que não afetam diretamente o código do produto (atualização de dependências, scripts de build, etc.).\
**Exemplo:**

```plaintext
chore: atualizar versão do eslint
```

---

## Mensagens de Corpo e Rodapé

### Corpo (opcional)

Use para descrever com mais detalhes o que foi alterado e por quê. Deve ter um tom objetivo e claro.

**Exemplo:**

```plaintext
fix(rota): corrigir erro de redirecionamento

Corrige o problema de redirecionamento incorreto quando o usuário tenta acessar uma rota protegida sem estar autenticado.
```

### Rodapé (opcional)

Use para informações extras, como links de tickets ou breaking changes.

- **Breaking changes**:

  ```plaintext
  BREAKING CHANGE: altera o formato da resposta da API
  ```

- **Referências**:

  ```plaintext
  Resolve: #123
  See: #456
  ```

---

## Dicas Úteis

1. **Seja claro e conciso**: A descrição deve deixar claro o propósito do commit.
2. **Evite mensagens genéricas**: Substitua "arrumado bug" por algo mais descritivo, como `fix(api): corrigir resposta com status 500`.
3. **Commits atômicos**: Cada commit deve representar uma mudança lógica única.

---

Adote essas práticas para facilitar a revisão de código e o rastreamento de alterações no projeto.

