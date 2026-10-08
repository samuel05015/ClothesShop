# Operação de varejo de moda

## ADDED Requirements

### Requirement: Estoque por variação com rastreabilidade local

O sistema SHALL manter o saldo separadamente para cada SKU e registrar a data, a quantidade e o motivo de cada ajuste realizado na interface.

#### Scenario: Entrada em uma grade

- **WHEN** o operador adiciona três peças ao SKU de cor preta e tamanho M
- **THEN** somente esse SKU aumenta em três unidades e a movimentação fica visível no histórico

#### Scenario: Ajuste inválido

- **WHEN** o operador tenta retirar mais peças que o saldo do SKU
- **THEN** o sistema recusa a operação e mantém o saldo anterior

### Requirement: Etiqueta legível por máquina

O sistema SHALL codificar o código interno de cada variação em barras Code 39 e exibir o mesmo texto legível abaixo delas.

#### Scenario: Impressão de uma variação

- **WHEN** o operador escolhe uma variação e imprime
- **THEN** a etiqueta contém nome, cor, tamanho, preço e barras que representam o código mostrado

### Requirement: Carrinho limitado pelo estoque

O sistema SHALL impedir a adição de mais unidades de um SKU do que o saldo disponível.

#### Scenario: Última unidade

- **WHEN** uma variação tem uma unidade disponível e já está no carrinho
- **THEN** uma nova tentativa de adicioná-la não aumenta a quantidade do carrinho

### Requirement: Indicadores honestos

O sistema SHALL exibir no painel apenas agregações dos registros locais, com indicação de que a base inicial é de demonstração.

#### Scenario: Primeira abertura

- **WHEN** a loja abre o protótipo sem dados salvos
- **THEN** o painel informa que os dados iniciais são de demonstração e não mostra comparações inventadas
