# 04 — Threat Model Legal

## 1. Objetivo do Threat Model

Este capítulo descreve o **modelo formal de ameaças jurídicas** associado à operação de sistemas de IA generativa.

Diferentemente de threat models de segurança, aqui o foco é:
- responsabilidade
- sanção
- obrigação regulatória
- risco institucional

---

## 2. Ativos Protegidos

Os ativos centrais protegidos por este padrão são:

- direitos fundamentais de usuários
- integridade institucional do operador
- conformidade regulatória
- capacidade de defesa jurídica ex post

---

## 3. Agentes de Ameaça

### 3.1 Usuário Malicioso
- explora ambiguidade normativa
- falseia contexto ou idade
- busca forçar saída proibida

### 3.2 Usuário Legítimo
- não intencionalmente causa exposição
- interage de boa-fé, mas gera risco

### 3.3 Falha Sistêmica
- decisões inconsistentes
- drift de política
- mudanças não versionadas

### 3.4 Regulador / Auditor
- solicita prova de diligência
- avalia mecanismos, não intenção

---

## 4. Vetores de Ameaça

- ausência de classificação prévia
- decisões dentro do LLM
- regras implícitas
- falta de logs
- políticas não versionadas

---

## 5. Ameaças Evitadas por Design

Este padrão **explicitamente evita**:

- exposição de menores
- decisões não auditáveis
- dependência de intenção declarada
- impossibilidade de reconstrução histórica
- risco jurídico não mensurado

---

## 6. Risco Residual

Nenhum sistema elimina risco totalmente.

Este padrão:
- reduz risco estrutural
- torna risco residual explícito
- permite aceitação consciente e documentada

---
