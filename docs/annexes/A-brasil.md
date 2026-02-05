# Anexo A — Brasil

## 1. Finalidade do Anexo

Este anexo contextualiza o padrão à luz do **ordenamento jurídico brasileiro**, demonstrando como a arquitetura proposta atende, de forma técnica, aos deveres legais existentes.

Não se trata de interpretação criativa da lei, mas de **tradução técnica de obrigações já vigentes**.

---

## 2. Bases Legais Relevantes

As principais normas consideradas são:

- Constituição Federal de 1988  
- Estatuto da Criança e do Adolescente (Lei nº 8.069/1990 – ECA)  
- Código de Defesa do Consumidor (Lei nº 8.078/1990 – CDC)  
- Lei Geral de Proteção de Dados (Lei nº 13.709/2018 – LGPD)  

---

## 3. Estatuto da Criança e do Adolescente (ECA)

### 3.1 Princípio da Proteção Integral

O ECA estabelece a **proteção integral** como princípio estruturante.

Do ponto de vista técnico, isso implica que:
- a dúvida opera em favor do menor;
- a ausência de verificação não autoriza entrega de conteúdo sensível;
- o dever de cuidado é reforçado.

O padrão responde a esse princípio assumindo **incerteza de idade por design**.

---

### 3.2 Dever de Prevenção

O ECA impõe dever de **prevenir exposição** a conteúdos inadequados.

A arquitetura proposta atende a esse dever ao:
- classificar conteúdo previamente;
- bloquear categorias proibidas;
- impedir decisão baseada em autodeclaração.

---

## 4. Código de Defesa do Consumidor (CDC)

### 4.1 Responsabilidade Objetiva

O CDC adota responsabilidade objetiva do fornecedor.

No contexto de IA generativa:
- falhas de modelo não eximem o operador;
- imprevisibilidade técnica não afasta responsabilidade.

O padrão assume essa responsabilidade como premissa.

---

### 4.2 Dever de Segurança

O fornecedor deve garantir segurança razoável do serviço.

Permitir que um LLM decida permissões legais **não atende ao dever de segurança**, pois é inerentemente não determinístico.

---

## 5. Lei Geral de Proteção de Dados (LGPD)

### 5.1 Princípio da Responsabilização

A LGPD exige capacidade de **demonstrar conformidade**.

Logs versionados, políticas executáveis e auditoria ex post atendem diretamente a esse princípio.

---

### 5.2 Proteção de Dados de Crianças e Adolescentes

A LGPD reforça deveres quando há dados de menores.

Ao assumir incerteza de idade, o padrão evita exposição indevida **sem depender de coleta adicional de dados pessoais**.

---

## 6. Síntese Jurídica (Brasil)

No contexto brasileiro, este padrão:
- não cria novas obrigações;
- operacionaliza obrigações já existentes;
- fornece meios técnicos para cumprimento do dever de cuidado.

---
