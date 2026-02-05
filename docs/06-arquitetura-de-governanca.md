# 06 — Arquitetura de Governança

## 1. Objetivo do Capítulo

Este capítulo traduz os princípios normativos e jurídicos do padrão em **arquitetura de sistemas concreta**.

Aqui se responde à pergunta central da engenharia:
> Onde exatamente a governança vive no sistema?

Governança, neste padrão, **não é transversal difusa** — ela é um **componente arquitetural explícito**.

---

## 2. Separação de Domínios Funcionais

A arquitetura proposta separa claramente três domínios:

1. **Entrada e Normalização**
2. **Decisão Normativa**
3. **Geração Probabilística**

Essa separação é obrigatória e NÃO DEVE ser colapsada em um único componente.

---

## 3. Camada de Normalização e Classificação

Antes de qualquer decisão normativa, o sistema DEVE:

- normalizar a entrada do usuário;
- classificar domínio temático;
- identificar categorias legalmente sensíveis;
- calcular métricas de risco contextual.

Essa camada NÃO decide permissões — apenas prepara insumos.

---

## 4. Motor de Decisão Normativa

O motor de decisão normativa é o **núcleo da governança**.

Ele DEVE:
- ser determinístico;
- operar com regras explícitas;
- ser auditável;
- estar fora do LLM.

Ele NÃO DEVE:
- gerar conteúdo;
- inferir intenção;
- “interpretar” texto livre sem regras.

---

## 5. Camada de Geração (LLM)

O LLM é tratado como:
- componente subordinado;
- mecanismo de geração condicionado;
- executor dentro de limites impostos.

O LLM **nunca é fonte de decisão normativa**.

---

## 6. Camada de Sanitização e Pós-processamento

Mesmo após geração autorizada, o sistema DEVE:
- validar saída;
- aplicar filtros finais;
- garantir aderência à decisão normativa.

Essa camada protege contra:
- comportamento emergente inesperado;
- regressões de modelo;
- falhas de contexto.

---

## 7. Persistência e Auditoria

Toda decisão normativa DEVE gerar:

- registro estruturado;
- metadados de versão;
- timestamp confiável;
- referência à política aplicada.

Sem isso, **não há governança**.

---
