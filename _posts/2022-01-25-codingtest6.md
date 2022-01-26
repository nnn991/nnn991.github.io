---
title:  "같은 숫자는 싫어"
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
# Programmers_codingTest [6]

## 문제 : 같은 숫자는 싫어

## 문제설명  
배열 arr가 주어집니다.  
배열 arr의 각 원소는 숫자 0부터 9까지로 이루어져 있습니다.  
이때, 배열 arr에서 연속적으로 나타나는 숫자는 하나만 남기고 전부 제거하려고 합니다.  
단, 제거된 후 남은 수들을 반환할 때는 배열 arr의 원소들의 순서를 유지해야 합니다.  

예를 들면,  
- arr = [1, 1, 3, 3, 0, 1, 1] 이면 [1, 3, 0, 1] 을 return 합니다.  
- arr = [4, 4, 4, 3, 3] 이면 [4, 3] 을 return 합니다.  
배열 arr에서 연속적으로 나타나는 숫자는 제거하고 남은 수들을 return 하는 solution 함수를 완성해 주세요.


## 제한사항
- 배열 arr의 크기 : 1,000,000 이하의 자연수
- 배열 arr의 원소의 크기 : 0보다 크거나 같고 9보다 작거나 같은 정수


## 문제에 대한 생각
하나의 정수를 가진 값을 이용해 값을 저장하며 배열의 값들과 비교한다.


## 풀이
<pre>
<code>
import java.util.*;

public class Solution {
    public int[] solution(int []arr) {
        
        ArrayList<Integer> list = new ArrayList();
        
        int prevalue = 0;
        
        for(int i = 0; i < arr.length; i++) {
            if(prevalue != arr[i]) {
                prevalue = arr[i];
                list.add(arr[i]);
            }
        }

        int[] answer = new int[list.size()];
        
        for(int i = 0; i < list.size(); i++) {
            answer[i] = list.get(i);
        }
        return answer;
    }
}
</code>
</pre>

## 또다른 풀이

Stream을 배우고 나서 새로운 방법으로 접근해보았다.
<pre>
<code>

import java.util.*;

public class Solution {
    public int[] solution(int []arr) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        
        int v = 0;
        for(int i = 0; i < arr.length; i++) {
            if(arr[i] != v) {
                list.add(arr[i]);
                v = arr[i];
            }
        }
        return list.stream().mapToInt(i->i).toArray();
    }
}

</code>
</pre>
처음 초기화를 위한 값 v를 0으로 설정하였을 때, 문제의 정답은 맞췄지만  
Test 평가에서는 실패를 맛봤다.  
![q](https://user-images.githubusercontent.com/59858894/150788583-55526f8b-fa7f-4516-8e7f-16b5d437e934.PNG)  

<pre>
<code>

import java.util.*;

public class Solution {
    public int[] solution(int []arr) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        
        int v = -10;
        for(int i = 0; i < arr.length; i++) {
            if(arr[i] != v) {
                list.add(arr[i]);
                v = arr[i];
            }
        }
        return list.stream().mapToInt(i->i).toArray();
    }
}

</code>
</pre>
초기화를 위한 값을 -10으로 변경한 후 성공하였다.

### 출처

프로그래머스 코딩테스트 연습 : 같은 숫자는 싫어
https://programmers.co.kr/learn/courses/30/lessons/12906
