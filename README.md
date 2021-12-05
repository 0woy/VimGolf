# VimGolf 문제 풀이

## Q1. Add quotes to ansible playbook

* $ vimgolf put 5f0f5fbe280fbf000c233304
* 최고점: 8
* 나의 타수: 9
> *마지막 줄 {} 양쪽에 큰 따옴표를 붙여주는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144712900-de3f3c08-16c0-4a2a-bcfc-b279a7642b21.GIF" width ="100%" height ="100%">
 


## My Solve
<img src = "https://user-images.githubusercontent.com/87132052/144713166-5e1104fa-4985-453d-8dba-4c77cf2dbc73.gif" width ="80%" height ="80%">\
### 입력 명령어: ***GWi"[END]"[ESC]ZZ*** 
> **G**: 마지막 줄로 이동, **W**: 다음 단어 앞으로 커서 이동\
> **i**: INSERT MODE,  **[END]**: 라인 맨 끝으로 이동\
> **[ESC]**: INSERT MODE 종료, **ZZ**: 저장 후 종료

---

### Q2.  simple replacements
* $ vimgolf put 603ba26a01b4d00009c10a49
* 최고점 : 19
* 나의 타수: 27
> *Start file의 sumbline, emasc 문자열을 vim으로 치환하는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144735079-490226bb-a8c2-431b-8d28-1ab85ac8e14b.GIF" width ="100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144735129-3c8740d0-c82c-48a3-aa80-96fe969fb991.gif" width ="80%" height ="80%">
### 입력 명령어: ***Wdwivim[Esc]:%s/emacs/vim/g[CR]ZZ***
> **W**: 다음 단어(subline) 앞으로 커서 이동, **dw**: 단어 잘라내기\
> **i, vim**: Insert Mode로 변경 후 vim입력, **[ESC]**:INSERT MODE 종료\
> **:%s/emacs/vim/g[CR]ZZ**: 모든(**%s**) emacs를 바로(**g**) vim으로 치환 후 종료

---

### Q3.  Satisfy the go linter
* $ vimgolf put 5f1063aa8361810006e73210
* 최고점 : 20
* 나의 타수: 35
> *주석을 추가하는 문제입니다.*
 <img src = "https://user-images.githubusercontent.com/87132052/144735289-8ca9c10a-ca88-4d80-82bb-ed2a9fd23ab1.GIF" width ="100%" height ="100%">

## MY Solve
<img src = "https://user-images.githubusercontent.com/87132052/144735129-3c8740d0-c82c-48a3-aa80-96fe969fb991.gif" width ="80%" height ="80%">
### 입력 명령어: ***:4[CR]ywO// TODO[Esc]BPyy:6[CR]PWdwiDebug [Esc]ZZ***

### Q3. Plotting some variables in python
### Q4. Python dataclasses
