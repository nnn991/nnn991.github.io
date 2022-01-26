---
title:  "수박수박수박수박수박수?"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories:
  - CodingTest
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---
# Programmers_codingTest [2]

## 문제 : 수박수박수박수박수박수?

## 문제설명  
길이가 n이고, "수박수박수박수...."와 같은 패턴을 유지하는 문자열을 리턴하는 함수, solution을 완성하세요.  
예를들어 n이 4이면 "수박수박"을 리턴하고 3이라면 "수박수"를 리턴하면 됩니다.


## 제한사항
- n은 길이 10,000이하인 자연수입니다.


## 문제에 대한 생각
반환받는 결과는 입력된 길이에 따라서 달라진다.  
홀수의 경우 "수"로 끝나고 짝수의 경우 "박"으로 끝난다.  
두가지 경우로 나누어 진행하려 한다.


## 풀이
<pre>
<code>
class Solution {
    public String solution(int n) {
        String answer = "";
        
        for(int i = 0; i < n; i++) {
            if(i%2 == 0) {
                answer+="수";
            }
            if(i%2 == 1) {
                answer+="박";
            }
        }
        return answer;
    }
}
</code>
</pre>
반복문을 통해 2로 나누었을때 나머지가 0인 경우 "수"를 추가하여 반환하고  
나머지가 1인 경우 "박"을 추가하여 반환하는 코드를 작성하였다.


### 출처

프로그래머스 코딩테스트 연습 : 완주하지 못한 선수  
https://programmers.co.kr/learn/courses/30/lessons/12922
