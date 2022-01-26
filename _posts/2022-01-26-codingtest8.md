---
title:  "x만큼 간격이 있는 n개의 숫자"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-26
last_modified_at: 2022-01-26
---
# Programmers_codingTest [8]

## 문제 : x만큼 간격이 있는 n개의 숫자

## 문제설명  
함수 solution은 정수 x와 자연수 n을 입력 받아,  
x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다.  
다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

## 제한사항
- x는 -10000000 이상, 10000000 이하인 정수입니다.  
- n은 1000 이하인 자연수입니다


## 문제에 대한 생각
for문을 통해 곱을 만들자고 생각하였다.

## 풀이
<pre>
<code>
class Solution {
    public long[] solution(int x, int n) {
        long[] answer = new long[n];
        long v = x;
        
        for(int i = 0; i < n ; i++) {
            answer[i] = v*(i+1);    
        }
        
        return answer;
    }
}
</code>
</pre>

### 출처

프로그래머스 코딩테스트 연습 : x만큼 간격이 있는 n개의 숫자  
https://programmers.co.kr/learn/courses/30/lessons/12954
