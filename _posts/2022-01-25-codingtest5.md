---
title:  "문자열 내 p와 y의 개수"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-25
last_modified_at: 2022-01-25
---
# Programmers_codingTest [5]

## 문제 : 문자열 내 p와 y의 개수

## 문제설명  
대문자와 소문자가 섞여있는 문자열 s가 주어집니다.  
s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요.  
'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다.  
단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.  

예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

## 제한사항
- 문자열 s의 길이 : 50 이하의 자연수  
- 문자열 s는 알파벳으로만 이루어져 있습니다.


## 문제에 대한 생각
대소문자를 구분하지않기 때문에 or를 사용하였다.

## 풀이
<pre>
<code>
class Solution {
    boolean solution(String s) {
        boolean answer = true;
        int count = 0;
        char ch = ' ';
        
        for(int i = 0; i < s.length(); i++) {
            
            ch = s.charAt(i);
            if(ch == 'p' || ch == 'P') {
                count ++;
            } else if(ch == 'y' || ch == 'Y') {
                count --;
            }
        }
        
        if(count != 0) {
            return false;
        }
        return true;
    }
}
</code>
</pre>
count라는 정수의 최종결과가 0이 되는지를 확인하여 같은 수의 문자가 나타났는지를 확인하였다.


### 출처

프로그래머스 코딩테스트 연습 : 문자열 내 p와 y의 개수 
https://programmers.co.kr/learn/courses/30/lessons/12916
