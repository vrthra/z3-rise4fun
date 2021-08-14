---
title: "Getting Started with Z3: A Guide"
layout: default
---

<script src="coi-serviceworker.js"></script>
<script src="out/z3.js"> </script>
<script src="helper.js"> </script> 

This is a reconstruction of the [rise4fun Z3](https://web.archive.org/web/20210119175613/https://rise4fun.com/Z3/tutorial/guide) website with a wasm compiled version of Z3 using [z3-wasm](https://github.com/bramvdbogaerde/z3-wasm).


## Tutorials

- [Guide](guide.html)
- [Fixedpoints](fixedpoint.html)
- [Optimization](optimization.html)
- [Sequences](sequences.html)
- [Strategies](strategies.html)

<textarea id="z3_input" rows=20 width="100%"> </textarea>
<button onclick="run_id('z3_input','z3_result')">Run</button>
<br>
<code id="z3_result"> </code>
