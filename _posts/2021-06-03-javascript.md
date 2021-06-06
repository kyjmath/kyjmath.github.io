---
layout: post
comments: true
title : JavaScript Basic [KOR]
categories: [Practice]
---

			
<html>									
<head>										
<meta charset="utf-8"> 						
</head>	
<body>	

<h1 style="color:navy;text-align: center;">Javascript</h1><br> 
html 에서 프로그래밍을 가능하게 하도록 한다. Ajax 기능을 제공한다.<br>

<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; padding: 0.5em; background: rgb(255, 255, 255); color: rgb(67, 79, 84);">javascript는 &lt;script type =<span class="hljs-string" style="color: rgb(0, 92, 95);">"text/javascript"</span>&gt;와 &lt;<span class="hljs-regexp" style="color: rgb(0, 151, 157);">/script&gt;사이에 작성을 한다.</span></pre></span><br><br>


javascript의 변수정의 html출력, 콘솔 출력<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"> <span class="hljs-comment" style="color: rgb(95, 109, 100);">// 변수 정의 법</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> aaa = <span class="hljs-number" style="color: rgb(159, 113, 60);">123</span>, bbb = <span class="hljs-number" style="color: rgb(159, 113, 60);">45.6</span>;

<span class="hljs-comment" style="color: rgb(95, 109, 100);">// html 출력 법</span>
<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(aa, <span class="hljs-string" style="color: rgb(72, 153, 99);">' '</span>, bb, <span class="hljs-string" style="color: rgb(72, 153, 99);">"&lt;br&gt;"</span>);

<span class="hljs-comment" style="color: rgb(95, 109, 100);">// 콘솔 출력 법</span>
<span class="hljs-built_in" style="color: rgb(159, 113, 60);">console</span>.log(aa, <span class="hljs-string" style="color: rgb(72, 153, 99);">' '</span>, bb);</pre></span><br><br>


조건 판단문 if<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> jumsu = prompt(<span class="hljs-string" style="color: rgb(72, 153, 99);">"평균 정수 입력"</span>, <span class="hljs-string" style="color: rgb(72, 153, 99);">"80"</span>)  <span class="hljs-comment" style="color: rgb(95, 109, 100);">// 키보드로 소량의 자료 입력하는 대화상자</span>

<span class="hljs-keyword" style="color: rgb(85, 133, 155);">if</span> (jumsu &gt;= <span class="hljs-number" style="color: rgb(159, 113, 60);">90</span>){
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">"&lt;br&gt;&lt;b style='font-size:30px;color:blue;'&gt;90 이상&lt;/b&gt;"</span>)
}<span class="hljs-keyword" style="color: rgb(85, 133, 155);">else</span> <span class="hljs-keyword" style="color: rgb(85, 133, 155);">if</span> (jumsu &gt;= <span class="hljs-number" style="color: rgb(159, 113, 60);">70</span>){
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;70이상'</span>);
}<span class="hljs-keyword" style="color: rgb(85, 133, 155);">else</span>{
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;70미만'</span>);
}</pre></span><br><br>


조건 판단문 switch<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> jumsu = <span class="hljs-number" style="color: rgb(159, 113, 60);">80</span>;

<span class="hljs-keyword" style="color: rgb(85, 133, 155);">switch</span> (jumsu){
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">case</span> <span class="hljs-number" style="color: rgb(159, 113, 60);">90</span>:
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;나이스'</span>);
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">break</span>;
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">case</span> <span class="hljs-number" style="color: rgb(159, 113, 60);">80</span>:
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;베리굿'</span>);
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">break</span>;
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">case</span> <span class="hljs-number" style="color: rgb(159, 113, 60);">70</span>:
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;원더풀'</span>);
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">break</span>;
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">default</span>:
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;기타'</span>);
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">break</span>;
}</pre></span><br><br>


순환문 for<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;table border="1"&gt;'</span>);
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">for</span> (<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> a = <span class="hljs-number" style="color: rgb(159, 113, 60);">2</span>; a &lt; <span class="hljs-number" style="color: rgb(159, 113, 60);">10</span>; a++){
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">if</span> (a % <span class="hljs-number" style="color: rgb(159, 113, 60);">2</span> === <span class="hljs-number" style="color: rgb(159, 113, 60);">0</span>){
		<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;tr class="my"&gt;'</span>);
	}<span class="hljs-keyword" style="color: rgb(85, 133, 155);">else</span>{
		<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;tr&gt;'</span>);
	}
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">for</span> (<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> b = <span class="hljs-number" style="color: rgb(159, 113, 60);">1</span>; b &lt; <span class="hljs-number" style="color: rgb(159, 113, 60);">10</span>; b++){
		<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;td&gt;'</span>);
		<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(a + <span class="hljs-string" style="color: rgb(72, 153, 99);">"*"</span> + b + <span class="hljs-string" style="color: rgb(72, 153, 99);">"="</span> + a * b);
		<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;/td&gt;'</span>);
	}
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;/tr&gt;'</span>);</pre></span><br><br>

순환문 while<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(85, 133, 155);">while</span> (k &lt;= <span class="hljs-number" style="color: rgb(159, 113, 60);">10</span>){
	k++;
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">if</span>(k === <span class="hljs-number" style="color: rgb(159, 113, 60);">3</span> || k === <span class="hljs-number" style="color: rgb(159, 113, 60);">5</span>) <span class="hljs-keyword" style="color: rgb(85, 133, 155);">continue</span>;  <span class="hljs-comment" style="color: rgb(95, 109, 100);">// ||는 and</span>
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(k + <span class="hljs-string" style="color: rgb(72, 153, 99);">' '</span>);
	<span class="hljs-keyword" style="color: rgb(85, 133, 155);">if</span> (k === <span class="hljs-number" style="color: rgb(159, 113, 60);">7</span>) <span class="hljs-keyword" style="color: rgb(85, 133, 155);">break</span>;
}
<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">'&lt;br&gt;'</span>);</pre></span><br><br>


array (python의 list)


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-comment" style="color: rgb(95, 109, 100);">// array 정의</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> cc = <span class="hljs-keyword" style="color: rgb(85, 133, 155);">new</span> <span class="hljs-built_in" style="color: rgb(159, 113, 60);">Array</span>();

<span class="hljs-comment" style="color: rgb(95, 109, 100);">// array에 원소 집어넣기</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">for</span> (<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> k = <span class="hljs-number" style="color: rgb(159, 113, 60);">0</span>; k &lt; <span class="hljs-number" style="color: rgb(159, 113, 60);">10</span>; k++){
	cc[k] = k + <span class="hljs-number" style="color: rgb(159, 113, 60);">1</span>;
}

<span class="hljs-comment" style="color: rgb(95, 109, 100);">// array 원소 출력</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">for</span> (<span class="hljs-keyword" style="color: rgb(85, 133, 155);">let</span> m = <span class="hljs-number" style="color: rgb(159, 113, 60);">0</span>; m &lt; cc.length; m++){
	<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(m + <span class="hljs-string" style="color: rgb(72, 153, 99);">" "</span>);
}
<span class="hljs-built_in" style="color: rgb(159, 113, 60);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 153, 99);">"&lt;br&gt;"</span>);</pre></span><br><br>


내장 함수<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(231, 233, 219); color: rgb(79, 66, 76); padding: 0.5em;"><span class="hljs-comment" style="color: rgb(119, 110, 113);">//문자 함수</span>
<span class="hljs-keyword" style="color: rgb(129, 91, 164);">let</span> str = <span class="hljs-string" style="color: rgb(72, 182, 133);">"javascript language"</span>;
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(str.charAt(<span class="hljs-number" style="color: rgb(249, 155, 21);">2</span>));      <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 문자의 3번째 요소 반환</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(str.indexOf(<span class="hljs-string" style="color: rgb(72, 182, 133);">"v"</span>));   <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 문자에서 v의 위치 반환</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(str.toLowerCase());  <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 문자를 소문자로 변환</span>

<span class="hljs-comment" style="color: rgb(119, 110, 113);">// 스타일 함수</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(tr.bold().fontcolor(<span class="hljs-string" style="color: rgb(72, 182, 133);">'#ff0000'</span>).fontsize(<span class="hljs-number" style="color: rgb(249, 155, 21);">20</span>));
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(str.strike().italics());

<span class="hljs-comment" style="color: rgb(119, 110, 113);">// 수학 함수</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(<span class="hljs-built_in" style="color: rgb(249, 155, 21);">Math</span>.abs(<span class="hljs-number" style="color: rgb(249, 155, 21);">-7</span>));    <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 절대값</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(<span class="hljs-built_in" style="color: rgb(249, 155, 21);">Math</span>.round(<span class="hljs-number" style="color: rgb(249, 155, 21);">3.6</span>)); <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 소숫점 반올림</span>
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(<span class="hljs-built_in" style="color: rgb(249, 155, 21);">Math</span>.random());   <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 0부터 1까지 랜덤 실수 반환</span>

<span class="hljs-comment" style="color: rgb(119, 110, 113);">// 날짜 함수</span>
<span class="hljs-keyword" style="color: rgb(129, 91, 164);">let</span> d = <span class="hljs-keyword" style="color: rgb(129, 91, 164);">new</span> <span class="hljs-built_in" style="color: rgb(249, 155, 21);">Date</span>();
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(d);
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(d.getFullYear() + <span class="hljs-string" style="color: rgb(72, 182, 133);">" "</span> + d.getMonth() + <span class="hljs-string" style="color: rgb(72, 182, 133);">" "</span> + d.getMonth() + <span class="hljs-string" style="color: rgb(72, 182, 133);">" "</span> + 
		d.getDate() + <span class="hljs-string" style="color: rgb(72, 182, 133);">" "</span> + d.getHours());</pre></span><br><br>


정의 함수<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(231, 233, 219); color: rgb(79, 66, 76); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(129, 91, 164);">let</span> count = <span class="hljs-number" style="color: rgb(249, 155, 21);">0</span>;
<span class="hljs-function"><span class="hljs-keyword" style="color: rgb(129, 91, 164);">function</span> <span class="hljs-title" style="color: rgb(254, 196, 24);">aa</span>(<span class="hljs-params" style="color: rgb(249, 155, 21);"></span>)</span>{
	count += <span class="hljs-number" style="color: rgb(249, 155, 21);">1</span>;
	<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(count + <span class="hljs-string" style="color: rgb(72, 182, 133);">"코드의 재활용이 목적&lt;br&gt;"</span>);
};
aa();  <span class="hljs-comment" style="color: rgb(119, 110, 113);">// 함수 실행</span>

<span class="hljs-comment" style="color: rgb(119, 110, 113);">//화살표 함수 : 모던 자바스크립트에서 지원</span>
<span class="hljs-keyword" style="color: rgb(129, 91, 164);">let</span> sum = (a, b) =&gt; a + b;
<span class="hljs-built_in" style="color: rgb(249, 155, 21);">document</span>.write(<span class="hljs-string" style="color: rgb(72, 182, 133);">'&lt;br&gt;'</span>, sum(<span class="hljs-number" style="color: rgb(249, 155, 21);">1</span>, <span class="hljs-number" style="color: rgb(249, 155, 21);">2</span>));</pre></span><br><br>


이벤트 처리<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-function"><span class="hljs-keyword" style="color: rgb(102, 121, 204);">function</span> <span class="hljs-title" style="color: rgb(61, 143, 209);">func</span>(<span class="hljs-params" style="color: rgb(199, 107, 41);"></span>)</span>{
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">let</span> data = prompt(<span class="hljs-string" style="color: rgb(172, 151, 57);">"날짜 입력 : "</span>, <span class="hljs-string" style="color: rgb(172, 151, 57);">"2021-5-27"</span>);
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">let</span> arrData = data.split(<span class="hljs-string" style="color: rgb(172, 151, 57);">"-"</span>);
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">let</span> y = arrData[<span class="hljs-number" style="color: rgb(199, 107, 41);">0</span>];
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">let</span> m = arrData[<span class="hljs-number" style="color: rgb(199, 107, 41);">1</span>];
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">let</span> d = arrData[<span class="hljs-number" style="color: rgb(199, 107, 41);">2</span>];
	<span class="hljs-built_in" style="color: rgb(199, 107, 41);">document</span>.write(y + <span class="hljs-string" style="color: rgb(172, 151, 57);">"년"</span> + m + <span class="hljs-string" style="color: rgb(172, 151, 57);">"월"</span> + d + <span class="hljs-string" style="color: rgb(172, 151, 57);">"일"</span>);
}
</pre><pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-comment" style="color: rgb(107, 115, 148);">&lt;!-- 이벤트 실행  --&gt;</span>
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">a</span> <span class="hljs-attr">href</span> = <span class="hljs-string" style="color: rgb(172, 151, 57);">"javascript:func();"</span>&gt;</span>이벤트 처리 1<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">a</span>&gt;</span>

<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">a</span> <span class="hljs-attr">href</span> = <span class="hljs-string" style="color: rgb(172, 151, 57);">"javascript:;"</span> <span class="hljs-attr">onclick</span> = <span class="hljs-string" style="color: rgb(172, 151, 57);">"func()"</span>&gt;</span>이벤트 처리 2<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">a</span>&gt;</span>

<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">button</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"func()"</span>&gt;</span>이벤트 처리 3<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">button</span>&gt;</span>

<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">'button'</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"func()"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"이벤트 처리 4"</span>&gt;</span>
}
</pre></span><br><br>


외부 css, javascript 불러오기<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">link</span> <span class="hljs-attr">rel</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"stylesheet"</span> <span class="hljs-attr">href</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"css폴더위치/css파일명.css"</span>&gt;</span> 
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">script</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"text/javascript"</span> <span class="hljs-attr">src</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"js폴더위치/js파일명.js"</span>&gt;</span><span class="undefined"></span><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">script</span>&gt;</span>  </pre></span><br><br>
							

window.onload : 클라이언트가 웹서버에게 html문서를 요청해서 그 결과가 모두 수신되면 자동발생되는 이벤트<br>

<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-built_in" style="color: rgb(199, 107, 41);">window</span>.onload = <span class="hljs-function"><span class="hljs-keyword" style="color: rgb(102, 121, 204);">function</span>(<span class="hljs-params" style="color: rgb(199, 107, 41);"></span>)</span>{
	<span class="hljs-built_in" style="color: rgb(199, 107, 41);">document</span>.getElementById(<span class="hljs-string" style="color: rgb(172, 151, 57);">"btn1"</span>).onclick=<span class="hljs-function"><span class="hljs-keyword" style="color: rgb(102, 121, 204);">function</span>(<span class="hljs-params" style="color: rgb(199, 107, 41);"></span>)</span>{
		<span class="hljs-built_in" style="color: rgb(199, 107, 41);">document</span>.getElementById(<span class="hljs-string" style="color: rgb(172, 151, 57);">"show"</span>).innerHTML=<span class="hljs-string" style="color: rgb(172, 151, 57);">"클릭1 선택"</span>;
	}</pre><pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"button"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"클릭1"</span> <span class="hljs-attr">id</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"btn1"</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">div</span> <span class="hljs-attr">id</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"show"</span>&gt;</span>결과 출력 지역<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">div</span>&gt;</span></pre></span><br><br>


form<br>


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-built_in" style="color: rgb(199, 107, 41);">window</span>.onload = <span class="hljs-function"><span class="hljs-keyword" style="color: rgb(102, 121, 204);">function</span>(<span class="hljs-params" style="color: rgb(199, 107, 41);"></span>)</span>{
	<span class="hljs-built_in" style="color: rgb(199, 107, 41);">document</span>.getElementById(<span class="hljs-string" style="color: rgb(172, 151, 57);">"btnSend"</span>).onclick = chkData;
}

<span class="hljs-function"><span class="hljs-keyword" style="color: rgb(102, 121, 204);">function</span> <span class="hljs-title" style="color: rgb(61, 143, 209);">chkData</span>(<span class="hljs-params" style="color: rgb(199, 107, 41);"></span>)</span>{
	<span class="hljs-keyword" style="color: rgb(102, 121, 204);">if</span> (frm.name.value ===<span class="hljs-string" style="color: rgb(172, 151, 57);">""</span> || <span class="hljs-built_in" style="color: rgb(199, 107, 41);">isNaN</span>(frm.name.value) == <span class="hljs-literal" style="color: rgb(199, 107, 41);">false</span>){
		frm.name.focus();  <span class="hljs-comment" style="color: rgb(107, 115, 148);">// 커서가 frm -&gt; name 으로 간다</span>
		alert(<span class="hljs-string" style="color: rgb(172, 151, 57);">"이름을 입력하시오"</span>)
		<span class="hljs-keyword" style="color: rgb(102, 121, 204);">return</span>;
	}
}</pre><pre class="hljs" style="display: block; overflow-x: auto; background: rgb(245, 247, 255); color: rgb(94, 102, 135); padding: 0.5em;"><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">form</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"frm"</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">table</span> <span class="hljs-attr">border</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"1"</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">tr</span>&gt;</span>
		<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span>&gt;</span>이름<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span>&gt;</span>
		<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span>&gt;</span><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"text"</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"name"</span>&gt;</span><span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">tr</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">tr</span>&gt;</span>
		<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span> <span class="hljs-attr">colspan</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"2"</span> <span class="hljs-attr">style</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"text-align:center;"</span>&gt;</span>
			<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;<span class="hljs-name" style="color: rgb(201, 73, 34);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"button"</span> <span class="hljs-attr">id</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"btnSend"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(172, 151, 57);">"자료전송"</span>&gt;</span>
		<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">td</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">tr</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">table</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(201, 73, 34);">&lt;/<span class="hljs-name" style="color: rgb(201, 73, 34);">form</span>&gt;</span></pre></span><br><br>


AJAX : XML에 기반으로 하여 서버와의 통신을 비동기 방식으로 연결함으로써 시스템 자원의 불필요한 시간낭비를 줄이고, 사용자 환경은 자바스크립트가 지원하는 대화형 웹 Application을 구현한 기술이다.


<span style="font-size: 15px">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(244, 243, 236); color: rgb(95, 94, 78); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(95, 145, 130);">let</span> xhr;

<span class="hljs-function"><span class="hljs-keyword" style="color: rgb(95, 145, 130);">function</span> <span class="hljs-title" style="color: rgb(54, 161, 102);">createXhr</span>(<span class="hljs-params" style="color: rgb(174, 115, 19);"></span>)</span>{
	<span class="hljs-keyword" style="color: rgb(95, 145, 130);">if</span> (<span class="hljs-built_in" style="color: rgb(174, 115, 19);">window</span>.ActiveXObject){
		xhr = <span class="hljs-keyword" style="color: rgb(95, 145, 130);">new</span> ActiveXObject(<span class="hljs-string" style="color: rgb(125, 151, 38);">"Msxml2.XMLHTTP"</span>);  <span class="hljs-comment" style="color: rgb(108, 107, 90);">// 인터넷 익스플로러8 이하</span>
	}<span class="hljs-keyword" style="color: rgb(95, 145, 130);">else</span>{
		xhr = <span class="hljs-keyword" style="color: rgb(95, 145, 130);">new</span> XMLHttpRequest();  <span class="hljs-comment" style="color: rgb(108, 107, 90);">// AJAX 지원 클래스</span>
	}
}
</pre></span><br><br>


</body>										
</html>									
