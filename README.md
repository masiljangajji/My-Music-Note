
# My-Music-Note Project Convention 

프로젝트의 컨벤션을 정의하는 문서입니다.
<br>
<br>
## commit convention 

다음의 양식으로 사용합니다. 
~~~
{태그}: {제목} #{이슈번호}
~~~

사진

### 태그 
1. feat 
    - 코드가 변경됐으며 결과또한 변경됐을때
2. refactor
    - 코드가 변경됐지만 결과가 같은 경우 
    - Ex) 같은 회원가입 기능이지만 , 코드 최적화로 성능이 개선됐다
3. test
    - 테스크코드 작성
4. fix
    - 버그 수정
5. docs
    - 문서 수정
    - Ex) gitignore 
6. chore
    - 코드 포멧팅 , 주석 추가 , 불필요한 파일 삭제 등 

~~~
feat: 회원가입 기능 추가 #1
refactor: 상품 카테고리 변경 #2 
~~~
<br>

## GitHub - Flow 


<img width="1097" alt="스크린샷 2024-09-09 10 13 00" src="https://github.com/user-attachments/assets/872bb71b-6a48-49ad-865c-747e9ba36efc">


### 규칙

1. main Branch는 stable 상태로 product에 배포되는 브랜치
    - 엄격한 role과 함께 사용
2. 새로운 브랜치는 항상 main 브랜치에서 만든다.
3. 브랜치 이름을 통해 의도를 명확하게 드러낸다.
4. 커밋 메시지를 명확하게 작성한다.
5. PR(Pull Request)을 통한 코드리뷰 후 Merge를 원칙으로한다.

#### 이와 관련한 CI/CD 작업은 추후에 설정하겠습니다.

<br>

## Project Management

일정관리는 GitHub Project 기능을 사용한다.

작업할 기능에대한 정보를 Issue로 작성하고  

Status, Start Date, End Date, Assignees 등의 정보를 설정해줘야 한다.

<img width="1228" alt="스크린샷 2024-09-09 10 46 52" src="https://github.com/user-attachments/assets/075d5e57-3561-4565-b308-fbcd70c0027f">


### Status Board

<img width="1428" alt="스크린샷 2024-09-09 10 37 00" src="https://github.com/user-attachments/assets/785b958d-fd12-4a6a-aed0-9bd574cc9acf">



### Label

<img width="813" alt="스크린샷 2024-09-09 10 45 45" src="https://github.com/user-attachments/assets/86245ec7-37cd-45f0-9019-c7c73eede576">


#### Label의 경우 위에 해당하는 Issue가 아니라면 별도로 설정하지 않아도 됩니다.

