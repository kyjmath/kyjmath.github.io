---
layout: post
comments: true
title : CGI Network [KOR]
categories: [Practice]
---

<body>

<img src="https://kyjmath.github.io/assets/Emogi/cgi1.png" width="70%" height=auto>
<img src="https://kyjmath.github.io/assets/Emogi/cgi2.jpg" width="25%" height=auto>
<br><br>

<b>network_cgi.py</b> : CGI 네트워크를 오픈한다<br>
<b>CGI</b> : 웹 서버와 클라이언트 사이에서 정보를 주고 받는 방법이나 규약, 대화형 웹 페이지를 운영한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; padding: 0.5em; background: rgb(255, 255, 255); color: rgb(0, 0, 0);"><span class="hljs-keyword" style="color: rgb(0, 0, 255);">from</span> http.server <span class="hljs-keyword" style="color: rgb(0, 0, 255);">import</span> CGIHTTPRequestHandler, HTTPServer
port = <span class="hljs-number">8888</span>

<span class="hljs-class"><span class="hljs-keyword" style="color: rgb(0, 0, 255);">class</span> <span class="hljs-title" style="color: rgb(163, 21, 21);">Handler</span><span class="hljs-params">(CGIHTTPRequestHandler)</span>:</span>
    cgi_directories = [<span class="hljs-string" style="color: rgb(163, 21, 21);">'/cgi-bin'</span>]  <span class="hljs-comment" style="color: green;"># 경로 설정, 폴더이름은 무조건 cgi-bin 으로 해야한다.</span>
    
serv = HTTPServer((<span class="hljs-string" style="color: rgb(163, 21, 21);">'127.0.0.1'</span>, port), Handler)
print(<span class="hljs-string" style="color: rgb(163, 21, 21);">'웹 서비스 시작...'</span>)
serv.serve_forever()</pre>
</span>
<br><br>

<b>main.html</b> : 메인화면을 담당한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; padding: 0.5em; background: rgb(251, 241, 199); color: rgb(60, 56, 54);"><span class="hljs-meta" style="color: rgb(175, 58, 3);">&lt;!DOCTYPE html&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">html</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">head</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">meta</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">charset</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"UTF-8"</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">title</span>&gt;</span>메인 페이지<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">title</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">head</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">body</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">h1</span>&gt;</span>여기가 메인 홈페이지<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">h1</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">ol</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">href</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"cgi-bin/hello.py"</span>&gt;</span>hello 파이썬 문서 요청<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span>  <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;">&lt;!-- 파이썬 부르기 --&gt;</span>
	<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">href</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"cgi-bin/world.py"</span>&gt;</span>world 파이썬 문서 요청<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">href</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"cgi-bin/my.py?name=tom&amp;age=23"</span>&gt;</span>my(get 방식으로 자료 전달)<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">href</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"friend.html"</span>&gt;</span>친구자료 입력<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span>
	<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span> <span class="hljs-attr" style="color: rgb(181, 118, 20);">href</span>=<span class="hljs-string" style="color: rgb(121, 116, 14);">"cgi-bin/sangpum.py"</span>&gt;</span>상품 자료<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">a</span>&gt;</span><span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">li</span>&gt;</span>  <span class="hljs-comment" style="color: rgb(146, 131, 116); font-style: italic;">&lt;!-- db 연동해서 부를거임 --&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">ol</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">body</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(66, 123, 88); font-weight: 700;">&lt;/<span class="hljs-name" style="color: rgb(7, 102, 120);">html</span>&gt;</span></pre>
</span>
<br><br>

<b>hello.py</b> : 여기서는 파이썬으로 처리한 내용을 클라이언트에게 전송한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(244, 251, 244); color: rgb(94, 110, 94); padding: 0.5em;">munja = <span class="hljs-string" style="color: rgb(41, 163, 41);">'파이썬 변수에 값 기억'</span>
kor = <span class="hljs-number" style="color: rgb(135, 113, 29);">50</span>
eng = <span class="hljs-number" style="color: rgb(135, 113, 29);">40</span>
hap = kor + eng

print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'Content-Type:text/html;charset=utf-8\n'</span>)  <span class="hljs-comment" style="color: rgb(104, 125, 104);"># 웹용 파이썬</span>
print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'&lt;html&gt;&lt;body&gt;'</span>)

print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'&lt;b&gt;안녕하세요&lt;/b&gt;강영진의 파이썬 문서입니다&lt;br&gt;'</span>)
print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'내 이름은 강영진 입니다&lt;br&gt;'</span>)
print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'minja : %s hap : %d'</span>%(munja, hap))  <span class="hljs-comment" style="color: rgb(104, 125, 104);"># 파이썬 변수도 웹으로 출력 가능</span>

print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'&lt;/body&gt;&lt;/html&gt;'</span>)</pre>
</span>
<br><br>

<b>world.py</b> : 여기서도 파이썬으로 처리한 내용을 클라이언트에게 전송한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(244, 251, 244); color: rgb(94, 110, 94); padding: 0.5em;">s1 = <span class="hljs-string" style="color: rgb(41, 163, 41);">'자료1'</span>
s2 = <span class="hljs-string" style="color: rgb(41, 163, 41);">'강영진'</span>

print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'Content-Type:text/html;charset=utf-8\n'</span>)  <span class="hljs-comment" style="color: rgb(104, 125, 104);"># 웹용 파이썬</span>
print(<span class="hljs-string" style="color: rgb(41, 163, 41);">"""
&lt;html&gt;
&lt;body&gt;
&lt;h1&gt; 난 월드 &lt;/h1&gt;
파이썬 값 출력 : {0}, {1} &lt;br&gt;
&lt;a href='../main.html'&gt;메인으로&lt;/a&gt;
&lt;/body&gt;
&lt;/html&gt;
"""</span>.format(s1, s2))</pre>
</span>
<br><br>

<b>my.py</b> : client가 넘겨준 정보를 수신한다 (name = tom, age = 23)<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(244, 251, 244); color: rgb(94, 110, 94); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(173, 43, 238);">import</span> cgi

form = cgi.FieldStorage()  <span class="hljs-comment" style="color: rgb(104, 125, 104);"># name=tom&amp;age=23 이부분을 가져온다</span>

irum = form[<span class="hljs-string" style="color: rgb(41, 163, 41);">'name'</span>].value
nai = form[<span class="hljs-string" style="color: rgb(41, 163, 41);">'age'</span>].value + <span class="hljs-string" style="color: rgb(41, 163, 41);">'살'</span>

print(<span class="hljs-string" style="color: rgb(41, 163, 41);">'Content-Type:text/html;charset=utf-8\n'</span>)  <span class="hljs-comment" style="color: rgb(104, 125, 104);"># 웹용 파이썬</span>
print(<span class="hljs-string" style="color: rgb(41, 163, 41);">"""
&lt;html&gt;
&lt;body&gt;
넘겨준 자료 보기&lt;br&gt;
이름은 : {0}, 나이는 : {1}
&lt;/body&gt;
&lt;/html&gt;
"""</span>.format(irum, nai))</pre>
</span>
<br><br>

<b>friend.html</b> : friend.py 에게 넘겨줄 입력값을 받는 폼 html<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(241, 239, 238); color: rgb(104, 97, 94); padding: 0.5em;"><span class="hljs-meta" style="color: rgb(223, 83, 32);">&lt;!DOCTYPE html&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">html</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">head</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">meta</span> <span class="hljs-attr">charset</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"UTF-8"</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">title</span>&gt;</span>Insert title here<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;/<span class="hljs-name" style="color: rgb(242, 44, 64);">title</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;/<span class="hljs-name" style="color: rgb(242, 44, 64);">head</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">body</span>&gt;</span>

** 친구 자료 ** <span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">br</span>&gt;</span>
<span class="hljs-comment" style="color: rgb(118, 110, 107);">&lt;!-- 입력 폼 이용 --&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">form</span> <span class="hljs-attr">action</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"cgi-bin/friend.py"</span> <span class="hljs-attr">method</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"get"</span>&gt;</span> <span class="hljs-comment" style="color: rgb(118, 110, 107);">&lt;!-- get 대신 post를 쓰면 보안이 유지가 된다 (위에 value가 안뜬다) --&gt;</span> 
이름 : <span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"text"</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"name"</span>&gt;</span><span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">br</span>&gt;</span>
전화 : <span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"text"</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"phone"</span>&gt;</span><span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">br</span>&gt;</span>
성별 : 
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"radio"</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"gen"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"남"</span> <span class="hljs-attr">checked</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"checked"</span>&gt;</span>남자
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"radio"</span> <span class="hljs-attr">name</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"gen"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"여"</span>&gt;</span>여자
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">br</span>&gt;</span><span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">br</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;<span class="hljs-name" style="color: rgb(242, 44, 64);">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"submit"</span> <span class="hljs-attr">value</span>=<span class="hljs-string" style="color: rgb(123, 151, 38);">"전송"</span>&gt;</span>  <span class="hljs-comment" style="color: rgb(118, 110, 107);">&lt;!-- button 이 아니라 submit 이라 해야 작동을 한다, 누르면 action 발동 --&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;/<span class="hljs-name" style="color: rgb(242, 44, 64);">form</span>&gt;</span>

<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;/<span class="hljs-name" style="color: rgb(242, 44, 64);">body</span>&gt;</span>
<span class="hljs-tag" style="color: rgb(242, 44, 64);">&lt;/<span class="hljs-name" style="color: rgb(242, 44, 64);">html</span>&gt;</span></pre>
</span>
<br>

<b>friend.py</b> : friend.html 에게 넘겨받은 값으로 클라이언트에게 반환한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(85, 133, 155);">import</span> cgi

form = cgi.FieldStorage()  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># name=tom&amp;age=23 이부분을 가져온다</span>

name = form[<span class="hljs-string" style="color: rgb(72, 153, 99);">'name'</span>].value  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># friend.html 에서 값 받아오기</span>
phone = form[<span class="hljs-string" style="color: rgb(72, 153, 99);">'phone'</span>].value
gender = form[<span class="hljs-string" style="color: rgb(72, 153, 99);">'gen'</span>].value

print(<span class="hljs-string" style="color: rgb(72, 153, 99);">'Content-Type:text/html;charset=utf-8\n'</span>)  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># 웹용 파이썬</span>
print(<span class="hljs-string" style="color: rgb(72, 153, 99);">"""
&lt;html&gt;
&lt;body&gt;
넘겨준 자료 보기&lt;br&gt;
이름은 : {0}, 전화는 : {1}, 성별은 : {2}
&lt;/body&gt;
&lt;/html&gt;
"""</span>.format(name, phone, gender))
</pre></span>
<br><br>

<b>sangpum.py</b> : MariaDB와 연동하여 상품 테이블을 클라이언트에게 반환한다<br>

<span style="font-size:15px;">
<pre class="hljs" style="display: block; overflow-x: auto; background: rgb(236, 244, 238); color: rgb(82, 96, 87); padding: 0.5em;"><span class="hljs-keyword" style="color: rgb(85, 133, 155);">import</span> MySQLdb
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">import</span> ast  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># sting 파일을 dict로 읽는다</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">import</span> os

<span class="hljs-comment" style="color: rgb(95, 109, 100);"># 주소 파일 읽어오기</span>
<span class="hljs-keyword" style="color: rgb(85, 133, 155);">with</span> open(os.getcwd() + <span class="hljs-string" style="color: rgb(72, 153, 99);">'\\mariadb.txt'</span>, <span class="hljs-string" style="color: rgb(72, 153, 99);">'r'</span>) <span class="hljs-keyword" style="color: rgb(85, 133, 155);">as</span> f:  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># os.getcwd() 를 통해 파일위치를 찾는다</span>
    config = ast.literal_eval(f.read())

print(<span class="hljs-string" style="color: rgb(72, 153, 99);">'Content-Type:text/html;charset=utf-8\n'</span>)  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># 웹용 파이썬</span>
print(<span class="hljs-string" style="color: rgb(72, 153, 99);">"""
&lt;html&gt;
&lt;body&gt;
&lt;b&gt;상품 정보&lt;/b&gt;
&lt;table border = "1"&gt;
&lt;tr&gt;&lt;th&gt;코드&lt;/th&gt;&lt;th&gt;상품명&lt;/th&gt;&lt;th&gt;수량&lt;/th&gt;&lt;th&gt;단가&lt;/th&gt;&lt;/tr&gt;
"""</span>)

<span class="hljs-keyword" style="color: rgb(85, 133, 155);">try</span>:
    conn = MySQLdb.connect(**config)
    cursor = conn.cursor()
    cursor.execute(<span class="hljs-string" style="color: rgb(72, 153, 99);">"select * from sangdata"</span>)
    datas = cursor.fetchall()
    <span class="hljs-keyword" style="color: rgb(85, 133, 155);">for</span> code, sang,su,dan <span class="hljs-keyword" style="color: rgb(85, 133, 155);">in</span> datas:  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># html 문에 넣어준다</span>
        print(<span class="hljs-string" style="color: rgb(72, 153, 99);">"""
        &lt;tr&gt;
        &lt;td&gt;{0}&lt;/td&gt;
        &lt;td&gt;{1}&lt;/td&gt;
        &lt;td&gt;{2}&lt;/td&gt;
        &lt;td&gt;{3}&lt;/td&gt;
        &lt;/tr&gt;
        """</span>.format(str(code), sang, su, dan))

<span class="hljs-keyword" style="color: rgb(85, 133, 155);">except</span> Exception <span class="hljs-keyword" style="color: rgb(85, 133, 155);">as</span> e:
    print(<span class="hljs-string" style="color: rgb(72, 153, 99);">'오류 : '</span>, e)

<span class="hljs-keyword" style="color: rgb(85, 133, 155);">finally</span>:
    cursor.close()
    conn.close()
    
print(<span class="hljs-string" style="color: rgb(72, 153, 99);">"""
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
"""</span>)  <span class="hljs-comment" style="color: rgb(95, 109, 100);"># 테이블 형식으로 출력, border="1" 은 테두리를 생성한다.</span></pre>
</span>
<br><br>

<center><span style="font-size:20px;color:navy;font-weight:bold;">최종 출력 화면</span></center>
<br>
<center><img src="https://kyjmath.github.io/assets/Emogi/CGI.gif" width="70%" height=auto></center>

</body>
