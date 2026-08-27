# Exercício 2, tornar uma página acessível

**IHC, Qualidade e Teste de Software** — IFSP Câmpus Campos do Jordão
Atividade individual, realizada em laboratório.

---

## Situação

A página `ingressos.html` faz parte do portal fictício Luzes da Cidade. Ela
funciona e tem boa aparência, mas apresenta barreiras que impedem ou dificultam
o uso por pessoas com deficiência.

## O que você deve fazer

Corrija a página para que ela atenda ao nível **AA** do WCAG.

Mantenha o mesmo conteúdo, a mesma informação e a mesma aparência geral. Nada
pode desaparecer da página. O que muda é a forma como está construída.

Você pode alterar `ingressos.html` e `css/estilo.css`.

## O que será avaliado

**1. HTML semântico**
Uso correto dos elementos que descrevem o significado do conteúdo, no lugar de
`div` genérica.

**2. WAI-ARIA**
Uso de atributos ARIA onde o HTML sozinho não dá conta. Atenção: ARIA não
corrige elemento errado. A primeira regra do ARIA é não usar ARIA quando existe
elemento HTML nativo com a mesma função.

**3. VLibras**
Integração do widget do VLibras à página.

**4. Justificativa**
Preencha o arquivo `RELATORIO.md` explicando cada alteração. Uma correção sem
justificativa vale menos do que uma justificativa consistente.

---

## Como entregar

A entrega é feita por **pull request**. Siga a ordem abaixo.

### 1. Faça o fork antes de começar

No repositório da disciplina, clique em **Fork**, no canto superior direito.
Isso cria uma cópia do repositório na sua conta.

Faça isso **antes** de editar qualquer coisa. Quem edita primeiro e bifurca
depois acaba perdendo trabalho.

### 2. Baixe os arquivos para editar no VS Code

No **seu fork**, clique em **Code** e depois em **Download ZIP**. Extraia em uma
pasta e abra essa pasta no VS Code.

Trabalhe normalmente: edite, salve e **abra a página no navegador** para testar.
Repita quantas vezes precisar.

### 3. Crie sua pasta de entrega no fork

Sua entrega vai em uma pasta com seu nome, no formato `sobrenome-nome`, dentro
de `entregas/`.

Para criar uma pasta pelo navegador: clique em **Add file**, depois em **Create
new file**, e no campo do nome digite o caminho completo, por exemplo:

```
entregas/silva-maria/ingressos.html
```

A pasta é criada junto com o arquivo.

### 4. Envie um arquivo por vez

Para cada arquivo que você alterou:

1. Abra o arquivo no VS Code e selecione tudo com `Ctrl+A`
2. Copie com `Ctrl+C`
3. No GitHub, crie o arquivo correspondente dentro da sua pasta de entrega
4. Cole o conteúdo e clique em **Commit changes**
5. **Confira** se o que foi salvo é o que você colou, antes de passar ao próximo

Sua pasta de entrega deve ficar assim:

```
entregas/sobrenome-nome/
  ingressos.html
  css/estilo.css
  RELATORIO.md
```

As imagens não precisam ser reenviadas. Ajuste o caminho delas no seu HTML para
`../../img/`.

### 5. Abra o pull request

No seu fork, clique em **Contribute** e depois em **Open pull request**.
Preencha a descrição conforme o modelo que aparece e envie.

---

## Pontos de atenção

**Não altere os arquivos originais do enunciado.** Sua entrega vai apenas para a
sua pasta dentro de `entregas/`. Pull request que modifica o enunciado será
devolvido para correção.

**O arquivo CSS também contém barreiras.** Duas delas envolvem valores de cor e
visibilidade do foco.

**Antes de concluir**, percorra a página inteira usando **apenas o teclado**, com
a tecla Tab. Se você não conseguir alcançar e acionar tudo, alguém também não
vai conseguir.

**Depois**, ligue o leitor de tela do seu sistema e ouça a página do começo ao
fim. O que ele anuncia é o que a pessoa recebe.

---

## Material de consulta

- Padrões e diretrizes de acessibilidade da W3C
  https://www.w3.org/WAI/standards-guidelines/

- WAI-ARIA
  https://www.w3.org/WAI/standards-guidelines/aria/

- VLibras, Governo Digital
  https://www.gov.br/governodigital/pt-br/acessibilidade-e-usuario/vlibras

- Elementos semânticos do HTML
  https://www.w3schools.com/html/html5_semantic_elements.asp

- Botões e links, quando usar cada um
  https://www.w3schools.com/accessibility/accessibility_buttons_links.php

- Contraste de cores, critério 1.4.3 do WCAG
  https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html

- Foco visível, critério 2.4.7 do WCAG
  https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html
