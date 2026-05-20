# 01 - Visão Geral do Projeto

---

## 1. Problema e Objetivo

O objetivo deste projeto é desenvolver uma plataforma de e-commerce especializada em camisas de seleções de futebol,
permitindo que torcedores visualizem, pesquisem e adquiram uniformes oficiais de forma ágil,
segura e intuitiva através de uma aplicação mobile.

O sistema deve contemplar:

- Camisas modelo torcedor
- Camisas modelo jogador
- Personalização com nome e número
- Aplicação de patches oficiais
- Gestão de estoque em tempo real
- Administração completa do catálogo

A aplicação será construída utilizando arquitetura modular e orientada a contratos de API.

---

## 2. Escopo do Projeto

O sistema abrangerá as seguintes funcionalidades principais:

### Gestão de Acesso

- Login de clientes
- Login administrativo
- Controle de permissões por perfil
- Recuperação de senha
- Persistência de sessão

---

### Catálogo de Produtos

- Tela Home com produtos em destaque
- Pesquisa avançada por:
  - Seleção
  - Modelo
  - Tamanho
  - Disponibilidade
  - Faixa de preço
- Filtros dinâmicos
- Visualização detalhada da camisa
- Galeria de imagens
- Exibição de estoque disponível

---

### Carrinho de Compras

- Adição e remoção de itens
- Alteração de quantidade
- Persistência local no dispositivo
- Cálculo automático de subtotal
- Validação de estoque antes do checkout

---

### Fluxo de Checkout

- Resumo da compra
- Escolha de endereço
- Escolha de forma de pagamento
- Confirmação do pedido
- Histórico de pedidos

---

### Gestão de Endereços

- Cadastro de múltiplos endereços
- Edição e remoção
- Definição de endereço principal

---

## 3. Painel Administrativo

O sistema contará com uma área administrativa exclusiva para gerenciamento operacional da loja.
- Analise com graficos e tabelas sobre as vendas e usos do app.

---

### Gestão de Produtos

O administrador poderá:

- Criar produtos
- Editar produtos
- Remover produtos
- Alterar preços
- Atualizar descrições
- Gerenciar imagens
- Definir categorias
- Definir modelo da camisa (torcedor/jogador)

---

### Gestão de Estoque

O administrador poderá:

- Visualizar estoque atual
- Atualizar quantidade disponível
- Controlar estoque por tamanho
- Bloquear produtos sem estoque
- Receber alertas de baixo estoque
- Registrar entrada e saída de itens

---

### Gestão de Itens e Variantes

Cada camisa poderá possuir:

- Tamanhos diferentes
- SKU único
- Variações de modelo
- Personalização opcional
- Patches opcionais

O sistema deve permitir:

- Cadastro de variantes
- Controle individual de estoque por variante
- Associação de SKU por item
- Controle de disponibilidade

---

### Gestão de Pedidos

O administrador poderá:

- Visualizar pedidos realizados
- Atualizar status do pedido
- Confirmar pagamento
- Atualizar envio
- Cancelar pedidos
- Consultar histórico de movimentações

---

## 4. Telas Previstas

### Área do Cliente

| Tela | Objetivo |
| :--- | :--- |
| Splash Screen | Inicialização do aplicativo |
| Login | Autenticação |
| Cadastro | Criação de conta |
| Home | Catálogo principal |
| Detalhe do Produto | Visualização da camisa |
| Carrinho | Gestão de itens selecionados |
| Checkout | Finalização da compra |
| Endereços | Gestão de entrega |
| Perfil | Dados do usuário |
| Meus Pedidos | Histórico de compras |

---

### Área Administrativa

| Tela | Objetivo |
| :--- | :--- |
| Dashboard Admin | Resumo operacional |
| Gestão de Produtos | CRUD de camisas |
| Gestão de Estoque | Controle de quantidades |
| Gestão de Variantes | Controle de tamanhos/SKUs |
| Gestão de Pedidos | Administração de vendas |
| Gestão de Usuários | Controle administrativo |
| Relatórios | Métricas e indicadores |

---

## 5. Atores Identificados

### Cliente

Usuário responsável por:

- Navegar no catálogo
- Pesquisar produtos
- Gerenciar carrinho
- Cadastrar endereços
- Finalizar compras
- Acompanhar pedidos

---

### Administrador

Usuário responsável por:

- Gestão do catálogo
- Controle de estoque
- Cadastro de produtos
- Gestão de variantes
- Visualização de pedidos
- Administração operacional da loja

---

## 6. Restrições Técnicas

As seguintes diretrizes são obrigatórias:

### Back-end

- Java Spring Boot
- Arquitetura em camadas:
  - Controller
  - Service
  - Repository
- Uso obrigatório de DTOs
- Persistência com JPA/Hibernate
- API REST padronizada

---

### Front-end Mobile

- React Native com Expo
- Functional Components
- Hooks
- TypeScript
- Navegação modular
- Gerenciamento de estado
- Consumo exclusivo via API REST

---

### Comunicação

Toda comunicação entre Front-end e Back-end deverá seguir rigorosamente os contratos definidos no arquivo:

`04_contratos_de_api.md`

---

## 7. Requisitos Não Funcionais

### Segurança

- Proteção de autenticação
- Criptografia de senhas
- Controle de acesso por perfil
- Proteção contra exposição de dados sensíveis

---

### Performance

- Carregamento otimizado de imagens
- Cache local de dados
- Paginação no catálogo
- Respostas rápidas da API

---

### Escalabilidade

A arquitetura deve permitir:

- Inclusão de novos módulos
- Novas categorias de produtos
- Integração futura com gateways de pagamento
- Expansão para múltiplas seleções e competições

---

## 8. Riscos do Projeto

| Risco | Impacto |
| :--- | :--- |
| Exposição de dados sensíveis | Alto |
| Inconsistência entre estoque e carrinho local | Alto |
| Lentidão no carregamento de imagens | Médio |
| Divergência entre contratos e implementação | Alto |
| Erros de sincronização de estoque | Alto |
| Crescimento desorganizado da API | Médio |

---

## 9. Premissas do Projeto

O projeto assume que:

- O aplicativo será exclusivamente mobile
- O administrador utilizará interface interna autenticada
- O estoque será controlado pelo Back-end
- O carrinho utilizará persistência local
- Os contratos REST serão a única fonte oficial de integração

---

RESUMO PARA VALIDAÇÃO HUMANA

1. O que foi feito:
Expansão completa do arquivo `01_visao_geral.md` com inclusão de painel administrativo, gestão de estoque, gestão de itens/variantes, listagem de telas previstas e detalhamento técnico do sistema.

2. O que precisa de aprovação:
Validação das funcionalidades administrativas e confirmação do fluxo de estoque e variantes por SKU.

3. Próximo passo previsto:
Iniciar o arquivo `02_requisitos_e_regras_de_negocio.md`.

Assinatura: Agente Arquiteto | 20/05/2026 | v1.1
