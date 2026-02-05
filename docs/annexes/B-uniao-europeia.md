# Anexo B — União Europeia

## 1. Finalidade do Anexo

Este anexo demonstra o alinhamento do padrão com o **marco regulatório europeu**, em especial o GDPR e o AI Act.

---

## 2. GDPR (Regulamento Geral de Proteção de Dados)

### 2.1 Accountability

O GDPR exige que o controlador **demonstre conformidade**, não apenas a alegue.

O padrão responde a isso por meio de:
- logs reconstruíveis;
- decisões versionadas;
- políticas explícitas.

---

### 2.2 Proteção de Menores

O GDPR impõe tratamento reforçado para dados de crianças.

A arquitetura proposta:
- evita depender de idade declarada;
- minimiza processamento adicional de dados;
- privilegia prevenção por design.

---

## 3. AI Act

### 3.1 Abordagem Baseada em Risco

O AI Act classifica sistemas conforme risco.

Sistemas de IA generativa com entrega direta de conteúdo podem se enquadrar como **alto risco**, dependendo do contexto.

---

### 3.2 Requisitos Técnicos Relevantes

Entre os requisitos:
- gestão de risco contínua;
- documentação técnica;
- governança humana e técnica.

O padrão atende a esses pontos com:
- threat model legal;
- policy-as-code;
- separação entre decisão e geração.

---

## 4. Síntese Jurídica (UE)

O padrão oferece uma **implementação prática** da abordagem baseada em risco exigida pelo AI Act, sem depender de avaliações subjetivas do modelo.

---
