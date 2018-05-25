---
title: Inferno
author: Peter Kourzanov
version: 0.0.1
output: word_document
markdown:
  image_dir: "assets"
export_on_save:
  markdown: true
---

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [§ Inferno](#inferno)
	* [§ Foo](#foo)
		* [§ Bar](#bar)
			* [§ Step1](#step1)
					* [§ &laquo;code/bar.py&raquo; (≡ 2)](#laquocodebarpychunk-code-barpyraquo-2)
			* [§ Step2](#step2)
					* [§ &laquo;code/bar.py&raquo; (⩲ 4)](#laquocodebarpychunk-code-barpyraquo-4)
* [§ Appendix](#appendix)
	* [§ Chunks](#chunks)
	* [§ Definitions](#definitions)
	* [§ Hierarchy](#hierarchy)
	* [§ Full code listings](#full-code-listings)
		* [§ &laquo;code/bar.py&raquo;](#laquocodebarpyraquo)

<!-- /code_chunk_output -->

# Inferno

{~~This~>That~~} repository[^1] is {==currently==} **not** in use, be$`\cos{\pi\over 2}=0`$..
[^1]: and only this one

Moreover,
```math
\sin^2{x}+\cos^2{x}=1
```
Some diagrams:

1. one

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```
2. two

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
3. three

```mermaid
gitGraph:
options
{
    "nodeSpacing": 150,
    "nodeRadius": 10
}
end
commit
branch newbranch
checkout newbranch
commit
commit
checkout master
commit
commit
merge newbranch
```
4. four

```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

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

Here comes a [Module](Module.md).

```latex {cmd=Noweb.bat args=["-b","-l","python"] stdin=true output=markdown hide=true run_on_save=true modify_source=true}
\subsection{Foo}
\subsubsection{Bar}
\paragraph{Step1} Define a variable
<<code/bar.py>>=
`var=2
@
\paragraph{Step2} Use it.
<<>>=
print("var =",var+1)
```
<!-- code_chunk_output -->


## Foo


### Bar


#### Step1
 Define a variable

<div id="chunk-code-barpy-2"/>

###### &laquo;[code/bar.py](#chunk-code-barpy)&raquo; (≡ 2)

```python {cmd=true id="code/bar.py 2" }
var=2
```
<div id="symbol-var"/>



#### Step2
 Use it.

<div id="chunk-code-barpy-4"/>

###### &laquo;[code/bar.py](#chunk-code-barpy)&raquo; (⩲ 4)

```python { continue="code/bar.py 2" cmd=true id="code/bar.py 4" }
print("var =",var+1)
```

___

___
# Appendix
## Chunks
1. &laquo;[code/bar.py](#chunk-code-barpy)&raquo;: [2](#chunk-code-barpy-2),[4](#chunk-code-barpy-4)

## Definitions
1. [var](#symbol-var): &laquo;[code/bar.py](#chunk-code-barpy)&raquo; ([2](#chunk-code-barpy-2))

## Hierarchy

```Dot.bat {cmd=true args=['-e','neato','-z','.25'] hide=true output=html run_on_save=true usemap="#deps"}
 digraph deps {bgcolor="#282c34"
node [color=white fontcolor=gray45]
edge [color=white fontcolor=gray45]
overlap=false
rankdir=LR
}
```
<map id="deps" name="deps">
</map>

## Full code listings

<div id="chunk-code-barpy"/>

### &laquo;code/bar.py&raquo;
```python {cmd=true stdin=false run_on_save=false id='code/bar.py'}
var=2
print("var =",var+1)
```


<!-- /code_chunk_output -->
