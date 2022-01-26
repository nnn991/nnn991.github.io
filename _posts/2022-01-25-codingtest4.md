---
title:  "약수의 합"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---

# Programmers_codingTest [4]

## 문제 : 약수의 합

## 문제설명  
정수 n을 입력받아 n의 약수를 모두 더한 값을 리턴하는 함수, solution을 완성해주세요.


## 제한사항
- n은 0 이상 3000이하인 정수입니다.


## 문제에 대한 생각
for문을 통해 나머지가 0이 나오는 값들을 찾아주었다.


## 풀이
<pre>
<code>
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for(int i = 1; i <= n; i++) {
            if(n%i == 0) {
                answer+=i;
            }
        }
        
        return answer;
    }
}
</code>
</pre>



### 출처

프로그래머스 코딩테스트 연습 : 약수의 합  
https://programmers.co.kr/learn/courses/30/lessons/12928
