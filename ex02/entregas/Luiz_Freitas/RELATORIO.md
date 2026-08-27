# Relatório de correções

**Nome:** Luiz Freitas  
**Data:** 27/08/2026

---

## Alteração 1

**Onde estava o problema:** Estrutura da página HTML, especialmente nos blocos de cabeçalho, navegação, conteúdo principal, seções e tabela de preços.

**Por que era um problema:** A página estava organizada de forma funcional, mas sem aproveitar completamente a semântica do HTML. Isso prejudica usuários de leitor de tela, que precisam de uma estrutura clara para compreender a hierarquia da página e navegar entre as seções com mais facilidade. A ausência de uma organização melhor também dificulta o uso por pessoas que dependem de navegação assistida.

**O que mudei:** Mantive e organizei corretamente os elementos semânticos, como `header`, `nav`, `main`, `section`, `h1`, `h2`, `table`, `thead`, `tbody`, `caption`, `th scope="col"` e `footer`. A estrutura do conteúdo passou a refletir melhor a lógica do portal, separando cabeçalho, menu, conteúdo principal e rodapé.

**Critério do WCAG:** WCAG 1.3.1 - Informações e Relacionamentos; WCAG 2.4.1 - Pular blocos.

---

## Alteração 2

**Onde estava o problema:** Ações e áreas importantes da página, como links do menu, botão de reserva e descrição da tabela.

**Por que era um problema:** Elementos genéricos, como links e botões sem descrição clara, podem ser interpretados de forma confusa por leitores de tela. Usuários com deficiência visual ou baixa visão podem ter dificuldade para compreender a função de cada parte da interface, principalmente quando o texto visível não transmite a finalidade do elemento de forma explícita.

**O que mudei:** Apliquei atributos como `aria-label` em links e ações, `aria-current="page"` no item do menu correspondente à página atual, `aria-labelledby` para associar títulos e regiões e `aria-describedby` para descrever a tabela de preços. Essa melhoria deixa a navegação e a leitura do conteúdo mais compreensíveis para tecnologias assistivas.

**Critério do WCAG:** WCAG 4.1.2 - Nome, Função e Valor; WCAG 1.3.1 - Informações e Relacionamentos.

---

## Alteração 3

**Onde estava o problema:** A página de ingressos não possuía suporte de tradução para LIBRAS, o que limita o acesso de usuários surdos e deficientes auditivos.

**Por que era um problema:** Mesmo com boa estrutura semântica e atributos ARIA, a página ainda não contemplava uma solução acessível para pessoas que utilizam LIBRAS como principal forma de comunicação. A ausência de um widget assistivo impede que esse público tenha uma experiência de acesso mais inclusiva e direta ao conteúdo.

**O que mudei:** Incluí o plugin do VLibras na página, com o código padrão do widget e a inicialização via JavaScript. O bloco foi adicionado ao final do documento, antes do fechamento do `body`, conforme a implementação recomendada. Com isso, a página passa a oferecer suporte de tradução para LIBRAS no próprio site.

**Critério do WCAG:** WCAG 1.1.1 - Conteúdo Não Textual; WCAG 1.3.1 - Informações e Relacionamentos; WCAG 3.1.2 - Idioma da Página e da Interface.

---

## Alteração 4

**Onde estava o problema:** Tabela de preços da seção principal, especialmente no uso de células em formato genérico e na ausência de uma descrição mais explícita para leitura por leitor de tela.

**Por que era um problema:** Quando uma tabela é estruturada com `td` em todas as células, o leitor de tela pode anunciar o conteúdo de forma menos contextualizada, sem deixar claro qual categoria se refere a cada valor. Isso prejudica usuários que navegam por tabela, especialmente em leituras sequenciais e em comparação entre colunas e linhas. A ausência de um resumo textual também reduz a clareza da estrutura da informação.

**O que mudei:** Reestruturei a tabela para que cada linha tenha uma célula de identificação com `scope="row"`, enquanto as demais células mantiveram relação com os cabeçalhos das colunas por meio de `headers` e `id`. Também ajustei o `caption` para descrever melhor o conteúdo da tabela, deixando a leitura mais natural para tecnologias assistivas. O trecho da seção “Sessões extras de dezembro” foi destacado como linha de categoria com `colspan`, preservando a lógica de agrupamento da informação.

**Critério do WCAG:** WCAG 1.3.1 - Informações e Relacionamentos; WCAG 2.4.6 - Cabeçalhos e Rótulos; WCAG 3.1.2 - Idioma da Página e da Interface.

---

## Verificação final

**Percorri a página inteira usando apenas o teclado:** ( ) sim   (x) não

**Consegui alcançar e acionar todos os elementos interativos:** ( ) sim   (x) não

**Ouvi a página com leitor de tela do começo ao fim:** ( ) sim   (x) não

**O que o leitor de tela ainda anuncia de forma confusa, se houver:**
Não foi realizada validação prática em ambiente com leitor de tela durante esta etapa. A estrutura foi ajustada conforme boas práticas de acessibilidade e com base na documentação do arquivo de explicação, mas a verificação real com um leitor de tela deve ser feita em navegador com tecnologia assistiva ativa para confirmar a leitura final do conteúdo.

---

## Observações

A página ficou mais organizada, mais semântica e mais inclusiva. A principal melhoria foi a combinação de HTML acessível, uso correto de atributos ARIA e a inserção do widget do VLibras, que reforça a acessibilidade para pessoas surdas. A validação técnica foi feita por leitura do código e análise das boas práticas, mas a revisão final em ambiente real com teclado e leitor de tela continua sendo o passo mais importante para garantir qualidade de uso.
