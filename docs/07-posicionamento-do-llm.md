# 07 — Posicionamento do LLM no Sistema

## 1. Objetivo do Capítulo

Este capítulo fixa, de forma inequívoca, o **papel do LLM** dentro da arquitetura.

Ele existe para evitar a ambiguidade comum:
> “O modelo decidiu errado.”

No padrão, o modelo **não decide**.

---

## 2. Natureza Probabilística dos LLMs

Modelos de linguagem:
- operam por probabilidade;
- não garantem consistência;
- não garantem rastreabilidade.

Essas características os tornam **inaptos para decisões normativas**.

---

## 3. Funções Permitidas ao LLM

O LLM PODE:
- redigir texto;
- reformular respostas;
- explicar conceitos dentro de limites impostos.

O LLM NÃO PODE:
- avaliar legalidade;
- classificar permissibilidade;
- assumir critérios normativos.

---

## 4. Relação Hierárquica com a Governança

Arquiteturalmente:
- o LLM está **abaixo** da política;
- recebe apenas contexto autorizado;
- não conhece regras completas de decisão.

Isso reduz superfície de risco.

---

## 5. Consequências da Violação

Permitir que o LLM decida implica:
- impossibilidade de auditoria;
- risco jurídico extremo;
- colapso da defesa regulatória.

Essa violação invalida a conformidade com o padrão.

---
