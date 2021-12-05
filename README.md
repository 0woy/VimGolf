# VimGolf 문제 풀이

## Q1. Add quotes to ansible playbook

* $ vimgolf put 5f0f5fbe280fbf000c233304
* 최고점: 8
* 나의 타수: 9
> *마지막 줄 {} 양쪽에 큰 따옴표를 붙여주는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144712900-de3f3c08-16c0-4a2a-bcfc-b279a7642b21.GIF" width ="100%" height ="100%">
 


## My Solve
<img src = "https://user-images.githubusercontent.com/87132052/144713166-5e1104fa-4985-453d-8dba-4c77cf2dbc73.gif" width ="80%" height ="80%"> 


### 입력 명령어 
***GWi"[END]"[ESC]ZZ*** 
|명령어|설명|
|:---:|:----:|
|**G**|마지막 줄로 이동|
|**W**|{ 앞으로 커서 이동|
|**i"[END]"[ESC]**|INSERT MODE 실행 후 " 입력, 라인 맨 끝으로 이동(**[END]**), " 입력 후 모드 종료|

---

### Q2.  simple replacements
* $ vimgolf put 603ba26a01b4d00009c10a49
* 최고점 : 19
* 나의 타수: 27
> *Start file의 sumbline, emasc 문자열을 vim으로 치환하는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144735079-490226bb-a8c2-431b-8d28-1ab85ac8e14b.GIF" width ="100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144735129-3c8740d0-c82c-48a3-aa80-96fe969fb991.gif" width ="80%" height ="80%">


### 입력 명령어 

***Wdwivim[Esc]:%s/emacs/vim/g[CR]ZZ***
|명령어|설명|
|:---:|:----:|
|**W**|subline 앞으로 커서 이동|
|**dw**|subline 잘라내기|
|**ivim[Esc]**|INSERT MODE 실행, vim입력 후 모드 종료|
|**:%s/emacs/vim/g[CR]**|모든(**%s**) emacs를 바로(**g**) vim으로 치환|


---

### Q3.  Satisfy the go linter
* $ vimgolf put 5f1063aa8361810006e73210
* 최고점 : 20
* 나의 타수: 33
> *주석을 추가하는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144735289-8ca9c10a-ca88-4d80-82bb-ed2a9fd23ab1.GIF" width ="100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144737192-93c18189-00f1-44c8-b490-8c2f95ba2d1e.gif" width ="80%" height ="80%">


### 입력 명령어 
***4GywO// TODO[Esc]bPyy6GPwdwiDebug [Esc]ZZ***

|명령어|설명|
|:---:|:-------:|
|**4(6)G**|4(6)번째 line으로 이동|
|**yw**|Version 잘라내기|
|**O**|커서가 위치하는 line을 뒤로 밀어내고 INSERT MODE 실행|
|**// TODO[ESC]**|"// TODO" 입력 후 종료(큰따옴표 포함X)|
|**B**|TODO의 앞으로 이동|
|**P**|잘라낸 Version 붙여넣기|
|**yy**|// Version TODO(라인 전체)복사|
| **PWdw**|복사한 line 붙여 넣기, V앞으로 이동(**W**)후 Version 잘라내기|
|**iDebug [ESC]**| INSERT MODE 실행 후 "Debug "입력(큰따옴표 포함X)후 모드 종료|

---

### Q4. Plotting some variables in python
*  $ vimgolf put 9v0060da5177000000000209
* 최고점 : 34
* 나의 타수: 55
> *행마다 숫자와 문자를 바꾸는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144735592-9034db8c-5af8-4f78-bd3f-94d640543f79.GIF" width ="100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144735600-a6bf5bad-82fb-4a18-8197-dc5b1b400b14.gif" width ="80%" height ="80%">


### 입력 명령어 
***:%s/y1/abs(y1)/g[CR]/k[CR]rg[Up]rr[Up]rb/1[CR][Home]nr2n.n.nr3n.n.nr4n.n.ZZ***
|명령어|설명|
|:---:|:----:|
|**:%s/y1/abs(y1)/g[CR]**|모든 y1을 abs(y1)으로 치환|
|**/k[CR]**|k 찾고 커서가 위치한 line의 k 앞으로 이동|
|**rg(r,b)[Up]**|k를 g(r,b)로 덮어쓰기|
|**/1[CR]**|1 찾고 커서가 위치한 line의 1 앞으로 이동|
|**[Home]**|라인의 맨 앞으로 이동|
|**n**|커서 위치를 기준, 다음 문자로 이동|
|**r2(3,4)**|1을 2(3,4)로 덮어쓰기|
| **.**|직전 명령 반복|

---

### Q5. Python dataclasses
* $ vimgolf put 6013804df3308e0009368f1c
* 최고점 : 19
* 나의 타수: 28
> *큰 따옴표 안에 문자열을 추가하는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144736685-9aa4a64c-60a3-4655-a7ab-61ef9b168c43.GIF" width = "100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144737574-02ff39c5-f330-49a0-b481-001ba55fa980.gif" width ="80%" height ="80%">


### 입력 명령어 

***5Gye5jf"pa,name,age,score[Esc]ZZ***
|명령어|설명|
|:---:|:----:|
|**5G**|5번째 line으로 이동|
|**ye**|student_id(한 마디) 복사|
|**5jf"**|5칸 아래로 이동(**5j**), "앞으로 이동|
|**p**|현재 위치 다음에 붙여넣기|
|**a**|현재 위치 다음 칸에서 INSERT MODE 시작|
