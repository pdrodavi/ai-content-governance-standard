# Checklist de Auditoria Externa

## 1. Finalidade do Checklist

Este checklist permite que **auditores independentes** avaliem a conformidade do sistema com o padrão, sem necessidade de acesso ao código-fonte do LLM.

---

## 2. Governança Geral

- [ ] Existe motor de decisão normativa externo ao LLM
- [ ] O LLM não executa decisões jurídicas
- [ ] Há separação explícita entre decisão e geração

---

## 3. Políticas e Regras

- [ ] Políticas estão codificadas (policy-as-code)
- [ ] Políticas possuem versionamento semântico
- [ ] Políticas possuem hash verificável
- [ ] Políticas têm data de vigência explícita

---

## 4. Fluxo Operacional

- [ ] Classificação ocorre antes da geração
- [ ] Avaliação de risco precede decisão
- [ ] Há apenas três saídas possíveis (PERMITIR, LIMITAR, BLOQUEAR)
- [ ] Fluxos são documentados e reproduzíveis

---

## 5. Logs e Evidências

- [ ] Logs são estruturados
- [ ] Logs são imutáveis
- [ ] Logs incluem policyVersion e policyHash
- [ ] Logs permitem reconstrução ex post

---

## 6. Compliance Regulatória

- [ ] Existe AIA/DPIA documentado
- [ ] Anexos por jurisdição estão atualizados
- [ ] Há processo formal de revisão de risco

---

## 7. Conclusão de Auditoria

A conformidade só pode ser declarada quando TODOS os itens aplicáveis estiverem atendidos.

Governança parcial **não constitui conformidade**.

---
