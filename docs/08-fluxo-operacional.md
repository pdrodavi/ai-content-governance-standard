# 08 — Fluxo Operacional

## 1. Objetivo do Capítulo

Este capítulo descreve o **fluxo operacional completo**, do input do usuário ao registro final.

Ele é o ponto de convergência entre:
- engenharia,
- governança,
- auditoria.

---

## 2. Etapas do Fluxo

O fluxo padrão é composto por:

1. Recepção da requisição
2. Normalização e classificação
3. Avaliação de risco
4. Decisão normativa
5. Geração condicionada
6. Sanitização
7. Registro e auditoria

Nenhuma etapa é opcional.

---

## 3. Ramos de Decisão

A decisão normativa possui apenas três saídas possíveis:

- **BLOQUEAR**
- **LIMITAR**
- **PERMITIR**

Qualquer outro estado é proibido por indefinição.

---

## 4. Fluxo em Caso de Bloqueio

Quando BLOQUEAR:
- nenhum conteúdo é gerado;
- resposta padrão é retornada;
- log é persistido.

---

## 5. Fluxo em Caso de Limitação

Quando LIMITAR:
- escopo da resposta é reduzido;
- capacidade operacional é removida;
- detalhes sensíveis são omitidos.

---

## 6. Fluxo em Caso de Permissão

Quando PERMITIR:
- o LLM recebe contexto autorizado;
- gera resposta;
- saída passa por sanitização final.

---

## 7. Observabilidade

Cada etapa DEVE ser observável e mensurável.

Governança sem observabilidade **não é governança**.

---
