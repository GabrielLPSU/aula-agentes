# 00 - Orientação para Agentes

## 1. Contexto e Stack Técnica

Este projeto consiste no desenvolvimento de um e-commerce de camisas de seleções de futebol.

### Stack Oficial

Back-end: Java Spring Boot.

Front-end Mobile: React Native com Expo.

Estrutura: Sistema multiagente coordenado por humano, operando de forma incremental e modular.

---

## 2. Ordem de Leitura e Estrutura de Arquivos

Todo agente deve ler obrigatoriamente este arquivo e o `09_glossario_dominio.md` antes de qualquer tarefa.

O projeto segue esta estrutura de 10 arquivos:

| Arquivo | Objetivo |
| :--- | :--- |
| `00_orientacao_agentes.md` | Regras gerais (este arquivo) |
| `01_visao_geral.md` | Escopo e atores |
| `02_requisitos_e_regras_de_negocio.md` | O que o sistema deve fazer |
| `03_modelagem_banco_e_dados.md` | Estrutura de dados (SQL/Entidades) |
| `04_contratos_de_api.md` | Contratos REST (essencial antes do código) |
| `05_desenvolvimento_backend_modulo.md` | Implementação Spring Boot |
| `06_desenvolvimento_frontend_mobile_modulo.md` | Implementação React Native |
| `07_plano_de_testes.md` | Estratégia de verificação |
| `08_log_de_evolucao.md` | Histórico e rastreabilidade |
| `09_glossario_dominio.md` | Termos técnicos do e-commerce |

---

## 3. Regras Universais de Operação

### Contratos Primeiro
O código dos arquivos `05` e `06` só pode ser iniciado após o `04_contratos_de_api.md` estar validado pelo humano.

### Testes Obrigatórios
Todo código gerado deve acompanhar seus respectivos testes unitários ou de integração.

### Fidelidade ao Contrato
Agentes de Back-end e Front-end não podem alterar o arquivo `04_contratos_de_api.md`.

Caso exista necessidade de alteração, deve-se abrir divergência no `08_log_de_evolucao.md`.

### Validação Humana
Nenhum agente avança para a próxima etapa do fluxo sem aprovação explícita do coordenador humano.

### Responsabilidade Única
Cada agente só pode escrever nos arquivos permitidos pelo seu papel.

---

## 4. Definição dos Agentes e Fronteiras

| Agente | Responsabilidade | Restrições |
| :--- | :--- | :--- |
| Arquiteto | Define estrutura e modelagem (`01`, `02`, `03`) | Não escreve código de aplicação |
| Designer de API | Cria contratos REST no arquivo `04` | Não decide arquitetura |
| Agente Back-end | Implementa Spring Boot baseado nos arquivos `04` e `05` | Não altera contratos |
| Agente Front-end/Mobile | Implementa React Native baseado nos arquivos `04` e `06` | Não altera contratos |
| Agente QA | Cria planos de teste (`07`) e valida saídas | Não corrige código |
| Documentador | Consolida log de evolução (`08`) e mantém glossário (`09`) | Não altera regras de negócio |

---

## 5. Protocolo de Divergência

Ao identificar conflito, erro ou impossibilidade técnica, o agente deve interromper a tarefa e registrar uma das tags abaixo no arquivo `08_log_de_evolucao.md`:

| Tag | Uso |
| :--- | :--- |
| `[PENDENTE]` | Falta decisão ou informação humana |
| `[QUESTIONAMENTO]` | Suspeita de erro em artefato já aprovado |
| `[CONFLITO]` | Contradição entre dois arquivos |
| `[BLOQUEIO]` | Impossibilidade técnica na implementação |

### Exemplos

```txt
[CONFLITO] Modelagem do banco diverge do contrato REST do endpoint de produtos.
