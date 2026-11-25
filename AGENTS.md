# Instruções para agentes

Este repositório é um **caderno de receitas em Markdown**, não um software. Não há banco de dados nem scripts: buscas e manutenção são feitas por agentes, lendo e editando os arquivos. Tudo é escrito em **português brasileiro**.

## Estrutura

```
README.md       índice das receitas (resumo)
CONTRIBUTING.md como contribuir (para pessoas)
LICENSE         licença (CC BY 4.0, exceto fotos de rótulos)
AGENTS.md       este arquivo
guia/
  creami.md       regras da máquina, princípios e preparo padrão
  ingredientes.md tabela nutricional de referência, conversões, marcas e rótulos conferidos, ingredientes técnicos
  rotulos/        fotos dos rótulos conferidos
receitas/
  <receita>.md            uma receita por arquivo
  <base>--<variacao>.md   variação de uma receita
```

**Fonte da verdade:** o arquivo da receita. O índice do `README.md` é um resumo e pode ficar defasado; em caso de divergência, vale a receita, e o índice deve ser corrigido.

## Como buscar

As buscas não precisam ser determinísticas, mas devem ser honestas sobre a aproximação.

- **Filtros numéricos** (por exemplo, "até 500 kcal", "pelo menos 55 g de proteína"): comece pelo índice do `README.md` e confirme na tabela **Nutrição por pote** de cada receita candidata.
- **Por ingrediente** (por exemplo, "receitas com pêssego"): procure na seção **Ingredientes** dos arquivos em `receitas/`. Considere também os ajustes e mix-ins, mas diga que estão fora da base.
- **Por status** (testada, aprovada…): use a tabela logo abaixo do título de cada receita.
- Os valores são estimativas com margem de ~5–10%. Num filtro, avise quando uma receita estiver perto do limite (por exemplo, ~485 kcal num filtro de "até 500 kcal").

## Formato de cada receita

Todas as receitas seguem o mesmo modelo, nesta ordem. Os nomes das seções e as colunas das tabelas são fixos, para facilitar a busca.

1. **Título** (`#`) e uma linha de descrição em itálico.
2. **Tabela de identificação:** `Versão | Status | Programa | Variação de | Autor`. **Autor** é quem criou a receita, com o @ do GitHub e link para o perfil (por exemplo, `[@lucasfugisawa](https://github.com/lucasfugisawa)`). Ao registrar a receita de outra pessoa, use o @ dela, não o de quem faz o commit.
3. Numa variação: a linha **Diferença em relação à base**.
4. **Nutrição por pote:** `Calorias | Proteína | Carboidratos | Gorduras | Fibras | Volume`, com valores arredondados e `~`, seguida de uma citação (`>`) com a margem e os itens ainda não conferidos.
5. **Ingredientes:** tabela `Quantidade | Ingrediente`. Depois, se houver: **Ajuste na prova**, **Mix-in opcional** e **Topping opcional**, todos marcados "(fora do total)".
6. **Preparo:** passos numerados, completos (a receita deve servir impressa, sozinha).
7. **Detalhamento nutricional:** uma linha por ingrediente, com as colunas `Ingrediente | Quantidade | kcal | Prot. (g) | Carb. (g) | Gord. (g) | Fibras (g) | Origem`, e a linha **Total**.
8. **Notas:** decisões e cuidados específicos.
9. **Histórico:** tabela `Versão | Data | Mudança`.
10. **Testes:** registros de teste, do mais antigo para o mais novo.

Use uma receita existente como modelo ao criar uma nova.

## Regras de conteúdo

- **O caderno aceita receitas de qualquer tipo** (sorvete, sorbet, gelato, milkshake etc.), proteicas ou não. O que é obrigatório: a **nutrição completa por pote, com a proteína**, na receita e no índice do `README.md`.
- **Receitas proteicas** (com whey): meta de **~48–50 g de proteína por pote**. Ajuste a quantidade de whey conforme a proteína dos outros ingredientes (cada 1 g de whey ≈ 0,77 g de proteína) e, se o whey mudar, complete o volume com o líquido da receita.
- Quantidades sempre em **g, ml, colher de chá ou colher de sopa**. Nunca "um pouco de". Pitada de sal = **1/16 de colher de chá (~0,3 g)**.
- Fruta em calda: sempre **peso drenado**, sem a calda.
- **Programa** conforme a composição, seguindo a Ninja: **`SORVETE LIGHT`** para bases com pouca gordura ou pouco açúcar, ou com adoçantes (é o caso das receitas proteicas); outros programas para outras composições (ver [guia/creami.md](guia/creami.md)).
- **Preenchimento alvo: ~470 ml**, nunca acima da **linha MAX (473 ml)**. Estime o volume com o método de [guia/creami.md](guia/creami.md) ("Regras do caderno") e mantenha a estimativa em até ~470 ml.
- Separe sempre **orientação oficial da Ninja**, **prática de usuários** e **inferência**, usando as marcações de [guia/creami.md](guia/creami.md). A fonte prioritária para regras da máquina é a Ninja/SharkNinja.
- Não invente informação técnica nem nutricional. Se não souber, marque como estimativa e avise o usuário.

## Como calcular a nutrição

1. Use os valores de [guia/ingredientes.md](guia/ingredientes.md). Se o ingrediente não estiver lá, **adicione-o primeiro** à tabela de referência, com a origem.
2. **Calorias** = soma das calorias dos ingredientes (não a conta 4/4/9 sobre os macros).
3. **Carboidratos não incluem as fibras** (padrão dos rótulos brasileiros); as fibras têm coluna própria. Em valores de tabela (TACO), desconte a fibra do carboidrato. Polióis (eritritol) não são somados.
4. **Ajustes na prova e mix-ins ficam fora do total.** Informe ao lado o acréscimo que eles causam.
5. No **Detalhamento nutricional**, use números com uma casa decimal para os macros e inteiros para kcal. Na **Nutrição por pote**, arredonde para inteiros com `~`. No índice do `README.md`, use inteiros sem `~`.
6. **Origem** de cada linha: `Rótulo` (conferido no produto usado), `Tabela` (TACO, USDA ou rótulo genérico) ou `Estimado`.
7. Uma pequena imprecisão é aceitável; uma grande não é. Depois de calcular, confira se a soma das linhas bate com o total.

### Quando um valor de referência mudar

Por exemplo, ao conferir o rótulo do whey:

1. Salve a foto do rótulo em `guia/rotulos/`, seguindo o padrão de nomes abaixo. Não apague fotos antigas sem o usuário pedir.
2. Em `guia/ingredientes.md`, atualize a linha da **tabela nutricional de referência** (com a origem `Rótulo`) e a linha do produto em **Ingredientes de marca** (data da conferência e link para a foto).
3. Encontre todas as receitas que usam o ingrediente.
4. Recalcule o detalhamento, o total e a **Nutrição por pote** de cada uma.
5. Atualize a citação de itens não conferidos e o índice do `README.md`.

### Nomes das fotos de rótulos

```
guia/rotulos/<produto>-<marca>[-<variante>]--<AAAA-MM-DD>.<extensão>
```

- Produto, marca e variante em `kebab-case`, sem acento, do mais geral para o mais específico: `pessego-em-calda-zero-schramm`, `whey-growth-sorvete-de-creme`.
- `--` separa o produto da data da conferência. A data evita colisão quando o mesmo produto for conferido de novo.
- Mais de uma foto do mesmo produto no mesmo dia: acrescente `-2`, `-3` depois da data.
- Mantenha a extensão original da imagem.

Mudança de valor de referência **não muda a versão** da receita, porque a fórmula é a mesma.

## Versões e variações

- **Versão** é a evolução da mesma receita: a nova substitui a anterior. O número **só sobe quando a fórmula muda** (ingrediente, quantidade ou programa). Correção de texto ou recálculo nutricional não muda a versão. Toda nova versão ganha uma linha no **Histórico**, com o que mudou e por quê.
- **Variação** é uma receita irmã que coexiste com a original. Vira um **arquivo completo** chamado `<base>--<variacao>.md`, com a base indicada na coluna **Variação de** (com a versão da base) e a linha **Diferença em relação à base**. A receita base ganha um link para a variação.
- **Regra de corte:** se a mudança altera a nutrição de forma relevante ou vai ser testada por conta própria, é variação. Se é um detalhe (uma pitada de canela, um mix-in), fica como opcional dentro da receita.
- Quando a base mudar de versão, **pergunte** se as variações devem acompanhar; não propague sozinho.

## Como registrar um teste

Adicione ao final da seção **Testes** (e remova o texto "Nenhum teste registrado ainda."):

```markdown
### AAAA-MM-DD — v1

- **Programa:** `SORVETE LIGHT`
- **RE-SPIN:** não / sim, 1×, com 2 colheres de sopa de leite desnatado
- **Textura:** …
- **Sabor e doçura:** …
- **Ajustes feitos na hora:** …
- **Nota:** 4/5
- **Para a próxima:** …
```

Depois do primeiro teste, mude o status da receita para **Em teste**. **Aprovada** e **Descontinuada** só com a decisão explícita do usuário.

Se o teste levar a uma mudança de fórmula, crie a nova versão (ou a variação) e registre no Histórico.

## Checklist ao alterar uma receita

- [ ] Tabela de identificação (versão, status e autor)
- [ ] Ingredientes e preparo coerentes entre si
- [ ] Detalhamento nutricional, total e **Nutrição por pote** recalculados
- [ ] Citação de itens não conferidos atualizada
- [ ] Histórico, se a fórmula mudou
- [ ] Variações e links entre base e variação
- [ ] Índice do `README.md`

## Git

Mensagens de commit em português, no imperativo, descrevendo a mudança na receita (por exemplo, "Aumenta o pêssego para 200 g na receita de pêssego").
