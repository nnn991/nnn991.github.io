---
title:  "두 정수 사이의 합"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---

# Programmers_codingTest [1]

## 문제 : 두 정수 사이의 합

## 문제설명  
두 정수 a, b가 주어졌을 때 a와 b 사이에 속한 모든 정수의 합을 리턴하는 함수, solution을 완성하세요.  
예를 들어 a = 3, b = 5인 경우, 3 + 4 + 5 = 12이므로 12를 리턴합니다.


## 제한사항
- a와 b가 같은 경우는 둘 중 아무 수나 리턴하세요.
- a와 b는 -10,000,000 이상 10,000,000 이하인 정수입니다.
- a와 b의 대소관계는 정해져있지 않습니다.


## 문제에 대한 생각
두 정수의 크기에 따라서 결과값을 구하는 방법이 달라질 수 있다는 점을 의식했다.  
if문을 이용해 3가지 경우로 나누어 계산하기로 하였다.


## 풀이
<pre>
<code>
class Solution {
    public long solution(int a, int b) {
        long answer = 0;
        int start = 0;
        int end = 0;
        
        if(a==b) {
            return a;
        } else if(a<b) {
            start = a;
            end = b;
        } else if(a>b) {
            start = b;
            end = a;
        }
        for(int i = start; i <= end; i++) {
            answer+=i;
        }
        return answer;
    }
}
</code>
</pre>
두 정수 a,b를 3가지 경우로 보았다.
- a>b인 경우  
- a<b인 경우  
- a=b인 경우  


### 출처

프로그래머스 코딩테스트 연습 : 두 정수 사이의 합  
https://programmers.co.kr/learn/courses/30/lessons/12912
