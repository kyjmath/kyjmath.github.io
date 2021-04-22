---
layout: post
comments: true
title : New start
categories: [Projects]
---

<!-- HTML generated using hilite.me --><div style="background: #202020; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #999999; font-style: italic"># 집합형 자료 형 중 list type : 순서가 있고, 요소값 수정 가능</span>
<span style="color: #6ab825; font-weight: bold">from</span> <span style="color: #447fcf; text-decoration: underline">astropy.units</span> <span style="color: #6ab825; font-weight: bold">import</span> <span style="color: #d0d0d0">fa</span>
<span style="color: #6ab825; font-weight: bold">from</span> <span style="color: #447fcf; text-decoration: underline">astropy.io.misc.yaml</span> <span style="color: #6ab825; font-weight: bold">import</span> <span style="color: #d0d0d0">name</span>

<span style="color: #d0d0d0">a</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #3677a9">1</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">2</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">3</span><span style="color: #d0d0d0">]</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(a,</span> <span style="color: #24909d">type</span><span style="color: #d0d0d0">(a))</span>

<span style="color: #d0d0d0">b</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #3677a9">10</span><span style="color: #d0d0d0">,</span> <span style="color: #d0d0d0">a,</span> <span style="color: #3677a9">30.5</span><span style="color: #d0d0d0">,</span> <span style="color: #24909d">True</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;컴퓨터&#39;</span><span style="color: #d0d0d0">]</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(b,</span> <span style="color: #24909d">type</span><span style="color: #d0d0d0">(b))</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #d0d0d0">family</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #ed9d13">&#39;엄마&#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;아빠&#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;나&#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;여동생&#39;</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">family.append(</span><span style="color: #ed9d13">&#39;남동생&#39;</span><span style="color: #d0d0d0">)</span>    <span style="color: #999999; font-style: italic"># 리스트 추가</span>
<span style="color: #d0d0d0">family.insert(</span><span style="color: #3677a9">0</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;할아버지&#39;</span><span style="color: #d0d0d0">)</span>    <span style="color: #999999; font-style: italic"># 위치 삽입</span>
<span style="color: #d0d0d0">family.extend([</span><span style="color: #ed9d13">&#39;삼촌&#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;조카&#39;</span><span style="color: #d0d0d0">])</span>
<span style="color: #d0d0d0">family</span> <span style="color: #d0d0d0">+=</span> <span style="color: #d0d0d0">[</span><span style="color: #ed9d13">&#39;이모&#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #ed9d13">&#39;고모&#39;</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">family.remove(</span><span style="color: #ed9d13">&#39;나&#39;</span><span style="color: #d0d0d0">)</span>  <span style="color: #999999; font-style: italic"># 삭제</span>
<span style="color: #6ab825; font-weight: bold">del</span> <span style="color: #d0d0d0">family[</span><span style="color: #3677a9">1</span><span style="color: #d0d0d0">]</span>   <span style="color: #999999; font-style: italic"># 인덱스 삭제</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(family,</span> <span style="color: #24909d">len</span><span style="color: #d0d0d0">(family))</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(family.index(</span><span style="color: #ed9d13">&#39;남동생&#39;</span><span style="color: #d0d0d0">))</span>  <span style="color: #999999; font-style: italic"># 특정 항목 위치 찾기</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #d0d0d0">aa2</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #ed9d13">&#39;123&#39;</span><span style="color: #d0d0d0">,</span><span style="color: #ed9d13">&#39;34&#39;</span><span style="color: #d0d0d0">,</span><span style="color: #ed9d13">&#39;234&#39;</span><span style="color: #d0d0d0">]</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(aa2)</span>
<span style="color: #d0d0d0">aa2.sort()</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(aa2)</span>
<span style="color: #d0d0d0">aa2.sort(key=</span><span style="color: #24909d">int</span><span style="color: #d0d0d0">)</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(aa2)</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #d0d0d0">aaa=[</span><span style="color: #3677a9">3</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">1</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">5</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">2</span><span style="color: #d0d0d0">,</span><span style="color: #3677a9">4</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">aaa.sort()</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(aaa)</span>
<span style="color: #d0d0d0">aaa.sort(reverse</span> <span style="color: #d0d0d0">=</span> <span style="color: #24909d">True</span><span style="color: #d0d0d0">)</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(aaa)</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(</span><span style="color: #ed9d13">&#39;---&#39;</span> <span style="color: #d0d0d0">*</span> <span style="color: #3677a9">5</span><span style="color: #d0d0d0">)</span>
<span style="color: #d0d0d0">name</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #ed9d13">&#39;tom&#39;</span><span style="color: #d0d0d0">,</span><span style="color: #ed9d13">&#39;james&#39;</span><span style="color: #d0d0d0">,</span><span style="color: #ed9d13">&#39;oscar&#39;</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">name2</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">name</span>    <span style="color: #999999; font-style: italic"># 주소 치환, 얕은 복사</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(name,</span> <span style="color: #24909d">id</span><span style="color: #d0d0d0">(name))</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(name2,</span> <span style="color: #24909d">id</span><span style="color: #d0d0d0">(name2))</span>
<span style="color: #d0d0d0">name[</span><span style="color: #3677a9">0</span><span style="color: #d0d0d0">]</span> <span style="color: #d0d0d0">=</span> <span style="color: #ed9d13">&#39;paul&#39;</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(name,</span> <span style="color: #ed9d13">&#39; &#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #d0d0d0">name2)</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #6ab825; font-weight: bold">import</span> <span style="color: #447fcf; text-decoration: underline">copy</span>
<span style="color: #d0d0d0">name3</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">copy.deepcopy(name)</span>     <span style="color: #999999; font-style: italic"># 깊은 복사, 완전 별개의 list가됨</span>
<span style="color: #d0d0d0">name3[</span><span style="color: #3677a9">1</span><span style="color: #d0d0d0">]</span> <span style="color: #d0d0d0">=</span> <span style="color: #ed9d13">&#39;john&#39;</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(name,</span> <span style="color: #ed9d13">&#39; &#39;</span><span style="color: #d0d0d0">,</span> <span style="color: #d0d0d0">name3)</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #d0d0d0">sbs</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #3677a9">10</span><span style="color: #d0d0d0">,</span> <span style="color: #3677a9">20</span><span style="color: #d0d0d0">,</span> <span style="color: #3677a9">30</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">sbs.append(</span><span style="color: #3677a9">40</span><span style="color: #d0d0d0">)</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(sbs)</span>
<span style="color: #d0d0d0">sbs.pop()</span>   <span style="color: #999999; font-style: italic"># stack 구조 : LIFO</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(sbs)</span>

<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">()</span>
<span style="color: #d0d0d0">sbs</span> <span style="color: #d0d0d0">=</span> <span style="color: #d0d0d0">[</span><span style="color: #3677a9">10</span><span style="color: #d0d0d0">,</span> <span style="color: #3677a9">20</span><span style="color: #d0d0d0">,</span> <span style="color: #3677a9">30</span><span style="color: #d0d0d0">]</span>
<span style="color: #d0d0d0">sbs.append(</span><span style="color: #3677a9">40</span><span style="color: #d0d0d0">)</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(sbs)</span>
<span style="color: #d0d0d0">sbs.pop(</span><span style="color: #3677a9">0</span><span style="color: #d0d0d0">)</span>  <span style="color: #999999; font-style: italic"># queue 구조 : FIFO</span>
<span style="color: #6ab825; font-weight: bold">print</span><span style="color: #d0d0d0">(sbs)</span>
</pre></div>







 
