### CSS기초 문제를 풀면서 학습을 해보자.

1번문제
plate를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/cc5092c7-aeb5-429d-8ea3-5f45a7c3185b/image.png)

```
정답 : plate
```

2번 문제
bento box를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/3826611c-e550-43f5-a3d6-3e1fb79201cd/image.png)

```
정답 : bento
```

3번 문제
plate를 선택해라
![](https://velog.velcdn.com/images/mandoo1229/post/debba288-0170-4c73-906e-f7dbe1399722/image.png)

```
정답 : #fancy //id태그 방식을 사용하였습니다.
```

4번 문제
plate 위에 있는 apple을 선택해라
![](https://velog.velcdn.com/images/mandoo1229/post/f1515337-7735-41b7-9160-2744e4ada188/image.png)

```
정답 : apple plate  // 특정 요소 안에 포함되어 있는 자식요소를 선택한다.

```

5번 문제
fancy plate 위에 있는 pickle을 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/1b937d9e-cea8-44e8-8bc4-c16e5e39b136/image.png)

```
정답 : #fancy pickle //id선택하는 방식이다.
```

6번
작은 사과를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/80370fc2-1d66-4ff6-9361-9c706bce1200/image.png)

```
정답 : .small  //클래스 선택하는 방식이다.
```

7번
작은 오렌지를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/48fee391-9167-4a0d-b700-647350f4e2e5/image.png)

```
정답 : orange.small //특정 요소안에 있는 class를 선택하는 방식을 알려주는 것이다.
```

8번
bento안에 작은 오렌지를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/c37d0609-d282-4f88-979c-78bf45e9dc92/image.png)

```
정답 : bento orange.small  //
```

9번
모든 bento와 plate를 선택해라.
![](https://velog.velcdn.com/images/mandoo1229/post/8cc34f4c-feef-474a-bd30-52729115867a/image.png)

```
정답 : bento, plate
```

10번
모든 것을 선택하세요!
![](https://velog.velcdn.com/images/mandoo1229/post/49686572-6ee2-4ab5-8376-d5d18d62519d/image.png)

```
정답 : *  // *은 모든 태그를 선택한다는 의미입니다.
```

11번
plate의 모든 것을 선택하세요.
![](https://velog.velcdn.com/images/mandoo1229/post/c0844025-7d34-47de-b265-fbe432176278/image.png)

```
정답 : plate *
```

12번
bento 옆에 있는 모든 apple를 선택하세요.
![](https://velog.velcdn.com/images/mandoo1229/post/e0b0734e-efdb-42df-857c-0153fae59785/image.png)

```
정답 : plate+ apple
```

13번
bento 옆에 있는 pickle을 선택하세요
![](https://velog.velcdn.com/images/mandoo1229/post/d60cb67f-2ce4-4c3e-9dfd-c83a6d99e0b4/image.png)

```
정답 : pickle ~ pickle
```

14번
plate에 있는 apple를 직접 선택
![](https://velog.velcdn.com/images/mandoo1229/post/b7baa1dc-b2f8-41cc-9404-974d7ec8e8da/image.png)

```
정답 : plate > apple
```

15번
상단 제일 위에 있는 orange 선택
<img width="519" alt="스크린샷 2023-07-24 오후 3 06 56" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/c2d0c73e-b5e5-42c6-928c-078513f864cb">

```
정답 : orange:first-child
```

16번
plate에 apple과 pickle를 선택
<img width="979" alt="스크린샷 2023-07-24 오후 3 08 15" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/b45cd69c-c963-4298-9690-d1c7b26a66c2">

```
정답 : plate: only-child
```

17번
작은 apple과 pickle를 선택
<img width="803" alt="스크린샷 2023-07-24 오후 3 09 41" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/02bdf5a4-72ee-4127-9933-23dd13a8bc47">

```
정답 : apple, pickle:last-child
```

18번
3번째 plate 선택
<img width="612" alt="스크린샷 2023-07-24 오후 3 11 56" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/739d86f3-e9cd-46e0-a848-6baaea8b10fb">

```
정답 : plate:nth-child(3)
```

19번
첫 번째 bento 선택
<img width="610" alt="스크린샷 2023-07-24 오후 3 13 21" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/e9ea7fd2-06b5-4be0-bb64-cfd5730f4446">

```
정답 : bento:last-child(3)
```

20번
첫 번째 apple 선택
<img width="571" alt="스크린샷 2023-07-24 오후 3 16 19" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/1d2d2faa-44d6-46aa-a499-eaaacaa571b8">

```
정답 : apple:first-of-type
```

21번
짝수 plate를 선택
<img width="789" alt="스크린샷 2023-07-24 오후 3 18 31" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/8a7b3458-6af2-4766-b797-e95c26483f6d">

```
정답 : plate:nth-of-type(even)
```

22번
3번째에서 시작하여 2번째 plate를 선택하세요.
<img width="963" alt="스크린샷 2023-07-24 오후 3 20 39" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/a443a461-d171-426c-9d1d-f4c251d73a28">

```
정답 : plate:nth-of-type(2n+3)
```

23번
중간에 있는 plate에 apple을 선택하세요
<img width="789" alt="스크린샷 2023-07-24 오후 3 22 15" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/4b46aec5-4986-4dc3-902a-96deba72cb47">

```
정답 : apple:only-of-type

```

24번
마지막 orange와 apple를 선택하세요.
<img width="775" alt="스크린샷 2023-07-24 오후 3 23 48" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/93d1223b-b54b-4e29-9de3-0fb3bcdc7ef0">

```
정답 : .small:last-of-type
```

25번
빈 bento를 선택하세요.
<img width="614" alt="스크린샷 2023-07-24 오후 3 24 36" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/c209669c-fdec-4eb0-9feb-5ee6c7563ad8">

```
정답 : bento:empty
```

26번
Big apple만 선택하세요.
<img width="617" alt="스크린샷 2023-07-24 오후 3 25 58" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/fd774377-e787-471d-a444-fe1af3e351b6">

```
정답 : apple:not(.small)
```

27번
누군가를 향한 항목을 선택하세요
<img width="643" alt="스크린샷 2023-07-24 오후 3 27 05" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/85573c65-f296-4049-9600-5263b26a36c5">

```
정답 : [for]
```

28번
누군가를 위해 plate를 선택하십시오.
<img width="663" alt="스크린샷 2023-07-24 오후 3 28 31" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/35d11073-e24a-4901-80fa-96c624d63163">

```
정답 : plate[for]
```

29번
Vitaly's의 식사를 선택하세요.
<img width="493" alt="스크린샷 2023-07-24 오후 3 29 54" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/8a7f0a06-e770-41b5-8f0f-60cab7258ae7">

```
정답 : bento[for="Vitaly"]
```

30번
이름이 'Sa'로 시작하는 사람을 선택
<img width="978" alt="스크린샷 2023-07-24 오후 3 32 09" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/775b8842-d82e-4250-a9f3-cbacddef0383">

```
정답 : [for^='Sa']
```

31번
이름이 'ato'로 끝나는 항목을 선택하세요.
<img width="981" alt="스크린샷 2023-07-24 오후 3 33 59" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/54100004-f59c-4eb8-a7c0-177bbcb5e8ff">

```
정답 : [for$='ato']
```

32번
이름에 'obb'가 포함된 식사를 선택하세요.
<img width="961" alt="스크린샷 2023-07-24 오후 3 34 50" src="https://github.com/mandoo1229/React-Board-Restart/assets/123732776/86e11f51-d194-4bc3-9e17-4996d00dbab3">

```
정답 : [for*="obb"]
```
