# ABASTECE — Stack Tecnológica

## Objetivo

Definir a stack inicial do ABASTECE priorizando:

- baixo custo;
- velocidade de desenvolvimento;
- facilidade de manutenção;
- integração com ferramentas de inteligência artificial;
- segurança;
- possibilidade de escala.

---

# 1. Frontend

## Next.js

Será utilizado como framework principal da aplicação.

Motivos:

- arquitetura moderna;
- suporte a aplicações web;
- possibilidade de frontend e backend no mesmo projeto;
- bom ecossistema;
- facilidade de deploy;
- integração com TypeScript.

---

# 2. Linguagem

## TypeScript

Será utilizada como linguagem principal.

Objetivos:

- maior segurança durante o desenvolvimento;
- redução de erros;
- melhor manutenção;
- melhor integração com ferramentas de IA.

---

# 3. Interface

## Tailwind CSS

Será utilizado para construção da interface.

Objetivos:

- desenvolvimento rápido;
- responsividade;
- padronização;
- componentes reutilizáveis.

---

# 4. Backend

## Next.js

O backend inicial será implementado dentro da própria aplicação Next.js.

Responsabilidades:

- regras de negócio;
- APIs;
- autenticação;
- comunicação com banco;
- integração com serviços externos.

Um backend separado poderá ser criado futuramente caso a escala do projeto justifique.

---

# 5. Banco de dados

## PostgreSQL

O banco relacional será PostgreSQL.

A primeira opção de infraestrutura será:

## Supabase

Motivos:

- PostgreSQL;
- autenticação;
- APIs;
- armazenamento;
- facilidade de configuração;
- baixo custo inicial;
- possibilidade de evolução.

A escolha definitiva deverá ser validada durante a implementação.

---

# 6. Autenticação

## Supabase Auth

Inicialmente será avaliado o uso do sistema de autenticação do Supabase.

Possibilidades:

- e-mail e senha;
- recuperação de senha;
- autenticação social futuramente.

---

# 7. Inteligência artificial

## Google Gemini

O Gemini será utilizado inicialmente para experimentação dos recursos de IA.

Possíveis aplicações:

- busca inteligente;
- recomendação;
- análise de preços;
- identificação de oportunidades;
- geração de insights.

Os recursos de IA deverão ser implementados de forma modular para permitir troca futura do provedor.

---

# 8. Versionamento

## GitHub

O GitHub será utilizado como repositório central do código e da documentação.

Todo código deverá ser versionado.

---

# 9. Desenvolvimento

Ferramentas planejadas:

- Visual Studio Code
- ChatGPT/Codex
- Claude
- Google AI Studio
- GitHub

---

# 10. Deploy

## Vercel

A primeira opção para hospedagem da aplicação será Vercel.

Motivos:

- integração com Next.js;
- facilidade de deploy;
- integração com GitHub;
- baixo custo inicial;
- possibilidade de escala.

A escolha definitiva será validada antes do primeiro deploy.

---

# 11. Arquitetura inicial

```text
                 ABASTECE
                    |
              ┌─────┴─────┐
              | Next.js   |
              | TypeScript|
              └─────┬─────┘
                    |
          ┌─────────┼─────────┐
          |         |         |
       Frontend   Backend     IA
          |         |         |
          |         |      Gemini
          |         |
          └────┬────┘
               |
           PostgreSQL
               |
            Supabase
               |
            GitHub
               |
            Vercel
