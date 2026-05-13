# 09 - Glossário de Domínio

## 1. Termos do Negócio

### Camisa (Jersey)
O produto principal. Deve-se especificar se é "Modelo Jogador" (ajuste atlético) ou "Modelo Torcedor" (corte padrão).

Sinônimos proibidos: Blusa, camiseta, uniforme (salvo se for o kit completo).
Exemplo: "Camisa Seleção Brasileira 2026 Modelo Jogador".

### Patch
Aplicação termo-colante na manga ou peito (ex: Patch da Copa do Mundo ou de Campeão).

Sinônimos proibidos: Adesivo, figurinha.
Exemplo: "Adicionar Patch FIFA World Cup 2026 à manga direita".

### Personalização
Inclusão de nome e número nas costas da camisa.

Sinônimos proibidos: Estampa personalizada.
Exemplo: "Personalização: Nome: 'PELÉ', Número: '10'".

### SKU (Stock Keeping Unit)
Identificador único que combina modelo, tamanho e variação.

Exemplo: "SKU: BRA-2026-HOME-JOG-GG".

---

## 2. Termos Técnicos

### Spring Boot (Back-end)
Framework Java para a API. Deve seguir o padrão MVC/Service/Repository.

### React (Front-end)
Biblioteca para a interface. Uso obrigatório de Functional Components e Hooks.

### DTO (Data Transfer Object)
Objetos de transferência de dados entre Back e Front para evitar exposição da entidade de banco.

### JPA/Hibernate
Camada de persistência para o banco de dados relacional.

---

## 3. Convenções de Nomenclatura

| Categoria | Padrão | Exemplo |
| :--- | :--- | :--- |
| Entidades (Java) | PascalCase | ProdutoSelecao.java |
| Campos de Banco | snake_case | nome_jogador |
| API/JSON (Req/Res) | camelCase | nomeJogador |
| Variáveis/Métodos | camelCase | buscarPorId |
| Endpoints | kebab-case | /api/v1/camisas-selecoes |

---

## 4. Termos Ambíguos Resolvidos
Nenhum termo em divergência no momento.

---

## 5. Pedido para o Agente Documentador
Manter este arquivo consistente. Toda nova definição passa por humano antes de ser oficializada.

---

RESUMO PARA VALIDAÇÃO HUMANA
1. O que foi feito: Reestruturação do arquivo 09 sem marcadores de ponto (bullets) para facilitar cópia e leitura por código.
2. O que precisa de aprovação: O formato de texto limpo apenas com quebras de linha.
3. Pendente: Iniciar o arquivo 01 (Visão Geral).

Assinatura: Agente Documentador | 13/05/2026 | v1.4
