---
title: Inferno
author: Peter Kourzanov
version: 0.0.2
markdown:
  image_dir: "assets"
export_on_save:
  markdown: true
---

# Inferno

{~~This~>That~~} repository[^1] is {==currently==} **not** in use, be$\cos{\pi\over 2}=0$..
[^1]: and only this one

<table class="noborder"><tr><th>1st</th><th>2nd</th></tr>
<tr><td>

*one* [[Module]]
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

Here comes a [[Module]].

```latex {cmd=Noweb.bat args=["-b","-l","python"] stdin=true output=markdown hide=true run_on_save=true modify_source=true}
\subsection{Foo}
\subparagraph{Step1} Define a variable
<<code/bar.py>>=
`var=2
@
\subparagraph{Step2} Use it.
<<>>=
print("var =",var+1)
```
<!-- code_chunk_output -->


## Foo


##### Step1
 Define a variable
<div id="chunk-code-bar.py-2"/>

###### Code for &laquo;[code/bar.py](#chunk-code-bar.py)&raquo; (2)

```python {cmd=true id="code/bar.py 2" }
var=2
```
<div id="symbol-var"/>


##### Step2
 Use it.
<div id="chunk-code-bar.py-4"/>

###### Code for &laquo;[code/bar.py](#chunk-code-bar.py)&raquo; (4)

```python { continue="code/bar.py 2" cmd=true id="code/bar.py 4" }
print("var =",var+1)
```

___
# Appendix
## Chunks
1. &laquo;[code/bar.py](#chunk-code-bar.py)&raquo;: [2](#chunk-code-bar.py-2),[4](#chunk-code-bar.py-4)

## Definitions
1. [var](#symbol-var): &laquo;[code/bar.py](#chunk-code-bar.py)&raquo; ([2](#chunk-code-bar.py-2))

## Hierarchy

```Dot.bat {cmd=true args=['-e','neato','-z','1'] hide=true output=html run_on_save=true}
 digraph deps {bgcolor="#282c34"
node [color=white fontcolor=gray45]
edge [color=white fontcolor=gray45]
overlap=false
rankdir=LR
"code/bar.py"[style=filled URL="#chunk-code-bar.py"]
}
```

## Full code listings

<div id="chunk-code-bar.py"/>

### &laquo;code/bar.py&raquo;
```python {cmd=true stdin=false run_on_save=false id='code/bar.py'}
var=2
print("var =",var+1)
```


<!-- /code_chunk_output -->
