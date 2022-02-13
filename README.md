This repository is automatically commited and pushed using:

```
autocmd BufWritePost *coc/ultisnips/*.snippets !git add .; git commit -m "update"; git push -u origin main
```

A valid snippet should starts with:

    	snippet trigger_word [ "description" [ options ] ]

and end with:

    	endsnippet

Snippet options:

    	b - Beginning of line.
    	i - In-word expansion.
    	w - Word boundary.
    	r - Regular expression
    	e - Custom context snippet
    	A - Snippet will be triggered automatically, when condition matches.

Basic example:

    	snippet emitter "emitter properties" b
    	private readonly ${1} = new Emitter<$2>()
    	public readonly ${1/^_(.*)/$1/}: Event<$2> = this.$1.event
    	endsnippet

Online reference: https://github.com/SirVer/ultisnips/blob/master/doc/UltiSnips.txt
