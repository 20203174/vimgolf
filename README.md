### vimgolf

(1) Add quotes to ansible playbook

<img src="https://user-images.githubusercontent.com/93987703/144702735-af431738-7f7e-4f82-96a4-90df28c890ce.png" width=50% height=50%> <img src="https://user-images.githubusercontent.com/93987703/144702740-6994a1a5-6691-419b-88d4-a2d141a67a72.png" width=50% height=50%>

Score: 9
1. 먼저 문서 맨 끝으로 이동한다: G
2. 단어 단위로 이동하면서 단어 시작을 기점으로 {로 이동한다: W
3. 해당 커서에서 입력모드로 바꿔주면 되기 때문에 바꾸어준다: i
4. "를 입력한다: "
5. 입력모드인 상태에서 문장 끝으로 이동한다: End
6. "를 입력한다: "
7. 입력모드에서 명령어모드로 바꿔준다: Esc
8. 저장 후 종료한다: ZZ

<img src="https://user-images.githubusercontent.com/93987703/144703236-959ef119-d831-4a04-9b56-3586a5e37330.png" width=50% height=50%>


(2) simple replacements

<img src="https://user-images.githubusercontent.com/93987703/144703310-d66c0446-a44d-40ad-96d2-e5b57c49f32c.png" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/93987703/144703313-c452629d-6183-40cf-b3f4-944d3d88a781.png" width=50% height=50%>

sublime --> vim
emacs --> vim

Score: 27

1. 문서 전체에 대한 문자열치환을 위해서 :%s/
2. 바꿀 문자인 sublime과 emacs를 or로 연결해준다: sublime\|emacs
3. 이를 vim으로 바꾸어준다: /vim
4. 전체를 바꿔줄 것이기 때문에 g옵션을 준다: /g

<img src="https://user-images.githubusercontent.com/93987703/144703857-47f71a4e-763f-4421-9040-d71a3387aa61.png" width=50% height=50%>


(3) Satisfy the go linter

<img src="https://user-images.githubusercontent.com/93987703/144703897-e68f1cde-6ddf-4efa-84b7-0f3c95f43c36.png" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/93987703/144703899-c6c547f1-2f7e-4527-86bc-4e2ea589d717.png" width=50% height=50%>

Score: 35

1. 먼저 4번째 줄로 이동해준다: :4 
2. 그러면 커서가 V로 이동하고 그 앞줄에 주석문을 추가하기 때문에 현재 라인 이전 줄 추가해서 편집모드를 열어준다: O
3. // Version TODO 작성한다
4. 또 작성해야할 줄과 Debug단어만 다르기 때문에 명령모드로 빠져나와 복사해준다: Esc, yy
5. 밑 줄로 이동한다: j
6. 그 밑에 복사한 내용을 붙여넣는다: p
7. 커서가 /로 이동하고 다음 문자의 시작으로 이동한다: W
8. 단어 단위로 편집하는 cw로 Version단어를 Debug로 수정한다: cw, Debug작성
9. 명령모드로 돌아와서 저장후 나간다: Esc, ZZ

<img src="https://user-images.githubusercontent.com/93987703/144740724-d6a243d5-91a4-4864-b4d3-5c597621c65e.png" width=50% height=50%>


(4) Plotting some variables in python

<img src="https://user-images.githubusercontent.com/93987703/144740747-b0a350a0-dd62-477d-af3a-f45e3ab9b861.png" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/93987703/144740755-6eaa4816-26cd-4e26-a712-f5d8ccbe893d.png" width=50% height=50%>

Score: 60

1. :%s/y1/abs(y1) #y1문자를 abs(y1)로 문자로 바꿔준다. 
2. 커서가 자동으로 마지막 라인으로 이동되는데, 이 때 문서 마지막 부분으로 커서를 옮겨준다: $
3. 1문자가 있는 곳을 1,2,3,4중 맞는 값으로 넣어줄건데 이를 위해 거꾸로 문자를 찾는 ?(text)를 이용한다: ?1 --> n 으로 이동가능! 문자를 바꿀 때는 한 글자만 바꿔주는 r 이용!
4. 마지막 1을 2로 바꾼 후에 마지막으로 k문자들만 바꾸어주면 된다. 해당 라인에서 문자를 바꿔주며 이동한다: /k --> n 으로 이동! 문자를 바꿀 때는 r 이용!
5. 이후 종료 ZZ

<img src="https://user-images.githubusercontent.com/93987703/144741067-0fd8fc24-85b6-4e48-8654-2e4169ca33ed.png" width=50% height=50%>

