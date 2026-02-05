
---

# 📄 11-opa-rego-politicas-executaveis.md

```markdown
# 11 — OPA / Rego: Políticas Executáveis

## 1. Objetivo do Capítulo

Este capítulo descreve como regras normativas são expressas de forma **executável e verificável** usando OPA / Rego.

Texto sem execução **não constitui política**.

---

## 2. Princípios das Políticas

Políticas DEVEM ser:
- explícitas;
- determinísticas;
- versionadas;
- independentes do LLM.

---

## 3. Exemplo de Política Rego

```rego
package governanca.conteudo

default decisao = "PERMITIR"

decisao = "BLOQUEAR" {
  input.dominio == "proibido_por_lei"
}

decisao = "LIMITAR" {
  input.dominio == "sensivel"
  input.riscoLegal >= 0.6
}
