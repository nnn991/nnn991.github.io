---
title:  "가운데 글자 가져오기"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---
# Programmers_codingTest [7]

## 문제 : 가운데 글자 가져오기

## 문제설명  
단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요.  
단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

## 제한사항
- s 는 길이가 1 이상, 100이하인 스트링입니다.


## 문제에 대한 생각
글자의 길이를 구해서 짝수, 홀수의 경우 문자를 반환하는 방법을 사용하려 생각했다.


## 풀이
<pre>
<code>
class Solution {
    public String solution(String s) {
        String answer = "";
         
            if(s.length()%2 == 0) {
                answer = s.substring(s.length()/2 - 1, s.length()/2 + 1);
            }
            else if(s.length()%2 == 1) {
                answer = s.substring(s.length()/2, s.length()/2 + 1);
            }
        
        return answer;
    }
}
</code>
</pre>
substring()을 사용하여 문자열을 추출하였다.

### 출처

프로그래머스 코딩테스트 연습 : 가운데 글자 가져오기  
https://programmers.co.kr/learn/courses/30/lessons/12903
