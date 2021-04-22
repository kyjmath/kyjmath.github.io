---
layout: post
comments: true
title : New start
categories: [Projects]
---

<!-- HTML generated using hilite.me --><div style="background: #ffffff; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #888888"># 집합형 자료 형 중 list type : 순서가 있고, 요소값 수정 가능</span>
<span style="color: #008800; font-weight: bold">from</span> <span style="color: #0e84b5; font-weight: bold">astropy.units</span> <span style="color: #008800; font-weight: bold">import</span> fa
<span style="color: #008800; font-weight: bold">from</span> <span style="color: #0e84b5; font-weight: bold">astropy.io.misc.yaml</span> <span style="color: #008800; font-weight: bold">import</span> name

a <span style="color: #333333">=</span> [<span style="color: #0000DD; font-weight: bold">1</span>,<span style="color: #0000DD; font-weight: bold">2</span>,<span style="color: #0000DD; font-weight: bold">3</span>]
<span style="color: #008800; font-weight: bold">print</span>(a, <span style="color: #007020">type</span>(a))

b <span style="color: #333333">=</span> [<span style="color: #0000DD; font-weight: bold">10</span>, a, <span style="color: #6600EE; font-weight: bold">30.5</span>, <span style="color: #007020">True</span>, <span style="background-color: #fff0f0">&#39;컴퓨터&#39;</span>]
<span style="color: #008800; font-weight: bold">print</span>(b, <span style="color: #007020">type</span>(b))

<span style="color: #008800; font-weight: bold">print</span>()
family <span style="color: #333333">=</span> [<span style="background-color: #fff0f0">&#39;엄마&#39;</span>, <span style="background-color: #fff0f0">&#39;아빠&#39;</span>, <span style="background-color: #fff0f0">&#39;나&#39;</span>, <span style="background-color: #fff0f0">&#39;여동생&#39;</span>]
family<span style="color: #333333">.</span>append(<span style="background-color: #fff0f0">&#39;남동생&#39;</span>)    <span style="color: #888888"># 리스트 추가</span>
family<span style="color: #333333">.</span>insert(<span style="color: #0000DD; font-weight: bold">0</span>, <span style="background-color: #fff0f0">&#39;할아버지&#39;</span>)    <span style="color: #888888"># 위치 삽입</span>
family<span style="color: #333333">.</span>extend([<span style="background-color: #fff0f0">&#39;삼촌&#39;</span>, <span style="background-color: #fff0f0">&#39;조카&#39;</span>])
family <span style="color: #333333">+=</span> [<span style="background-color: #fff0f0">&#39;이모&#39;</span>, <span style="background-color: #fff0f0">&#39;고모&#39;</span>]
family<span style="color: #333333">.</span>remove(<span style="background-color: #fff0f0">&#39;나&#39;</span>)  <span style="color: #888888"># 삭제</span>
<span style="color: #008800; font-weight: bold">del</span> family[<span style="color: #0000DD; font-weight: bold">1</span>]   <span style="color: #888888"># 인덱스 삭제</span>
<span style="color: #008800; font-weight: bold">print</span>(family, <span style="color: #007020">len</span>(family))
<span style="color: #008800; font-weight: bold">print</span>(family<span style="color: #333333">.</span>index(<span style="background-color: #fff0f0">&#39;남동생&#39;</span>))  <span style="color: #888888"># 특정 항목 위치 찾기</span>

<span style="color: #008800; font-weight: bold">print</span>()
aa2 <span style="color: #333333">=</span> [<span style="background-color: #fff0f0">&#39;123&#39;</span>,<span style="background-color: #fff0f0">&#39;34&#39;</span>,<span style="background-color: #fff0f0">&#39;234&#39;</span>]
<span style="color: #008800; font-weight: bold">print</span>(aa2)
aa2<span style="color: #333333">.</span>sort()
<span style="color: #008800; font-weight: bold">print</span>(aa2)
aa2<span style="color: #333333">.</span>sort(key<span style="color: #333333">=</span><span style="color: #007020">int</span>)
<span style="color: #008800; font-weight: bold">print</span>(aa2)

<span style="color: #008800; font-weight: bold">print</span>()
aaa<span style="color: #333333">=</span>[<span style="color: #0000DD; font-weight: bold">3</span>,<span style="color: #0000DD; font-weight: bold">1</span>,<span style="color: #0000DD; font-weight: bold">5</span>,<span style="color: #0000DD; font-weight: bold">2</span>,<span style="color: #0000DD; font-weight: bold">4</span>]
aaa<span style="color: #333333">.</span>sort()
<span style="color: #008800; font-weight: bold">print</span>(aaa)
aaa<span style="color: #333333">.</span>sort(reverse <span style="color: #333333">=</span> <span style="color: #007020">True</span>)
<span style="color: #008800; font-weight: bold">print</span>(aaa)

<span style="color: #008800; font-weight: bold">print</span>(<span style="background-color: #fff0f0">&#39;---&#39;</span> <span style="color: #333333">*</span> <span style="color: #0000DD; font-weight: bold">5</span>)
name <span style="color: #333333">=</span> [<span style="background-color: #fff0f0">&#39;tom&#39;</span>,<span style="background-color: #fff0f0">&#39;james&#39;</span>,<span style="background-color: #fff0f0">&#39;oscar&#39;</span>]
name2 <span style="color: #333333">=</span> name    <span style="color: #888888"># 주소 치환, 얕은 복사</span>
<span style="color: #008800; font-weight: bold">print</span>(name, <span style="color: #007020">id</span>(name))
<span style="color: #008800; font-weight: bold">print</span>(name2, <span style="color: #007020">id</span>(name2))
name[<span style="color: #0000DD; font-weight: bold">0</span>] <span style="color: #333333">=</span> <span style="background-color: #fff0f0">&#39;paul&#39;</span>
<span style="color: #008800; font-weight: bold">print</span>(name, <span style="background-color: #fff0f0">&#39; &#39;</span>, name2)

<span style="color: #008800; font-weight: bold">print</span>()
<span style="color: #008800; font-weight: bold">import</span> <span style="color: #0e84b5; font-weight: bold">copy</span>
name3 <span style="color: #333333">=</span> copy<span style="color: #333333">.</span>deepcopy(name)     <span style="color: #888888"># 깊은 복사, 완전 별개의 list가됨</span>
name3[<span style="color: #0000DD; font-weight: bold">1</span>] <span style="color: #333333">=</span> <span style="background-color: #fff0f0">&#39;john&#39;</span>
<span style="color: #008800; font-weight: bold">print</span>(name, <span style="background-color: #fff0f0">&#39; &#39;</span>, name3)

<span style="color: #008800; font-weight: bold">print</span>()
sbs <span style="color: #333333">=</span> [<span style="color: #0000DD; font-weight: bold">10</span>, <span style="color: #0000DD; font-weight: bold">20</span>, <span style="color: #0000DD; font-weight: bold">30</span>]
sbs<span style="color: #333333">.</span>append(<span style="color: #0000DD; font-weight: bold">40</span>)
<span style="color: #008800; font-weight: bold">print</span>(sbs)
sbs<span style="color: #333333">.</span>pop()   <span style="color: #888888"># stack 구조 : LIFO</span>
<span style="color: #008800; font-weight: bold">print</span>(sbs)

<span style="color: #008800; font-weight: bold">print</span>()
sbs <span style="color: #333333">=</span> [<span style="color: #0000DD; font-weight: bold">10</span>, <span style="color: #0000DD; font-weight: bold">20</span>, <span style="color: #0000DD; font-weight: bold">30</span>]
sbs<span style="color: #333333">.</span>append(<span style="color: #0000DD; font-weight: bold">40</span>)
<span style="color: #008800; font-weight: bold">print</span>(sbs)
sbs<span style="color: #333333">.</span>pop(<span style="color: #0000DD; font-weight: bold">0</span>)  <span style="color: #888888"># queue 구조 : FIFO</span>
<span style="color: #008800; font-weight: bold">print</span>(sbs)
</pre></div>






 
