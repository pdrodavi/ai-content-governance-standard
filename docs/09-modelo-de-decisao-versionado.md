# 09 — Modelo de Decisão Versionado

## 1. Objetivo do Capítulo

Este capítulo define como **decisões normativas são versionadas, identificadas e reconstruídas** ao longo do tempo.

Sem versionamento explícito, não existe:
- auditoria válida,
- defesa regulatória,
- nem aprendizagem institucional.

---

## 2. Decisão como Artefato Técnico

Neste padrão, uma decisão normativa é tratada como um **artefato técnico**, não como efeito colateral da execução.

Cada decisão DEVE produzir um registro contendo:
- identificação única;
- versão da política aplicada;
- hash da política;
- data de vigência;
- resultado da decisão.

---

## 3. Componentes Obrigatórios da Decisão

### 3.1 Identificador da Decisão

Cada decisão DEVE possuir um identificador único e rastreável, associado à requisição que a originou.

---

### 3.2 policyVersion

Identifica a versão semântica da política no momento da decisão.

Permite reconstrução histórica mesmo após mudanças futuras.

---

### 3.3 policyHash

Hash criptográfico do conteúdo da política aplicada.

Garante integridade e prova de não adulteração ex post.

---

### 3.4 effectiveDate

Data e hora de vigência da política no momento da decisão.

Evita ambiguidades em transições de versão.

---

## 4. Imutabilidade do Registro

Após persistida, a decisão:
- NÃO DEVE ser alterada;
- NÃO DEVE ser reprocessada retroativamente;
- PODE ser contextualizada por registros adicionais.

---

## 5. Reconstrução Ex Post

Com os dados versionados, torna-se possível responder:

- qual política estava ativa?
- qual regra foi aplicada?
- por que a saída foi bloqueada ou permitida?

Essa capacidade é central para defesa jurídica.

---
