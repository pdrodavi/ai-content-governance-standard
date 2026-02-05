# 01 — Escopo e Objetivos do Padrão

## 1. Finalidade do Capítulo

Este capítulo define **com precisão normativa**:

- o que este padrão **cobre**
- o que este padrão **não cobre**
- quais são seus **objetivos explícitos**
- quais interpretações são **explicitamente rejeitadas**

Essa delimitação não é apenas editorial.  
Ela é fundamental para **auditoria, aplicação prática e defesa jurídica**.

Um padrão que “vale para tudo” não vale para nada.

---

## 2. Escopo de Aplicação

### 2.1 Sistemas Abrangidos

Este padrão se aplica a **qualquer sistema** que atenda simultaneamente às seguintes condições:

- utilize **IA generativa** (texto, imagem, áudio, vídeo ou multimodal);
- entregue conteúdo **diretamente a usuários humanos**;
- opere em contextos com **potencial risco legal, regulatório ou reputacional**;
- seja controlado, operado ou ofertado por uma entidade identificável.

Isso inclui, mas não se limita a:

- assistentes conversacionais (chatbots, copilotos);
- sistemas de suporte à decisão com saída textual;
- plataformas de criação de conteúdo assistidas por IA;
- sistemas educacionais baseados em LLMs;
- produtos B2B que gerem conteúdo para usuários finais.

---

### 2.2 Sistemas Explicitamente Fora do Escopo

Este padrão **não se aplica** a:

- sistemas puramente internos, sem entrega de conteúdo a usuários finais;
- pipelines de treinamento offline sem interação humana direta;
- mecanismos de busca tradicionais sem geração de conteúdo novo;
- ferramentas de análise que não produzem saída interpretável por humanos;
- sistemas experimentais isolados de ambientes produtivos.

A exclusão desses casos não é técnica, mas **regulatória**:  
o risco jurídico nesses cenários é qualitativamente distinto.

---

## 3. Escopo Funcional

O padrão incide especificamente sobre as seguintes funções do sistema:

- **tomada de decisão normativa** sobre entrega de conteúdo;
- **classificação de risco legal** antes da geração;
- **orquestração entre políticas e LLMs**;
- **registro e auditoria das decisões**;
- **resposta a incidentes regulatórios**.

O padrão **não** define:
- como o conteúdo deve ser redigido,
- quais modelos devem ser usados,
- como treinar LLMs,
- nem como otimizar performance ou custo.

Essas decisões pertencem à engenharia de produto, não à governança.

---

## 4. Premissas Normativas Fundamentais

Este padrão é construído sobre premissas **não negociáveis**.

### 4.1 Incerteza como Estado Padrão

O sistema **DEVE assumir** que:

- idade do usuário é desconhecida;
- identidade real é desconhecida;
- intenção declarada não é confiável;
- contexto fornecido pode ser falso ou incompleto.

Qualquer arquitetura que dependa da veracidade dessas informações
incorre em **falha estrutural de governança**.

---

### 4.2 Responsabilidade Objetiva do Operador

Independentemente de:
- termos de uso,
- avisos,
- disclaimers,
- ou autodeclarações do usuário,

o **operador do sistema** mantém responsabilidade objetiva sobre a entrega do conteúdo.

Este padrão parte dessa responsabilidade como **fato jurídico dado**, não como hipótese.

---

### 4.3 Separação Obrigatória entre Decisão e Geração

O sistema **DEVE separar** de forma inequívoca:

- componentes que **decidem permissões** (determinísticos);
- componentes que **geram conteúdo** (probabilísticos).

A violação dessa separação constitui:
- falha técnica grave;
- risco regulatório elevado;
- e inviabilidade de auditoria consistente.

---

## 5. Objetivos Primários do Padrão

Os objetivos deste padrão são **operacionais**, não abstratos.

### 5.1 Redução de Risco Jurídico e Regulatório

Criar mecanismos técnicos que:
- reduzam exposição a sanções;
- permitam defesa baseada em diligência comprovável;
- evitem decisões arbitrárias ou inconsistentes.

---

### 5.2 Proteção de Públicos Vulneráveis

Especialmente:
- menores de idade;
- usuários em situação de hipervulnerabilidade;
- contextos legalmente sensíveis.

Essa proteção é implementada por **arquitetura**, não por confiança.

---

### 5.3 Auditabilidade Ex Post

Permitir que qualquer decisão possa ser reconstruída posteriormente, incluindo:

- qual política estava vigente;
- qual regra foi aplicada;
- qual foi a decisão tomada;
- em que data e sob qual versão.

---

### 5.4 Escalabilidade com Governança

Viabilizar que sistemas de IA cresçam em escala sem que o risco cresça de forma descontrolada.

Governança, neste padrão, **não bloqueia escala** — ela a viabiliza.

---

## 6. Objetivos Explicitamente Fora do Escopo

Este padrão **não tem** como objetivo:

- eliminar todo risco possível;
- garantir correção semântica perfeita;
- substituir aconselhamento jurídico humano;
- atender todas as jurisdições possíveis de forma automática;
- decidir o que é “eticamente correto” em sentido filosófico.

Ele busca **redução estruturada de risco**, não eliminação absoluta.

---

## 7. Critérios de Sucesso do Padrão

A adoção deste padrão é considerada bem-sucedida quando:

- decisões normativas não dependem do LLM;
- regras de política são executáveis e versionadas;
- logs permitem reconstrução completa de decisões;
- auditores conseguem validar o funcionamento sem acesso ao código-fonte do modelo;
- reguladores conseguem entender o fluxo decisório sem interpretação subjetiva.

---

## 8. Consequências da Não Adoção

A não adoção dos princípios aqui definidos expõe o operador a:

- decisões normativas não rastreáveis;
- dificuldade de defesa regulatória;
- risco de sanções administrativas;
- bloqueios de produto por órgãos reguladores;
- perda de confiança institucional.

Essas consequências não são hipotéticas.

---

## 9. Considerações Finais sobre Escopo e Objetivos

Este capítulo fixa os **limites do padrão**.

Qualquer implementação que:
- expanda além do escopo,
- ou reduza suas premissas,

deve fazê-lo de forma **explícita e documentada**.

Governança robusta começa pela clareza sobre **o que se está fazendo** —
e, principalmente, sobre **o que não se está fazendo**.

---
