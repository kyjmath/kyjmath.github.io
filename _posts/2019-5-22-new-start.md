---
layout: post
comments: true
title : New start
categories: [Projects]
---

```python

# 집합형 자료 형 중 list type : 순서가 있고, 요소값 수정 가능
from astropy.units import fa
from astropy.io.misc.yaml import name

a = [1,2,3]
print(a, type(a))

b = [10, a, 30.5, True, '컴퓨터']
print(b, type(b))

print()
family = ['엄마', '아빠', '나', '여동생']
family.append('남동생')    # 리스트 추가
family.insert(0, '할아버지')    # 위치 삽입
family.extend(['삼촌', '조카'])
family += ['이모', '고모']
family.remove('나')  # 삭제
del family[1]   # 인덱스 삭제
print(family, len(family))
print(family.index('남동생'))  # 특정 항목 위치 찾기

print()
aa2 = ['123','34','234']
print(aa2)
aa2.sort()
print(aa2)
aa2.sort(key=int)
print(aa2)

print()
aaa=[3,1,5,2,4]
aaa.sort()
print(aaa)
aaa.sort(reverse = True)
print(aaa)

print('---' * 5)
name = ['tom','james','oscar']
name2 = name    # 주소 치환, 얕은 복사
print(name, id(name))
print(name2, id(name2))
name[0] = 'paul'
print(name, ' ', name2)

print()
import copy
name3 = copy.deepcopy(name)     # 깊은 복사, 완전 별개의 list가됨
name3[1] = 'john'
print(name, ' ', name3)

print()
sbs = [10, 20, 30]
sbs.append(40)
print(sbs)
sbs.pop()   # stack 구조 : LIFO
print(sbs)

print()
sbs = [10, 20, 30]
sbs.append(40)
print(sbs)
sbs.pop(0)  # queue 구조 : FIFO
print(sbs)

```





 
