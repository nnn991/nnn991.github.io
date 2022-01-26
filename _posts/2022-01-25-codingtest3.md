---
title:  "완주하지 못한 선수"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---

# Programmers_codingTest [3]

## 문제 : 완주하지 못한 선수

## 문제설명  
String형 배열 seoul의 element중 "Kim"의 위치 x를 찾아,  
"김서방은 x에 있다"는 String을 반환하는 함수, solution을 완성하세요.  
seoul에 "Kim"은 오직 한 번만 나타나며 잘못된 값이 입력되는 경우는 없습니다.


## 제한사항
- seoul은 길이 1 이상, 1000 이하인 배열입니다.  
- seoul의 원소는 길이 1 이상, 20 이하인 문자열입니다.  
- "Kim"은 반드시 seoul 안에 포함되어 있습니다.



## 문제에 대한 생각
"Kim"의 위치를 생각하고 배열에서의 자리를 의미하는 수를 통해 결과를 도출하려 생각했다.


## 풀이
<pre>
<code>
class Solution {
    public String solution(String[] seoul) {
        String answer = "";
        
        for(int i = 0; i < seoul.length; i++) {
            if(seoul[i].equals("Kim")) {
                answer = "김서방은 " + i + "에 있다";
            }
        }
        return answer;
    }
}
</code>
</pre>
seoul이라는 배열을 반복문에서 "Kim"이라는 값을 찾고 결과를 대입하였다.


### 출처

프로그래머스 코딩테스트 연습 : 서울에서 김서방 찾기  
https://programmers.co.kr/learn/courses/30/lessons/12919
