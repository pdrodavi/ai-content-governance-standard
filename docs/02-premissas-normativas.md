# 02 — Premissas Normativas

## 1. Objetivo do Capítulo

Este capítulo estabelece as **premissas normativas fundamentais** sobre as quais todo o padrão é construído.  
Essas premissas **não são sugestões**: são pressupostos obrigatórios para validade técnica, jurídica e operacional do framework.

Qualquer implementação que viole essas premissas **deixa de estar em conformidade** com o padrão.

---

## 2. Linguagem Normativa

Ao longo deste documento, os termos abaixo são utilizados com significado normativo explícito:

- **DEVE**: requisito obrigatório
- **NÃO DEVE**: requisito proibido
- **PODE**: comportamento opcional
- **NÃO DEVERIA**: prática fortemente desencorajada

Essa convenção segue padrões internacionais de especificações técnicas (RFC/ISO).

---

## 3. Premissa da Incerteza Total do Usuário

### 3.1 Incerteza de Identidade

O sistema **DEVE assumir** que não conhece a identidade real do usuário.

Credenciais técnicas (login, conta, token) **não equivalem** a identidade jurídica verificada.

---

### 3.2 Incerteza de Idade

O sistema **DEVE assumir** que a idade do usuário é desconhecida ou potencialmente incorreta, mesmo quando declarada.

Autodeclaração **não constitui controle técnico válido**.

---

### 3.3 Incerteza de Intenção

O sistema **NÃO DEVE** inferir legalidade com base na intenção declarada pelo usuário.

Intenção é:
- subjetiva
- facilmente manipulável
- juridicamente irrelevante para fins de dever de cuidado técnico

---

## 4. Premissa da Responsabilidade Objetiva

O operador do sistema **DEVE assumir responsabilidade objetiva** pelas decisões de entrega de conteúdo.

Essa responsabilidade:
- não é transferível ao usuário
- não é mitigada por disclaimers
- não é absorvida pelo fornecedor do modelo

---

## 5. Premissa da Não-Delegação Normativa ao LLM

Modelos de linguagem são **probabilísticos**, não determinísticos.

O sistema **NÃO DEVE** permitir que o LLM:
- interprete leis
- decida permissões
- avalie risco jurídico
- determine elegibilidade de conteúdo

Essa proibição é absoluta dentro do escopo do padrão.

---

## 6. Premissa da Deterministicidade da Governança

Toda decisão normativa **DEVE ser**:
- reproduzível
- rastreável
- versionada
- auditável ex post

Isso exige motores externos ao LLM, com regras explícitas.

---

## 7. Falhas Estruturais Decorrentes da Violação das Premissas

A violação de qualquer premissa deste capítulo implica:

- risco jurídico elevado
- impossibilidade de auditoria confiável
- fragilidade regulatória
- exposição reputacional sistêmica

Não se trata de risco teórico, mas estrutural.

---
