# Referências

Registro das conferências feitas no mundo real (rótulos, medidas do equipamento) e as evidências de cada uma. Os valores em uso ficam em [guia/ingredientes.md](../guia/ingredientes.md) e [guia/creami.md](../guia/creami.md); aqui fica **de onde eles vieram**.

**Este registro só cresce:** novas conferências entram no fim da tabela. Se um valor mudar (por exemplo, o fabricante mudou a fórmula), registre a nova conferência numa nova linha, sem apagar a antiga.

## Conferências

| Data | O que foi conferido | Resultado | Evidência |
|---|---|---|---|
| 2026-10-25 | Rótulo do whey Growth, sabor sorvete de creme (site da Growth) | 30 g: 125 kcal, 23 g de proteína, 3,8 g de carboidratos, 2 g de gorduras | [foto](rotulos/whey-growth-sorvete-de-creme--2026-10-25.webp) |
| 2026-10-25 | Rótulo do figo em calda Tozzi (lata de 850 g, 400 g drenado) | 100 g: 174 kcal, 44 g de carboidratos, 4 g de fibras | [foto](rotulos/figo-em-calda-tozzi--2026-10-25.webp) |
| 2026-10-25 | Rótulo do pêssego em calda zero adição de açúcar Schramm | 100 g (fruta com calda): 23 kcal, 5,7 g de carboidratos. Substitui o Tozzi, cuja tabela não foi encontrada | [foto](rotulos/pessego-em-calda-zero-schramm--2026-10-25.jpg) |
| 2026-10-25 | Rótulo do cacau solúvel 100% Dr. Oetker | 100 g: 334 kcal; 1 colher de sopa ≈ 10 g. Substitui o Dois Frades | [foto](rotulos/cacau-soluvel-dr-oetker--2026-10-25.jpg) |
| 2026-10-25 | Volume do pote de 473 ml | Até a linha MAX: 473 ml. Até a boca: 500 ml | Medição do usuário |

## Nomes dos arquivos

```
rotulos/<produto>-<marca>[-<variante>]--<AAAA-MM-DD>.<extensão>
```

- **Produto, marca e variante** em `kebab-case`, sem acento, do mais geral para o mais específico: `pessego-em-calda-zero-schramm`, `whey-growth-sorvete-de-creme`.
- **`--` separa o produto da data**, como o `--` das variações de receita. A data é a da conferência.
- **A data evita colisão** quando o mesmo produto for conferido de novo (rótulo novo, fórmula nova): o arquivo antigo fica, e o novo ganha outra data.
- Mais de uma foto do mesmo produto no mesmo dia: acrescente `-2`, `-3` depois da data (`...--2026-10-25-2.jpg`).
- Mantenha a extensão original da imagem.
