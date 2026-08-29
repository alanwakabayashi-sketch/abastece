# ABASTECE — Modelo Inicial do Banco de Dados

## 1. Objetivo

Definir a estrutura lógica inicial dos dados utilizados pelo ABASTECE.

Este documento representa o modelo conceitual do banco de dados do MVP.

A tecnologia definitiva do banco poderá ser definida posteriormente.

---

# 2. Entidades principais

O MVP terá inicialmente as seguintes entidades:

- Usuários
- Empresas
- Fornecedores
- Categorias
- Produtos
- Preços
- Oportunidades
- Favoritos
- Planos
- Assinaturas

---

# 3. Usuários

## users

Representa as pessoas que utilizam a plataforma.

### Campos

- id
- name
- email
- password_hash
- company_id
- role
- created_at
- updated_at

### Regras

Cada usuário deverá estar associado a uma empresa.

Um usuário poderá possuir diferentes níveis de permissão futuramente.

---

# 4. Empresas

## companies

Representa o negócio que utiliza o ABASTECE.

### Campos

- id
- name
- segment
- city
- state
- created_at
- updated_at

### Exemplos de segmentos

- restaurante
- bar
- lanchonete
- cafeteria
- hotel
- confeitaria
- food_truck
- outros

---

# 5. Fornecedores

## suppliers

Representa empresas ou profissionais que fornecem produtos.

### Campos

- id
- name
- description
- city
- state
- phone
- email
- website
- accepts_cnpj
- accepts_cpf
- status
- created_at
- updated_at

### Regras

Um fornecedor poderá oferecer diversos produtos.

Um fornecedor poderá atender CNPJ, CPF ou ambos.

---

# 6. Categorias

## categories

Organiza produtos por grupos.

### Campos

- id
- name
- description
- created_at
- updated_at

### Exemplos

- carnes
- aves
- pescados
- hortifruti
- laticínios
- secos
- bebidas
- embalagens
- limpeza
- outros

---

# 7. Produtos

## products

Representa os produtos disponíveis na plataforma.

### Campos

- id
- name
- description
- category_id
- unit
- created_at
- updated_at

### Exemplos de unidade

- kg
- g
- unidade
- caixa
- pacote
- litro
- ml

---

# 8. Produtos dos fornecedores

## supplier_products

Relaciona fornecedores aos produtos que comercializam.

### Campos

- id
- supplier_id
- product_id
- sku
- minimum_quantity
- availability
- notes
- created_at
- updated_at

### Regra

Um produto poderá ser comercializado por vários fornecedores.

Um fornecedor poderá comercializar vários produtos.

---

# 9. Preços

## prices

Registra o preço de um produto oferecido por determinado fornecedor.

### Campos

- id
- supplier_product_id
- price
- previous_price
- currency
- valid_from
- valid_until
- created_at
- updated_at

### Objetivo

Permitir futuramente:

- comparação de preços;
- histórico;
- identificação de redução de preço;
- identificação de oportunidades.

---

# 10. Oportunidades

## opportunities

Representa oportunidades identificadas na plataforma.

### Campos

- id
- supplier_product_id
- title
- description
- previous_price
- current_price
- discount_percentage
- valid_until
- status
- created_at
- updated_at

### Tipos possíveis

- promoção
- redução de preço
- condição especial
- oportunidade de economia

---

# 11. Favoritos

## favorites

Registra itens salvos pelos usuários.

### Campos

- id
- user_id
- entity_type
- entity_id
- created_at

### Tipos

- product
- supplier
- opportunity

---

# 12. Planos

## plans

Representa os planos comerciais do ABASTECE.

### Campos

- id
- name
- price
- description
- status
- created_at
- updated_at

### Planos iniciais

START

R$ 9,90/mês

PRO

R$ 19,90/mês

BUSINESS

R$ 39,90/mês

CONSULT

R$ 99,90/mês

---

# 13. Assinaturas

## subscriptions

Representa a assinatura de uma empresa.

### Campos

- id
- company_id
- plan_id
- status
- started_at
- expires_at
- created_at
- updated_at

### Status possíveis

- active
- canceled
- expired
- pending

---

# 14. Relacionamentos

## Usuário → Empresa

Uma empresa poderá possuir vários usuários.

```text
Company
   |
   +---- User
   +---- User
   +---- User
