# Some examples of geiser and chicken problems

This repo contains a bare bones Chicken program that shows what happens in
Geiser now. There are two use cases:

## Auto-completion problems

Steps:

1. Open `test.scm`
2. Run Geiser `M-x run-geiser` (or `C-c C-z`)
3. In the REPL, load the module foo with `,l foo`
4. In the REPL, enter `(import foo)`
5. In the REPL, type `(frob` and begin completion
6. It should now freeze for a while. If not, then I'm alone with this!

## Redefinition problems

Quit the REPL if you haven't and start a new one. Do the above steps until step
four and then

5. Go to `bar.scm` and go to the definition of `frobnicate`
6. Hit `C-M-x` to evaluate the form

And it should hang/freeze. And it doesn't re-evaluate it!
