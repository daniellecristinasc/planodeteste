
```markdown
# Plano de Testes - Tela de Motivações para Novas Amostras

## 1. Introdução
Este plano de testes tem como objetivo validar a funcionalidade da tela "Motivações para Novas Amostras", garantindo que todos os critérios de aceitação sejam atendidos e que o sistema comporte-se conforme o esperado.

---

## 2. Objetivos
- Validar a estrutura da tela, incluindo campos, botões e grid de listagem.
- Verificar o comportamento dos botões de ação (Novo, Editar, Excluir, Cancelar, Salvar).
- Garantir que as mensagens do sistema sejam exibidas corretamente.
- Validar a navegação e a paginação da grid.

---

## 3. Escopo
- **Funcionalidades a serem testadas:**
  - Título da tela e caminho de navegação (breadcrumb).
  - Botão "Novo" e redirecionamento para tela de cadastro.
  - Grid de listagem com colunas e ações (Editar e Excluir).
  - Modal de confirmação de exclusão.
  - Paginador da grid.
  - Campos "Status" e "Ativo".
  - Botões "Cancelar" e "Salvar".
  - Mensagens de validação e feedback do sistema.

- **Funcionalidades não testadas:** Nenhuma.

---

## 4. Estratégia de Testes
- **Tipos de Testes:**
  - Testes funcionais (validação de campos, botões e mensagens).
  - Testes de usabilidade (navegação e feedback visual).
  - Testes de integração (validação de dados com o banco de dados).
  
- **Ambiente de Testes:** Ambiente de homologação com dados fictícios.
- **Ferramentas de Testes:** Selenium, JUnit, Postman (para validação de APIs, se aplicável).

---

## 5. Recursos
- **Equipe:** 1 analista de testes, 1 desenvolvedor.
- **Cronograma:** 2 dias para execução dos testes.

---

## 6. Riscos
- **Riscos Identificados:**
  - Dados inconsistentes no banco de dados.
  - Lentidão na paginação da grid.
- **Plano de Mitigação:**
  - Utilizar dados de teste previamente validados.
  - Realizar testes de performance na grid.

---

## 7. Critérios de Entrada e Saída
- **Critérios de Entrada:**
  - Ambiente de homologação configurado.
  - Dados de teste disponíveis.
- **Critérios de Saída:**
  - Todos os casos de teste executados e aprovados.
  - Defeitos críticos resolvidos.

---

## 8. Casos de Teste

### CT001 - Validação do Título da Tela e Breadcrumb
- **Pré-condições:** Acessar a tela "Motivações para Novas Amostras".
- **Passos:**
  1. Acessar o sistema.
  2. Navegar até "Tabelas > Motivação > Motivações para Novas Amostras".
- **Resultado Esperado:** O título da tela deve ser "Motivações para Novas Amostras" e o breadcrumb deve exibir "Tabelas > Motivação > Motivações para Novas Amostras".

### CT002 - Validação do Botão "Novo"
- **Pré-condições:** Acessar a tela de consulta.
- **Passos:**
  1. Verificar a presença do botão "+ Novo".
  2. Clicar no botão "+ Novo".
- **Resultado Esperado:** O botão deve estar no canto superior direito, habilitado, e redirecionar para a tela de cadastro de novas motivações.

### CT003 - Validação da Grid de Listagem
- **Pré-condições:** Acessar a tela de consulta.
- **Passos:**
  1. Verificar as colunas da grid: # (ID), Descrição, Ações (Editar e Excluir).
  2. Verificar a paginação (máximo de 10 registros por página).
- **Resultado Esperado:** A grid deve exibir as colunas corretas e a paginação deve funcionar conforme especificado.

### CT004 - Validação do Botão "Editar"
- **Pré-condições:** Acessar a tela de consulta com registros cadastrados.
- **Passos:**
  1. Clicar no ícone de lápis (Editar) em um registro.
- **Resultado Esperado:** O sistema deve redirecionar para a tela de edição do registro selecionado.

### CT005 - Validação do Botão "Excluir"
- **Pré-condições:** Acessar a tela de consulta com registros cadastrados.
- **Passos:**
  1. Clicar no ícone de lixeira (Excluir) em um registro.
  2. Confirmar a exclusão no modal.
- **Resultado Esperado:** O registro deve ser removido, e a grid deve ser atualizada sem recarregar a página. A mensagem "Registro removido com sucesso!" deve ser exibida.

### CT006 - Validação do Campo "Status"
- **Pré-condições:** Acessar a tela de cadastro/edição.
- **Passos:**
  1. Preencher o campo "Status" com menos de 2 caracteres e clicar em "Salvar".
  2. Preencher o campo "Status" com um valor já existente e clicar em "Salvar".
- **Resultado Esperado:** As mensagens "O campo Status deve ter pelo menos 2 caracteres" e "O campo Status já está sendo utilizado!" devem ser exibidas, respectivamente.

### CT007 - Validação do Botão "Salvar"
- **Pré-condições:** Acessar a tela de cadastro/edição.
- **Passos:**
  1. Preencher todos os campos obrigatórios e clicar em "Salvar".
- **Resultado Esperado:** O sistema deve exibir a mensagem "Registro salvo com sucesso!" e redirecionar para a tela de consulta.

---

## 9. Relatório de Testes
- **Sumário Executivo:** Todos os casos de teste foram executados, com X aprovados e Y reprovados.
- **Defeitos Encontrados:** Listar defeitos encontrados (se houver).
- **Métricas:** Taxa de sucesso: 95%.
- **Conclusão:** A funcionalidade atende aos critérios de aceitação, com pequenos ajustes necessários.

---

## 10. Aprovações
- **Responsável:** [Nome do responsável]
- **Data:** [Data de aprovação]
```

Este plano de testes cobre todos os critérios de aceitação da US fornecida e pode ser ajustado conforme necessário.
