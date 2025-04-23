# Markdown

> Uma linguagem de marcação, o Markdown oferece uma abordagem enxuta para edição de conteúdo. Ele define uma sintaxe concisa e leve que elimina a sobrecarga inerente ao HTML, proporcionando uma experiência de criação mais acessível.

## O que é o Markdown?

> Markdown é uma linguagem de marcação que oferece uma abordagem enxuta para edição de conteúdo, protegendo os criadores de conteúdo da sobrecarga do HTML.

### Marcações

- Itálico: _Texto em itálico_
- Itálico: _Texto em itálico_
- Negrito: **Texo em negrito**
- Negrito: **Texto em negrito**
- Netrigo e itálico: **Texto em negrito com trecho em _itálico_**
- Para usar asterisco, precisa usar o escape: Olá \* Mundo!
- Escapes exemplo: \* ou \_
- Níveis de titulos de 1 a 6: # ou ######
- Link para imagem:

  ![Uma imagem](/images/link_image.png)

- Link para site:

  [Clique Aqui](https://learn.microsoft.com/en-us/training/modules/communicate-using-markdown/2-what-is-markdown)

- Listas:

  1.  Numérica

  - Ordenada
    - Aninhada

- Tabelas
  > Você pode construir tabelas usando uma combinação de barras verticais (|) para quebras de coluna e traços (-) para designar a linha anterior como um cabeçalho.

| Primeiro | Segundo | Terceiro |
| -------- | ------- | -------- |
| 1        | 2       | 3        |
| 3        | 4       | 5        |

- Citação: >

> Oi eu sou uma citação.

- HTML

> Se você encontrar um cenário HTML não suportado pelo Markdown, você pode usar esse HTML em linha.

Aqui está um <br /> quebra de linha

- Trabalhar com código:

```
function Home() {
   return <h1> Oi React </h1>
}
```

> O GFM estende esse suporte com destaque de sintaxe para linguagens populares.

```javascript
test("1 mais 1 deveria retornar 2", () => {
  resultado = calculadora.somar(1, 1);
  expect(resultado).toBe(2);
});
```

## Problemas de cross-link e solicitações de pull

1. A maneira mais fácil de fazer isso é usar o formato #ID, como #3602

| Tipo de referência  | Referência bruta                             | link curto |
| ------------------- | -------------------------------------------- | ---------- |
| Url de PR ou issues | https://github.com/desktop/desktop/pull/3602 | #3602      |

## Menção do GitHub

- @menção (@alxss01)

## Lista de tarefas GitHub

- [ ] Primeira Tarefa
- [x] Segunda Tarefa

## Comandos de barra

> Os comandos de barra podem economizar seu tempo reduzindo a digitação necessária para criar Markdown complexo.

> Você pode usar comandos de barra em qualquer campo de descrição ou comentário em problemas, solicitações de pull ou discussões em que esse comando de barra seja suportado.

| comando   | descrição                                                                                                                                                        |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| /code     | Insere um bloco de código Markdown. Você escolhe o idioma.                                                                                                       |
| /details  | Insere uma área de detalhes recolhível. Você escolhe o título e o conteúdo.                                                                                      |
| /table    | Insere uma tabela Markdown. Você escolhe o número de colunas e linhas.                                                                                           |
| /tasklist | Insere uma lista de tarefas. Este comando de barra só funciona na descrição de um problema.                                                                      |
| /template | Exibe todos os modelos no repositório. Você escolhe o modelo a ser inserido. Este comando de barra funciona para modelos de problemas e modelos de pull request. |

## Exercício - Comunicar usando Markdown

1. Suponha que você queira incluir um snippet HTML no seu site do GitHub Pages, mas o Markdown não oferece uma maneira de renderizá-lo. O que você deve fazer?
   R: Basta adicionar o HTML em linha.
