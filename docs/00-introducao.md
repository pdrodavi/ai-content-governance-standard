# 00 — Introdução

## 1. Contexto Geral

A adoção de sistemas de Inteligência Artificial generativa cresceu de forma acelerada nos últimos anos, impulsionada por avanços em modelos de linguagem de grande escala (LLMs) e pela redução da barreira técnica para sua integração em produtos e serviços.

No entanto, esse crescimento ocorreu de maneira **assimétrica**:  
a capacidade técnica de gerar conteúdo evoluiu mais rápido do que os **mecanismos de governança, controle e responsabilização**.

Na prática, muitas organizações passaram a operar sistemas de IA generativa:

- sem separação clara entre geração e decisão  
- sem modelos formais de risco legal  
- sem capacidade de auditoria ex post  
- sem critérios técnicos verificáveis de diligência  

Essa lacuna não é teórica. Ela se manifesta em **incidentes reais**, sanções administrativas, bloqueios regulatórios e crises reputacionais.

Este padrão nasce exatamente desse contexto.

---

## 2. O Problema Estrutural da Governança em IA Generativa

A maioria das abordagens atuais de “governança de IA” sofre de três falhas estruturais recorrentes:

### 2.1 Governança baseada em intenção

Muitos sistemas partem da premissa implícita de que o usuário:
- declarará sua idade corretamente,
- explicitará sua intenção real,
- e utilizará o sistema de boa-fé.

Do ponto de vista jurídico e de engenharia, essa premissa é **inaceitável**.

Sistemas robustos não confiam em intenção declarada; eles operam sob **incerteza adversarial**.

---

### 2.2 Delegação normativa ao modelo

Outra falha comum é permitir que o próprio LLM:
- interprete permissões legais,
- decida se algo é “adequado”,
- ou classifique risco jurídico em tempo real.

Modelos de linguagem são **probabilísticos** por natureza.  
Eles não oferecem garantias de consistência, rastreabilidade ou repetibilidade — requisitos mínimos para decisões normativas.

Delegar decisões jurídicas a um LLM equivale a **internalizar risco regulatório no componente menos confiável do sistema**.

---

### 2.3 Governança reativa e documental

Por fim, muitas organizações tratam governança como:
- política escrita,
- termo de uso,
- ou guideline interno.

Esses artefatos podem ter valor declaratório, mas **não produzem controle técnico**.

Reguladores, auditores e tribunais não avaliam intenções — avaliam **mecanismos implementados**.

---

## 3. Governança como Problema de Engenharia

Este padrão parte de uma premissa central:

> Governança de IA generativa é um problema de **arquitetura e engenharia de sistemas**, não de moral, intenção ou bom senso.

Isso implica tratar governança como:

- componentes dedicados,
- fluxos determinísticos,
- regras executáveis,
- decisões versionadas,
- logs reconstruíveis.

Em outras palavras:  
**governança deve ser codificada, testável e auditável**.

---

## 4. Separação entre Geração e Decisão

Um dos pilares deste padrão é a separação explícita entre:

- **decisão normativa**  
- **geração probabilística**

A decisão normativa responde perguntas como:
- este conteúdo pode ser entregue?
- há restrição legal ou regulatória?
- o risco é aceitável?

A geração probabilística responde apenas:
- como formular a resposta dentro dos limites permitidos?

Essa separação não é opcional.  
Ela é condição necessária para qualquer sistema que pretenda operar de forma defensável em ambientes regulados.

---

## 5. Responsabilidade Objetiva do Operador

Do ponto de vista jurídico, especialmente em legislações como:

- Brasil (CDC, ECA, LGPD)
- União Europeia (GDPR, AI Act)
- Estados Unidos (FTC, COPPA)

o operador do sistema mantém **responsabilidade objetiva** sobre a entrega de conteúdo, independentemente de:

- intenção do usuário,
- imprevisibilidade do modelo,
- ou complexidade técnica.

Este padrão assume essa responsabilidade como **dado de projeto**, não como risco residual ignorável.

---

## 6. Objetivo Deste Documento

O objetivo deste documento não é:

- ensinar como usar LLMs,
- definir boas práticas genéricas,
- ou fornecer recomendações abstratas.

O objetivo é:

- definir **controles técnicos mínimos** de governança,
- fornecer uma **linguagem comum** entre engenharia, jurídico e compliance,
- criar um **framework auditável**, reutilizável e extensível.

---

## 7. Estrutura do Padrão

Os capítulos seguintes aprofundam, de forma progressiva:

- o problema jurídico formal
- o threat model legal
- as estratégias de mitigação adotadas
- a arquitetura de governança proposta
- a posição explícita do LLM no sistema
- os fluxos operacionais
- os contratos técnicos (OpenAPI)
- as políticas executáveis (OPA/Rego)
- os mecanismos de auditoria
- os procedimentos de resposta a incidentes

Cada capítulo foi escrito para ser:
- lido isoladamente,
- implementado tecnicamente,
- auditado por terceiros.

---

## 8. Leitura Esperada

Este não é um documento de leitura leve.

Ele assume familiaridade básica com:
- arquitetura de sistemas
- APIs
- conceitos regulatórios
- noções de risco jurídico

A densidade é **intencional**.  
Governança séria não se comunica por slogans.

---

## 9. Considerações Finais da Introdução

A pergunta que este padrão responde não é:
> “É possível usar IA generativa com responsabilidade?”

A pergunta real é:
> **“Quais mecanismos técnicos tornam o uso de IA generativa juridicamente defensável?”**

Os próximos capítulos tratam dessa resposta em detalhes.

---
