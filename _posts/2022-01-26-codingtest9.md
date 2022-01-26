---
title:  "직사각형 별찍기"
excerpt: "프로그래머스 코딩 테스트 문제입니다. 자바를 이용하여 문제를 해결해봅시다! "

categories: programmers
tags:
  - [CodingTest, Programmers, java]

toc: true
toc_sticky: true
 
date: 2022-01-26
last_modified_at: 2022-01-26
---
# Programmers_codingTest [9]

## 문제 : 직사각형 별찍기

## 문제설명  
이 문제에는 표준 입력으로 두 개의 정수 n과 m이 주어집니다.  
별(*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 출력해보세요.

## 제한사항
- n과 m은 각각 1000 이하인 자연수입니다.



## 문제에 대한 생각
이중 for문을 이용해 행, 렬의 값을 추가해야 한다고 생각하였다.  

## 풀이
<pre>
<code>
import java.util.*;

class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        for(int i = 0; i < b; i++) {
            for(int j = 0; j < a; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
        
    }
}
</code>
</pre>
스캐너(Scanner)를 이용하여 문제에 접근하였다.  
스캐너는 기본 타입의 데이터들을 입력받을 수 있기때문에  
정수값을 받아오기 위해 nextInt()를 함께 사용하였다.

### 출처

프로그래머스 코딩테스트 연습 : 직사각형 별찍기    
https://programmers.co.kr/learn/courses/30/lessons/12969