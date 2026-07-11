# LaTeX style

Apply these conventions to all generated or revised mathematical content.

## Delimiters

- Use `$...$` for inline mathematics.
- Use `$$...$$` for display mathematics.
- Do not use `\(...\)` or `\[...\]` as equation delimiters.

Preferred:

```latex
The reaction progress is $\lambda\left(t\right)$.

$$
\frac{\mathrm{d}\lambda}{\mathrm{d}t}=R\left(\lambda,T\right)
$$
```

Avoid:

```latex
The reaction progress is \(\lambda(t)\).
```

## Upright symbols

- Write the differential operator as `\mathrm{d}`, not italic `d`.
- Write the base of the natural exponential as `\mathrm{e}`, not italic `e`.
- Write the imaginary unit as `\mathrm{i}`, not italic `i`.
- Do not extend this rule to arbitrary symbols or constants unless the user adds another convention.

Preferred:

```latex
$\mathrm{d}x$, $\frac{\mathrm{d}u}{\mathrm{d}t}$, $\mathrm{e}^{-kt}$
```

## Subscripts

- Wrap a semantic word or textual state label in `\text{...}`.
- Leave a subscript unwrapped when it is itself a mathematical variable or index.

Preferred:

```latex
$u_{\text{unreacted}}$, $T_{\text{ignition}}$, $p_x$, $u_i$
```

Avoid semantic words set as multiplied italic variables:

```latex
$u_{unreacted}$
```

## Parentheses

- Use round parentheses for grouping, precedence, and function calls.
- Wrap paired parentheses with `\left(` and `\right)` so they scale with the content.
- Do not switch to square brackets or braces merely to express nested precedence.

Preferred:

```latex
$f\left(x\right)$
$a\left(b\left(c+d\right)+z\right)$
```

Avoid:

```latex
$f[x]$
$a\{b[c+d]+z\}$
```

Use mathematical brackets only when they carry their own established meaning, not as visual substitutes for parentheses.

## Spacing

- Keep formulas compact and avoid ornamental manual spacing.
- Do not insert `\,` simply to make an expression look airier.
- Use semantic spacing when separating multiple relations or major expression groups on one line.

Acceptable:

```latex
$a=b,\quad c=d$
```

Avoid:

```latex
$a\,=\,b$
```

## Marp HTML interaction

- Keep equations out of `<legend>`.
- When an equation appears inside an HTML container, place a blank line between the equation block and both surrounding HTML tags.
