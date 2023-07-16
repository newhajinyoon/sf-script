**주의**<br>
_아직 같은 경로에 있는 `summon.sf` 밖에 인식하지 못합니다!<br>이름이 달라도 인식하지 못합니다!_<br>
패치예정

[English README](https://github.com/newhajinyoon/sf-script/blob/main/READ%20ENGLISH.md)

# SF 스크립트 (Summon File Script) 사용 방법

![sf script](https://github.com/newhajinyoon/sf-script/assets/61103309/dee7e8d5-16d8-49de-918c-e6d41ac6471a)

**SF 스크립트**는 파일과 코드를 자동으로 생성하는 명령 스크립트입니다. 주어진 명령대로 파일과 코드를 생성하거나 덮어쓸 수 있습니다. GPT와 함께 활용하면 효과가 2051배 됩니다.

1. [다운로드](https://github.com/newhajinyoon/sf-script/releases)합니다.
2. 작성된 `summon.sf` 파일과 같은 경로에 `sf.exe` 파일을 둡니다. 
3. `sf.exe`를 실행합니다.

## 명령 스크립트 작성법

1. `m : 경로;`: 파일을 생성할 기본 경로를 설정합니다. 다음에 오는 모든 파일과 디렉토리는 이 기본 경로를 기준으로 생성됩니다.

2. `f : 파일명;`: 파일을 생성합니다. 파일명은 생성할 파일의 상대 경로를 의미합니다. 기본 경로를 기준으로 생성됩니다. 파일명에 하위 디렉토리를 포함하면 해당 디렉토리가 없으면 자동으로 생성됩니다.

3. 코드 덮어쓰기:
   ```
   c[파일명] :
   --!
   코드
   --!;
   ```
   파일 내용을 덮어씁니다. `[파일명]` 부분에 덮어쓸 파일의 상대 경로를 지정하고, `코드` 부분에는 파일에 덮어쓸 내용을 작성합니다.

4. `;`: 세미콜론은 하나의 명령이 끝났음을 나타냅니다. 각 명령은 세미콜론으로 구분됩니다.

5. `* ` : 주석입니다. 

6. `l : true` : 코드의 맨 앞에 작성할시, `log.txt`를 생성합니다.

## 예시

아래는 `.sf` 스크립트의 예시입니다. 이를 "summon.sf" 파일에 복사하여 사용할 수 있습니다:

```sf
m : D:\desktop\파이썬\서먼;

f : templates/hi.html;
f : templates/test.html;
f : app.py;
f : data.json;

c[templates/test.html] : 
--!
<div> This is the in-game template </div>
--!;

c[templates/hi.html] : 
--!
<p> hi! </p>
--!;
```

## GPT 활용

`.sf`와 GPT를 함께 사용한다면, 30초 안에 **웬만한 사이트**를 하나 만들 수 있습니다.

아래는 GPT에게 간단한 채팅 사이트를 Flask로 만들어달라고 한 예시입니다:

```
온라인 채팅 서비스를 Flask와 함께 만들어줘 CSS도 해주고
적어도 파일 5개를 생성해줘
SF 스크립트를 활용하여 해줘.
```

https://github.com/newhajinyoon/sf-script/assets/61103309/9f00c53c-fa4a-4612-852c-0d9e284357ee

여기서 만들어진 `summmon.sf`는 [여기서](https://github.com/newhajinyoon/sf-script/blob/main/example/chat/summon.sf) 다운할수 있습니다.


### SF 파일 작성법을 GPT에게 학습시키기

GPT에게 학습시키려면 [여기에서](https://raw.githubusercontent.com/newhajinyoon/sf-script/main/GPT/V2%20en) 글을 모두 복사해서 GPT에게 붙여넣으세요. GPT가 학습된 후, SF 스크립트를 활용해달라는 말을 뒤에 붙이기만 하면 작동합니다.<br>
[한국어](https://raw.githubusercontent.com/newhajinyoon/sf-script/main/GPT/V2) / [이전 버전](https://raw.githubusercontent.com/newhajinyoon/sf-script/main/GPT/)

## 구현 예정

SF 파일을 그냥 클릭해서 열어서 작동하는 기능이 구현 예정에 포함되어 있습니다.

## 특별한 감사
[kdh8219](https://github.com/kdh8219)
