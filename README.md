# 🎯 Desafio Criativo: Quem Não Vende, Ajuda a Vender! O Poder da Argumentação

### Caderno de Engenharia de Prompt | Desafio Criativo DIO

> **Contexto do desafio:** argumentação de vendas para distribuição da linha **FYS**
> — refrigerantes do Grupo Heineken com até 50% menos açúcar.

---

## 📌 Contexto e Objetivos

### Por que este tema?

O mercado de bebidas é altamente competitivo e os compradores de PDV (ponto de
venda) recebem dezenas de abordagens por semana. Para um distribuidor da linha
**FYS**, argumentar bem significa saber traduzir os diferenciais do produto
(menos açúcar, Grupo Heineken, posicionamento premium) em razões concretas de
compra para donos de bares, restaurantes, mercados e empórios.

A IA generativa permite construir argumentos personalizados por canal e produto
em segundos — este caderno documenta como chegar a um prompt que realmente
funciona no dia a dia comercial.

### Sobre o produto

**FYS** é o refrigerante do Grupo Heineken com até **50% menos açúcar**
comparado à média de mercado. Linha atual:

| Produto | Diferencial |
|---|---|
| Tônica com toque de Limão Siciliano | 45% menos açúcar |
| Tônica com toque de Limão Siciliano **Zero** | Zero açúcar e calorias |
| Refrigerante de Guaraná da Amazônia | 50% menos açúcar |
| Refrigerante de Limão Siciliano | 50% menos açúcar |
| Refrigerante de Laranja-Pera | 50% menos açúcar |

### Objetivos do Desafio

- [ ] Definir com clareza o tipo de argumento de venda desejado
- [ ] Mapear o perfil do comprador e o canal de abordagem
- [ ] Especificar formato, tom e restrições da resposta
- [ ] Testar, refinar e documentar versões do prompt
- [ ] Chegar a um prompt final reutilizável por produto e por canal

---

## 🧩 Construção Passo a Passo

### 🧱 Passo 1 — Defina a intenção
*O que você quer gerar? Para quem? Qual o resultado esperado?*

**Modelo:**
```
Quero que a IA gere [tipo de conteúdo] para [público],
com o objetivo de [resultado esperado].
```

**Minha resposta:**
```
Quero que a IA gere argumentos de venda para compradores de PDV
(donos de bares, restaurantes, empórios e mercados), com o objetivo
de convencê-los a incluir a linha FYS no mix de bebidas do estabelecimento.
```

---

### 🧱 Passo 2 — Adicione contexto e restrições
*Qual estilo? Limite de tamanho? O que evitar?*

**Modelo:**
```
Considere o seguinte contexto: [contexto].
O conteúdo deve ter [formato].
Evite [o que evitar].
```

**Minha resposta:**
```
Considere o seguinte contexto: FYS é um refrigerante premium do Grupo Heineken
com até 50% menos açúcar. Os compradores são donos de estabelecimentos que
já trabalham com marcas Heineken ou buscam produtos diferenciados para um
público mais exigente e consciente. A abordagem é feita via WhatsApp ou visita
presencial. O conteúdo deve ter formato de mensagem curta e direta (máximo
5 linhas), linguagem próxima e profissional. Evite superlativos genéricos
como "o melhor refrigerante do mercado" e promessas não verificáveis.
```

---

### 🧱 Passo 3 — Una tudo no prompt final
*Junte os dois passos em um único comando claro.*

**Modelo:**
```
Quero que a IA gere [tipo de conteúdo] para [público], com o objetivo de
[resultado]. Considere o seguinte contexto: [contexto]. O conteúdo deve ter
[formato]. Evite [o que evitar].
```

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

Registro do processo real de teste — o que funcionou, o que falhou e como
ajustamos.

---

### 🔵 Rodada 1 — Prompt Inicial (Diagnóstico)

**Objetivo:** Testar uma versão simples, só com o nome do produto.

#### Prompt 1.1
```
"Crie um argumento de venda para o refrigerante FYS."
```

**Resposta obtida:** A IA inventou informações — mencionou sabores que não
existem, afirmou que FYS é "natural" (sem base na marca) e usou linguagem de
propaganda genérica.

**⚠️ Dificuldade encontrada:** Sem contexto real, a IA preenche as lacunas com
suposições — perigoso no B2B, onde o comprador percebe imprecisão rapidamente.

**🔧 Ajuste feito:** Fornecer os dados reais do produto (diferenciais, linha,
grupo Heineken) no próprio prompt (ver 1.2).

---

#### Prompt 1.2 (versão refinada)
```
"FYS é um refrigerante do Grupo Heineken com até 50% menos açúcar comparado
à média do mercado. Crie um argumento de venda para um dono de restaurante que
já trabalha com produtos Heineken. Destaque o diferencial de saúde e o
prestígio da marca. Máximo 5 linhas."
```

**Resposta obtida:** Muito mais precisa e ancorada nos fatos reais. Porém,
o tom ficou formal demais para uma abordagem de WhatsApp.

**✅ Lição aprendida:** Dados reais no prompt = resposta confiável. Mas o
**canal de comunicação** ainda precisa ser especificado.

---

### 🟡 Rodada 2 — Ajustando Tom e Canal

**Objetivo:** Calibrar a linguagem para o WhatsApp comercial — próxima, ágil,
sem formalidade de e-mail corporativo.

#### Prompt 2.1
```
"FYS é um refrigerante do Grupo Heineken com até 50% menos açúcar. Escreva
uma mensagem de WhatsApp para um dono de bar que trabalha com produtos
Heineken. Tom: direto, amigável, como um vendedor que já conhece o cliente.
Não use 'prezado' ou 'cordialmente'. Máximo 4 linhas."
```

**Resposta obtida:**

> Oi [nome]! Lembra que a gente falou em agregar algo diferente ao seu cardápio?
> O FYS chegou — refri do Grupo Heineken com até 50% menos açúcar, opção
> premium pra quem curte sabor sem exagero no doce. Posso te mandar os sabores
> disponíveis?

**✅ O que funcionou:** Referenciar a relação prévia com o cliente ("a gente
falou") deixou o texto mais natural. Terminar com uma pergunta aberta gera
resposta do comprador.

---

#### Prompt 2.2 — Variação por canal de venda
```
"Com base nos dados do FYS (refrigerante Heineken, até 50% menos açúcar,
sabores: Guaraná da Amazônia, Limão Siciliano, Laranja-Pera, Tônica e Tônica
Zero), crie um argumento de venda curto (3 linhas) para cada canal abaixo:
- Empório premium
- Restaurante fitness / saudável
- Bar de coquetéis"
```

**Resposta obtida:** Três argumentos com ângulos distintos — exclusividade para
o empório, alinhamento com o estilo de vida para o restaurante fitness, e o
uso da tônica em drinks para o bar.

**✅ Lição aprendida:** Segmentar por canal em um único prompt é muito mais
eficiente do que criar um prompt separado para cada tipo de estabelecimento.

---

### 🔴 Rodada 3 — Troubleshooting (Dificuldades Encontradas)

#### Problema 1: IA inventa informações sobre o produto
**Causa:** Prompt não forneceu dados reais — a IA preencheu com suposições.
**Solução:** Sempre incluir no prompt os dados verificados do produto:
```
"FYS: refrigerante do Grupo Heineken | até 50% menos açúcar comparado à
média de mercado | sabores: Guaraná da Amazônia, Limão Siciliano,
Laranja-Pera, Tônica, Tônica Zero."
```

#### Problema 2: Argumento não se diferencia dos concorrentes
**Causa:** O prompt não pediu diferenciação competitiva explícita.
**Solução:**
```
"Destaque o que torna FYS diferente dos refrigerantes tradicionais: menos
açúcar sem abrir mão do sabor, e o respaldo do Grupo Heineken."
```

#### Problema 3: Mensagem longa demais para o WhatsApp
**Causa:** Sem limitador explícito de linhas.
**Solução:**
```
"Máximo 4 linhas. Uma frase por ideia. Sem listas ou bullet points —
flua como texto de mensagem."
```

#### Problema 4: Tom agressivo ou de pressão de venda
**Causa:** A IA tende a incluir gatilhos de urgência genéricos.
**Solução:**
```
"Evite frases de pressão como 'aproveite agora' ou 'oferta por tempo
limitado'. Prefira um tom consultivo — apresente o produto, não force
a venda."
```

---

## 📖 Prompt Final — Entrega

```
Você é um vendedor experiente do setor de bebidas, representando a linha FYS
do Grupo Heineken.

Dados do produto: FYS é um refrigerante com até 50% menos açúcar comparado
à média de mercado. Linha disponível: Guaraná da Amazônia, Limão Siciliano,
Laranja-Pera, Tônica com Limão Siciliano e Tônica Zero.

Público: [dono de bar / restaurante / empório / mercado] que já trabalha com
produtos premium ou marcas do Grupo Heineken.

Tarefa: Crie uma mensagem de WhatsApp para apresentar a linha FYS e despertar
o interesse do comprador em conhecer os produtos.

Formato: máximo 4-5 linhas, tom direto e amigável como conversa entre
profissionais do setor. Sem saudações formais. Encerre com uma pergunta
aberta para gerar engajamento.

Evite: superlativos sem base real, promessas de vendas exageradas, linguagem
de e-mail corporativo e urgências artificiais.
```

### Exemplos de resposta gerada com o prompt final

**Para bar de coquetéis:**
> Oi [nome]! Você conhece o FYS? É o refrigerante do Grupo Heineken com
> até 50% menos açúcar — a tônica deles tá sendo muito usada em drinks
> mais elaborados. Posso te mandar uma amostra pra experimentar antes de
> decidir?

**Para restaurante fitness:**
> [Nome], tenho uma novidade que combina muito com o perfil do seu restaurante.
> O FYS é um refri do Grupo Heineken com até 50% menos açúcar — sabor de
> verdade pra quem não quer abrir mão da qualidade. Quer ver a linha completa?

**Para empório premium:**
> Oi [nome]! O FYS é o refrigerante do Grupo Heineken que chegou pra ocupar
> o espaço das opções premium no seu mix. Menos açúcar, sabores diferenciados,
> embalagem cuidadosa. Faz sentido pro seu público?

---

## 🔁 Prompts Reutilizáveis — Linha FYS

Coleção de prompts testados para o dia a dia comercial:

#### 📌 Apresentação inicial por canal
```
"Crie uma mensagem de WhatsApp apresentando a linha FYS (refrigerante Heineken,
até 50% menos açúcar) para [tipo de estabelecimento]. Tom amigável,
máximo 4 linhas, encerre com pergunta aberta."
```

#### 📌 Argumento por sabor
```
"Crie um argumento de venda de 3 linhas para o [sabor FYS], destacando o
principal diferencial para um comprador de [tipo de PDV]."
```

#### 📌 Resposta a objeção de preço
```
"O comprador disse que o FYS é mais caro que o refri que ele já vende.
Crie uma resposta de WhatsApp que valorize o posicionamento premium e o
diferencial de saúde, sem atacar concorrentes. Máximo 4 linhas."
```

#### 📌 Reativação de PDV inativo
```
"Crie uma mensagem para reativar um ponto de venda que experimentou FYS
mas não repetiu o pedido. Tom leve, sem cobranças. Ofereça [amostra / nova
condição]. Máximo 3 linhas."
```

#### 📌 Argumento para inclusão no cardápio de drinks
```
"Crie um argumento para convencer um bartender a usar a FYS Tônica nos
drinks da casa. Destaque o sabor diferenciado e o apelo premium da marca.
Tom próximo, máximo 4 linhas."
```

#### 📌 Fechamento de pedido
```
"Crie uma mensagem de fechamento de pedido para WhatsApp, após apresentação
da linha FYS. Tom consultivo, sem pressão. Máximo 3 linhas."
```

---

## 🛠️ Ferramentas Utilizadas

- **[Claude (Anthropic)](https://claude.ai)** — construção e refinamento dos prompts
- **[FYS](https://www.fys.com.br)** — fonte dos dados reais do produto
- **[GitHub](https://github.com)** — versionamento e portfólio do desafio
- **[DIO](https://www.dio.me)** — plataforma do desafio criativo

---

## 👤 Autor

**Gabriel**
 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Gabriel_Alves-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/gabriel-alves-06755822b/)
---

⭐ Se este repositório foi útil para você, deixa uma estrela!



