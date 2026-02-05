# AI Impact Assessment (AIA) / Data Protection Impact Assessment (DPIA)

## 1. Finalidade do Documento

Este documento constitui uma **Avaliação Completa de Impacto de IA (AIA)**, alinhada aos requisitos de **DPIA** previstos em legislações como a LGPD e o GDPR.

Seu objetivo é:
- identificar riscos a direitos fundamentais;
- avaliar impactos potenciais do sistema;
- documentar medidas técnicas de mitigação;
- justificar o risco residual aceito.

---

## 2. Descrição do Sistema Avaliado

O sistema avaliado é um **sistema de IA generativa**, com as seguintes características:

- entrega direta de conteúdo a usuários finais;
- uso de modelos probabilísticos (LLMs);
- operação em ambiente de incerteza de identidade e idade;
- aplicação de decisões normativas prévias à geração.

---

## 3. Contexto de Uso

O sistema pode ser utilizado em múltiplos contextos, incluindo:

- educação assistida por IA;
- suporte informacional;
- criação de conteúdo;
- interação conversacional aberta.

Todos esses contextos envolvem **potencial risco jurídico**, especialmente quando:
- há usuários menores;
- há temas sensíveis;
- há assimetria de informação.

---

## 4. Identificação de Riscos

### 4.1 Riscos aos Direitos Fundamentais

- exposição de menores a conteúdo inadequado;
- fornecimento de informações legalmente restritas;
- impacto psicológico ou educacional negativo;
- violação indireta de normas protetivas.

---

### 4.2 Riscos Reguladores

- sanções administrativas;
- ordens de suspensão de serviço;
- investigações de práticas negligentes;
- imposição de obrigações corretivas.

---

### 4.3 Riscos Operacionais

- decisões inconsistentes;
- ausência de rastreabilidade;
- falha de defesa ex post;
- escalonamento de incidentes.

---

## 5. Medidas de Mitigação Implementadas

As seguintes medidas técnicas são adotadas:

- classificação prévia de domínio e risco;
- motor de políticas determinístico;
- separação clara entre decisão e geração;
- bloqueio absoluto por categoria legal;
- rebaixamento progressivo de capacidade;
- logs imutáveis e versionados.

---

## 6. Avaliação de Proporcionalidade

As medidas adotadas são consideradas proporcionais porque:

- não exigem coleta adicional de dados pessoais sensíveis;
- evitam identificação forçada do usuário;
- priorizam prevenção por arquitetura;
- reduzem impacto sem inviabilizar o sistema.

---

## 7. Risco Residual

Após mitigação, permanecem riscos residuais relacionados a:

- erro de classificação semântica;
- limitação inerente a modelos probabilísticos;
- ambiguidades regulatórias futuras.

Esses riscos são:
- documentados;
- monitorados;
- aceitos de forma consciente pelo operador.

---

## 8. Conclusão do AIA / DPIA

Conclui-se que o sistema, conforme projetado:
- apresenta risco residual aceitável;
- incorpora medidas técnicas razoáveis;
- atende aos princípios de prevenção e responsabilização.

Este AIA/DPIA DEVE ser revisado:
- periodicamente;
- após incidentes;
- após mudanças arquiteturais relevantes.

---
