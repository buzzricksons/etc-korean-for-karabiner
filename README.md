# Karabiner-Elements 한글 전환용 커스텀 프로필(custom profile for Korean)
Mac OS에 일본어(JIS) 키보드 or 영어(US) 키보드를 사용하면서 영어,일본어,한국어를 사용하는 경우

# 특징
현재 설정되어 있는 언어에 관계없이 다음의 키를 더블 클릭하면 입력 언어를 한글로 전환합니다.
- 일본어(JIS) 키보드: `Kana키`
- 영어(US) 키보드: `우측 커맨드키`
    > ※영어(US) 키보드의 경우 아래의 동작도 포함됩니다.
    > - `좌측 커맨드키` 한번 클릭 : 영어로 전환
    > - `우측 커맨드키` 한번 클릭 : 일본어로 전환

# 동작 확인 환경
- 영어 카탈리나 10.15.6
- 영어 모하비 10.14.4
- 일본어 모하비 10.14.6
- 일본어 하이시에라 10.13.4
- 영어 시에라 10.12.6
- 영어 하이시에라 10.13.6
- 한국어 하이시에라 10.13.5

# 설정 하기 전에
## 1.Karabiner-Elements앱이 설치 되어 있어야 합니다
https://pqrs.org/osx/karabiner/

## 2.세개의 언어(영어, 히라가나, 한글)가 추가되어 있어야 하고 언어변환 순서(Ctrl+Option+Space로 변환했을때)가 일본어 다음에 한글이어야 합니다.
![](https://i.imgur.com/iZZwYgk.png)

카타카나는 삭제할 필요가 있습니다. `구글영어`, `구글히라가나`, `한글2벌식` 이렇게 세개의 언어로 설정 되있는 상태에서 테스트 했습니다.

보통 위의 3개 언어가 설정되어 있는 경우 일본어 다음에 한글로 변환됩니다.

일본에 다음에 한글이 아닐경우 등록되있는 언어를 삭제, 추가해서 순서를 변경해 주세요.

## 3.언어전환이 디폴트 설정으로 되어 있어야 합니다.
![](https://i.imgur.com/eUXsvKQ.png)

`入力メニューの次のソースを選択`설정이 활성화되어 있고 키설정이 디폴트인 `Ctrl+Option+Space`로 되어 있어야 합니다.

# 설정 방법
1.`ChangeKoreanforJapaneseMacOS_rev2.json`파일을 다운로드해서 카라비너의 complex modifications폴더에 추가 합니다.
 > 하이시에라의 경우에는 아래 브랜치의 파일을 다운받으세요.  
 > https://github.com/buzzricksons/etc-korean-for-karabiner/tree/v.1
 
(Finder에서 `shift + command + g`를 실행후 `~/.config/karabiner/assets/complex_modifications`를 붙여넣어서 이동하면 카라비너의 complex modifications폴더로 갈 수 있습니다.)
>※ChangeKoreanforJapaneseMacOS_rev1.json파일을 다운로드할때 github에서 마우스 우클릭의 다른이름으로 저장을 사용하면 확장자는 json이지만 파일내용은 html로 저장되므로 주의.

- 파일위치 ex)
```
/Users/yoda/.config/karabiner/assets/complex_modifications/ChangeKoreanforJapaneseMacOS_rev2.json

``` 

2.카라비너의 preference화면의 Complex Modifications메뉴에서 좌측하단에 있는 Add rule버튼을 클릭합니다.
![](https://i.imgur.com/Kixy6ZN.png)

3.For Korean 일본어 맥OS에서 한글전환키 커스텀 지정 (rev.2)설정에 있는 2가지의 설정중 자기의 키보드에 맞는 설정을 Enable합니다.
![](https://i.imgur.com/dyeLFo4.png)

4.Enable한 설정이 추가되 있는것을 확인합니다. 문제가 있거니 제대로 작동하지 않을때는 이 화면에서 Remove버튼을 클릭하면 설정을 삭제할 수 있습니다.
![](https://i.imgur.com/SKzR2fw.png)

# 주의점
이미 다음의 Rules를 사용하고 있는 경우 설정 전에 삭제해야할 필요가 있습니다.
```
コマンドキーを簡単で押した時に、英数・かなキーを送信する。（左コマンドキーは英数、右コマンドキーはかな）
```

# Change Log
### 2.0 (2018.10.08)
- 모하비에서 US 매직 키보드의 경우 커맨드키와 다른 키와 조합으로 사용할때 인식이 되지 않던 버그 임시 수정.(ex:파인더에서 커맨드키를 누르고 파일을 선택할때 복수개의 파일이 선택이 안됐었음.)

### 1.1 (2018.06.14)
- US 키보드의 오른쪽 커맨드키를 다른 키와 조합으로 사용할때 인식이 되지 않던 버그 수정.

### 1.0 (2018.06.13)
- 최초 버전
