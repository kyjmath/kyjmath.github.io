---
layout: post
comments: true
title : New start
categories: [Projects]
---
<pre class="hljs" style="display: block; overflow-x: auto; padding: 0.5em; background: rgb(40, 40, 40); color: rgb(235, 219, 178);"><span class="hljs-keyword" style="color: rgb(251, 73, 52);">from</span> astropy.units <span class="hljs-keyword" style="color: rgb(251, 73, 52);">import</span> fa
<span class="hljs-keyword" style="color: rgb(251, 73, 52);">from</span> astropy.io.misc.yaml <span class="hljs-keyword" style="color: rgb(251, 73, 52);">import</span> name
 
a = [<span class="hljs-number" style="color: rgb(211, 134, 155);">1</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">2</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">3</span>]
print(a, type(a))
 
b = [<span class="hljs-number" style="color: rgb(211, 134, 155);">10</span>, a, <span class="hljs-number" style="color: rgb(211, 134, 155);">30.5</span>, <span class="hljs-keyword" style="color: rgb(251, 73, 52);">True</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'컴퓨터'</span>]
print(b, type(b))
 
print()
family = [<span class="hljs-string" style="color: rgb(184, 187, 38);">'엄마'</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'아빠'</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'나'</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'여동생'</span>]
family.append(<span class="hljs-string" style="color: rgb(184, 187, 38);">'남동생'</span>)    <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 리스트 추가</span>
family.insert(<span class="hljs-number" style="color: rgb(211, 134, 155);">0</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'할아버지'</span>)    <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 위치 삽입</span>
family.extend([<span class="hljs-string" style="color: rgb(184, 187, 38);">'삼촌'</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'조카'</span>])
family += [<span class="hljs-string" style="color: rgb(184, 187, 38);">'이모'</span>, <span class="hljs-string" style="color: rgb(184, 187, 38);">'고모'</span>]
family.remove(<span class="hljs-string" style="color: rgb(184, 187, 38);">'나'</span>)  <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 삭제</span>
<span class="hljs-keyword" style="color: rgb(251, 73, 52);">del</span> family[<span class="hljs-number" style="color: rgb(211, 134, 155);">1</span>]   <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 인덱스 삭제</span>
print(family, len(family))
print(family.index(<span class="hljs-string" style="color: rgb(184, 187, 38);">'남동생'</span>))  <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 특정 항목 위치 찾기</span>
 
print()
aa2 = [<span class="hljs-string" style="color: rgb(184, 187, 38);">'123'</span>,<span class="hljs-string" style="color: rgb(184, 187, 38);">'34'</span>,<span class="hljs-string" style="color: rgb(184, 187, 38);">'234'</span>]
print(aa2)
aa2.sort()
print(aa2)
aa2.sort(key=int)
print(aa2)
 
print()
aaa=[<span class="hljs-number" style="color: rgb(211, 134, 155);">3</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">1</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">5</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">2</span>,<span class="hljs-number" style="color: rgb(211, 134, 155);">4</span>]
aaa.sort()
print(aaa)
aaa.sort(reverse = <span class="hljs-keyword" style="color: rgb(251, 73, 52);">True</span>)
print(aaa)
 
print(<span class="hljs-string" style="color: rgb(184, 187, 38);">'---'</span> * <span class="hljs-number" style="color: rgb(211, 134, 155);">5</span>)
name = [<span class="hljs-string" style="color: rgb(184, 187, 38);">'tom'</span>,<span class="hljs-string" style="color: rgb(184, 187, 38);">'james'</span>,<span class="hljs-string" style="color: rgb(184, 187, 38);">'oscar'</span>]
name2 = name    <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 주소 치환, 얕은 복사</span>
print(name, id(name))
print(name2, id(name2))
name[<span class="hljs-number" style="color: rgb(211, 134, 155);">0</span>] = <span class="hljs-string" style="color: rgb(184, 187, 38);">'paul'</span>
print(name, <span class="hljs-string" style="color: rgb(184, 187, 38);">' '</span>, name2)
 
print()
<span class="hljs-keyword" style="color: rgb(251, 73, 52);">import</span> copy
name3 = copy.deepcopy(name)     <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># 깊은 복사, 완전 별개의 list가됨</span>
name3[<span class="hljs-number" style="color: rgb(211, 134, 155);">1</span>] = <span class="hljs-string" style="color: rgb(184, 187, 38);">'john'</span>
print(name, <span class="hljs-string" style="color: rgb(184, 187, 38);">' '</span>, name3)
 
print()
sbs = [<span class="hljs-number" style="color: rgb(211, 134, 155);">10</span>, <span class="hljs-number" style="color: rgb(211, 134, 155);">20</span>, <span class="hljs-number" style="color: rgb(211, 134, 155);">30</span>]
sbs.append(<span class="hljs-number" style="color: rgb(211, 134, 155);">40</span>)
print(sbs)
sbs.pop()   <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># stack 구조 : LIFO</span>
print(sbs)
 
print()
sbs = [<span class="hljs-number" style="color: rgb(211, 134, 155);">10</span>, <span class="hljs-number" style="color: rgb(211, 134, 155);">20</span>, <span class="hljs-number" style="color: rgb(211, 134, 155);">30</span>]
sbs.append(<span class="hljs-number" style="color: rgb(211, 134, 155);">40</span>)
print(sbs)
sbs.pop(<span class="hljs-number" style="color: rgb(211, 134, 155);">0</span>)  <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;"># queue 구조 : FIFO</span>
print(sbs)
</pre>
