# ABASTECE — Protocolo de Trabalho das IAs

## 1. Objetivo

Definir como ferramentas de inteligência artificial deverão trabalhar no projeto ABASTECE.

As IAs deverão atuar como ferramentas complementares de desenvolvimento, revisão, pesquisa e experimentação.

---

# 2. Fonte de verdade

Antes de executar qualquer tarefa importante, a IA deverá considerar como fonte principal:

1. CONTEXT.md
2. documentação em /docs
3. código existente
4. decisões registradas no GitHub

A IA não deverá assumir que uma informação não documentada é verdadeira.

---

# 3. Hierarquia de trabalho

## ChatGPT

Função:

Arquitetura, produto e coordenação.

Responsabilidades:

- planejamento;
- arquitetura;
- requisitos;
- documentação;
- análise de decisões;
- definição de tarefas;
- revisão estratégica.

---

## Codex

Função:

Implementação técnica.

Responsabilidades:

- escrever código;
- modificar código;
- criar componentes;
- corrigir bugs;
- executar testes;
- refatorar;
- implementar funcionalidades.

---

## Claude

Função:

Revisão técnica e segunda opinião.

Responsabilidades:

- revisar código;
- encontrar bugs;
- identificar riscos;
- avaliar arquitetura;
- sugerir melhorias;
- revisar segurança;
- avaliar qualidade do código.

---

## Google AI Studio / Gemini

Função:

Laboratório de inteligência artificial.

Responsabilidades:

- experimentar prompts;
- testar modelos;
- desenvolver recursos de IA;
- avaliar respostas;
- testar APIs Gemini;
- prototipar funcionalidades inteligentes.

---

# 4. Fluxo de trabalho

O fluxo padrão deverá ser:

```text
IDEIA
 ↓
REQUISITO
 ↓
CHATGPT
 ↓
PLANEJAMENTO
 ↓
CODEX
 ↓
IMPLEMENTAÇÃO
 ↓
TESTES
 ↓
CLAUDE
 ↓
REVISÃO
 ↓
CORREÇÕES
 ↓
GITHUB
 ↓
DOCUMENTAÇÃO
