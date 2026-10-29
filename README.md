<h1 align="center">Functional Versus Imperative Is Solved</h1>

<p align="center">
  <i>A deadpan paper that settles the functional versus imperative debate, mostly by citing the people who settled it first.</i>
</p>

<h3 align="center">
  <a href="./functional-vs-imperative.pdf">Read the paper</a>
  <span> · </span>
  <a href="./functional-vs-imperative.tex">LaTeX source</a>
  <span> · </span>
  <a href="#building">Build</a>
</h3>

<br/>

## What is this?

*Functional Versus Imperative Is Solved* treats the argument between the two styles as a list of questions with known answers. Both compute the same functions, compilers translate between them, purity costs at most a logarithmic factor in Pippenger's model, and data races need state that is both shared and mutable, which functional programming and Rust rule out from opposite ends. The tone is deadpan, but every theorem, number and citation is meant to be correct.

Energy figures come from Pereira et al. (SLE 2017); every source is listed in the paper's references.

## What's inside

<table>
  <tr>
    <td width="50%"><b>The Ceasefire of 1937</b><br>Why neither style can compute anything the other can't</td>
    <td width="50%"><b>Every Program Is Both</b><br>SSA form is functional programming, and lazy evaluation runs on mutation</td>
  </tr>
  <tr>
    <td width="50%"><b>Equally Powerful, Not Equally Expressive</b><br>Felleisen's expressiveness, and the changes each style makes awkward</td>
    <td width="50%"><b>The Price of Purity</b><br>A logarithm at most, charged by Pippenger and refunded by laziness</td>
  </tr>
  <tr>
    <td width="50%"><b>Share or Mutate</b><br>Data races need shared mutable state, and each side rules them out its own way</td>
    <td width="50%"><b>What the Evidence Says</b><br>Defect studies, controlled experiments, energy use and verified software</td>
  </tr>
</table>

## Building

Requires a TeX distribution with `latexmk`, `pgfplots`, `tcolorbox`, `listings`, `booktabs` and `hyperref`; a full TeX Live install has them all.

```sh
latexmk -pdf functional-vs-imperative.tex
```

The source is formatted with [tex-fmt](https://github.com/WGUNDERWOOD/tex-fmt) using `tex-fmt.toml`. Run `tex-fmt --check functional-vs-imperative.tex` before committing; VS Code with LaTeX Workshop formats on save.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
