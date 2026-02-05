# 10 — OpenAPI de Decisão de Política

## 1. Objetivo do Capítulo

Este capítulo define o **contrato técnico público** para o serviço de decisão normativa.

A OpenAPI é a fronteira explícita entre:
- lógica de governança
- e o restante do sistema.

---

## 2. Princípios do Contrato

A API de decisão DEVE ser:
- simples;
- determinística;
- estável;
- independente de implementação interna.

Ela NÃO DEVE:
- expor lógica interna sensível;
- depender de contexto implícito;
- assumir estado fora da requisição.

---

## 3. Especificação OpenAPI (Exemplo Normativo)

```yaml
openapi: 3.0.3
info:
  title: API de Decisão Normativa
  version: "1.0.0"

paths:
  /policy/decidir:
    post:
      summary: Decide permissibilidade de entrega de conteúdo
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/PolicyRequest'
      responses:
        '200':
          description: Decisão aplicada
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/PolicyDecision'

components:
  schemas:
    PolicyRequest:
      type: object
      required:
        - dominio
        - riscoLegal
      properties:
        dominio:
          type: string
        riscoLegal:
          type: number
        jurisdicao:
          type: string

    PolicyDecision:
      type: object
      required:
        - decisao
        - policyVersion
        - policyHash
        - effectiveDate
      properties:
        decisao:
          type: string
          enum: [PERMITIR, LIMITAR, BLOQUEAR]
        policyVersion:
          type: string
        policyHash:
          type: string
        effectiveDate:
          type: string
