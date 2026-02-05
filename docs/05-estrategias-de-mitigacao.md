# 05 — Estratégias de Mitigação

## 1. Visão Geral

As estratégias adotadas neste padrão não são genéricas; elas são **respostas diretas ao threat model jurídico**.

Cada estratégia corresponde a uma falha estrutural identificada.

---

## 2. Bloqueio Absoluto por Categoria Legal

Conteúdos proibidos por lei **DEVEM ser bloqueados**, independentemente de contexto ou intenção.

Não há mitigação progressiva nesses casos.

---

## 3. Rebaixamento Progressivo de Capacidade

Quando o risco é contextual ou graduado:
- o sistema **LIMITA**, não bloqueia completamente;
- reduz detalhamento, precisão ou operacionalidade.

---

## 4. Policy-as-Code

Toda regra normativa:
- DEVE ser codificada
- versionada
- executável

Texto sem código **não constitui governança**.

---

## 5. Threat Modeling Contínuo

O threat model **DEVE ser revisado**:
- periodicamente
- após incidentes
- após mudanças de produto

Governança é processo contínuo, não estado final.

---
