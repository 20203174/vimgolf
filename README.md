### vimgolf

(1) Add quotes to ansible playbook

<img src="https://user-images.githubusercontent.com/93987703/144702735-af431738-7f7e-4f82-96a4-90df28c890ce.png" width=50% height=50%> <img src="https://user-images.githubusercontent.com/93987703/144702740-6994a1a5-6691-419b-88d4-a2d141a67a72.png" width=50% height=50%>

Score: 9
1. 먼저 문서 맨 끝으로 이동한다: G
2. 단어 단위로 이동하면서 단어 시작을 기점으로 {로 이동한다: w
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

