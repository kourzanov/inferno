---
title: Inferno
author: Peter Kourzanov
version: 0.1
export_on_save:
  markdown: true
---

# Inferno

This repository[^1] is currently **not** in use, be$\cos{\pi\over 2}=0$..
[^1]: and only this one

<table class="noborder"><tr><th>1st</th><th>2nd</th></tr>
<tr><td>

*one*
```julia
1+2
```
</td>
<td>

**two**
* foo
* bar</td>
</tr>
</table>

```latex {cmd=Noweb.bat args=["-b","-l","python"] stdin=true output=markdown hide=true run_on_save=true modify_source=true}
\subsection{Foo}
\paragraph{Step1}. Define a variable
<<bar>>=
var=2
@
\paragraph{Step2}. Use it.
<<>>=
print("var =",var)
```
<!-- code_chunk_output -->


## Foo


#### Step1
. Define a variable
<div id="chunk-bar-2"/>

###### Code for &laquo;[bar](#chunk-bar)&raquo; (2)

```python {cmd=true id="bar 2" }
var=2
```


#### Step2
. Use it.
<div id="chunk-bar-4"/>

###### Code for &laquo;[bar](#chunk-bar)&raquo; (4)

```python { continue="bar 2" cmd=true id="bar 4" }
print("var =",var)
```

___
# Appendix
## Chunks
1. &laquo;[bar](#chunk-bar)&raquo;: [2](#chunk-bar-2),[4](#chunk-bar-4)

## Definitions

## Hierarchy

```Dot.bat {cmd=true args=['-e','neato','-z','1'] hide=true output=html run_on_save=true}
 digraph deps {bgcolor="#282c34"
node [color=white fontcolor=gray45]
edge [color=white fontcolor=gray45]
overlap=false
rankdir=LR
"bar"[style=filled URL="#chunk-bar"]
}
```

## Full code listings

<div id="chunk-bar"/>

### &laquo;bar&raquo;
```python {cmd=true stdin=false run_on_save=false id='bar'}
var=2
print("var =",var)
```


<!-- /code_chunk_output -->
