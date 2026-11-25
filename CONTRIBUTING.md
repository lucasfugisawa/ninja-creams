# Como contribuir

Obrigado pelo interesse! Este é um caderno de receitas para a Ninja CREAMi (pote de 473 ml). Toda contribuição é bem-vinda: receita nova, variação, correção ou resultado de teste.

## O que é aceito

**Receitas de qualquer tipo**: sorvete, sorbet, gelato, milkshake, frozen yogurt e afins, proteicas ou não.

Toda receita precisa ter:

- **a nutrição completa por pote**: calorias, proteína, carboidratos, gorduras e fibras. A proteína aparece sempre, na receita e no índice;
- quantidades em **g, ml, colher de chá ou colher de sopa** (colheres medidoras padrão, sempre rasas), nunca "um pouco de";
- volume de base que **não passe da linha MAX** do pote (473 ml); o ideal é encher até ~470 ml;
- o **programa** da CREAMi indicado conforme a composição da receita (veja o [guia da CREAMi](guia/creami.md)).

**Receitas proteicas**, feitas com whey, seguem a convenção do caderno: **~48–50 g de proteína por pote**.

O formato completo de cada receita (seções, tabelas e cálculo nutricional) está no [AGENTS.md](AGENTS.md). Use uma receita existente como modelo.

## Como enviar

**Não sabe ou não quer calcular a nutrição?** Abra uma issue com o formulário **[Nova receita](https://github.com/lucasfugisawa/ninja-creams/issues/new?template=nova-receita.yml)**: ele pede os ingredientes, as quantidades e o preparo. A receita é formatada e calculada na revisão.

**Quer enviar pronta?**

1. Crie `receitas/<nome-da-receita>.md`, em kebab-case e sem acentos.
2. Preencha as colunas **Tipo** e **Autor** (com o seu @ do GitHub).
3. Se usar um ingrediente que ainda não está em [guia/ingredientes.md](guia/ingredientes.md), acrescente-o na tabela de referência, com a origem do valor (rótulo, tabela TACO/USDA ou estimativa).
4. Acrescente a receita ao índice do [README.md](README.md), em ordem alfabética.
5. Abra um pull request e confira o checklist que aparece na descrição.

## Índice sempre consistente

O índice do [README.md](README.md) precisa refletir exatamente o que existe em `receitas/`. Todo pull request que mexe em receitas atualiza o índice junto:

- **receita nova:** acrescente a linha no índice;
- **receita removida:** remova a linha;
- **receita renomeada:** atualize o nome e o link;
- **valores alterados** (calorias, macros ou volume): atualize a linha com os mesmos valores da receita.

## Testes

Receitas não testadas são aceitas, com o status **Não testada**.

Testou uma receita do caderno? Conte como ficou pelo formulário **[Resultado de teste](https://github.com/lucasfugisawa/ninja-creams/issues/new?template=resultado-de-teste.yml)**, ou registre direto na seção **Testes** da receita, no modelo do [AGENTS.md](AGENTS.md#como-registrar-um-teste). Informe quem testou (seu @) e o que você fez diferente da receita: marca do whey, tipo de leite, quantidades.

## Fotos de rótulos

Fotos de tabelas nutricionais são bem-vindas para conferir valores. Antes de enviar:

- remova a localização e os demais metadados da foto;
- enquadre só o rótulo, sem pessoas nem ambientes da casa.

## Fontes

Não copie receitas de sites ou livros. Inspirar-se é ótimo: cite a fonte nas **Notas** da receita.

## Licença

Ao contribuir, você concorda que sua contribuição seja publicada sob a licença deste repositório ([CC BY 4.0](LICENSE)).
