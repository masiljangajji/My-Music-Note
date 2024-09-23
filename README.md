#   🎶 My-Music-Note
- My-Music-Note는 일기와 음악을 통한 심리치료 서비스입니다.

### 개발 기간
- 2024-09-13 ~ 

### 구성원
| <a href="https://github.com/masiljangajji"><img src="https://github.com/masiljangajji.png" width="100px"><br>BE 이승재</a> | <a href="https://github.com/kooyoonji"><img src="https://github.com/kooyoonji.png" width="100px"><br>FE 구윤지</a> | <a href="https://github.com/NyongCho"><img src="https://github.com/NyongCho.png" width="100px"><br>AI 조준용</a> |<a href="https://github.com/UiinKim"><img src="https://github.com/UiinKim.png" width="100px"><br>AI 김의인</a> 
|-----|-----|-----|----|

### 개발 환경
- 개발도구: Intellij IDEA - Ultimate
- 언어: Java 17 LTS<br>
- 빌드도구: Gradle
- 개발
  - Spring 6.1
  - Spring Boot: 3.3.4
  - Spring Data
    - Spring Data JPA
- 테스트
  - Junit5
  - AssertJ
  - Mockito
  - SonarCloud
- Cloud
  - AWS 
- CI/CD
  - AWS S3
  - AWS CodeDeploy
  - GitHub Actions
- 데이터베이스
  - PostgreSQL 16.3
- ERD
  - ERDCloud

### 사용 기술
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=gradle&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)
<br>
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=react&logoColor=black)
<br>
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-%236DB33F.svg?style=for-the-badge&logo=spring-boot&logoColor=white)
<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-007396.svg?style=for-the-badge&logo=java&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C.svg?style=for-the-badge&logo=hibernate&logoColor=white)
<br>
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![AWS S3](https://img.shields.io/badge/Amazon%20S3-569A31.svg?style=for-the-badge&logo=amazon-s3&logoColor=white)
![AWS CodeDeploy](https://img.shields.io/badge/AWS%20CodeDeploy-232F3E.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon%20AWS-232F3E.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
<br>
![Git](https://img.shields.io/badge/Git-F05032.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=github&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
![DataGrip](https://img.shields.io/badge/DataGrip-000000.svg?style=for-the-badge&logo=datagrip&logoColor=white)
![SonarLint](https://img.shields.io/badge/SonarLint-CB2029.svg?style=for-the-badge&logo=sonarlint&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-F3702A.svg?style=for-the-badge&logo=sonarcloud&logoColor=white)


## 아키텍쳐 구조
![My-Music-Note](https://github.com/user-attachments/assets/d741f12d-06e7-4e57-a1f2-3243b71e3f73)


### WBS
- GitHub Projects의 [RoadMap]([https://github.com/orgs/My-Books-projects/projects/2/views/1?groupedBy%5BcolumnId%5D=Assignees](https://github.com/orgs/My-Music-Note/projects/1/views/4)) 사용
  <img width="1397" alt="스크린샷 2024-09-23 11 30 29" src="https://github.com/user-attachments/assets/a7af2a68-33b8-4950-a4d9-55f67d274d05">

## Refactoring 요소

배포 파이프라인이 GitHub Actions + S3 + CodeDeploy 인 상태  
S3 + CodeDeploy를 조합해서 사용하고자 했던 이유는 zip파일로 기록이 남으니 버전관리가 가능할 것 이라는 생각 또한 Docker라는 AWS내의 서비스가 아닌 외부 서비스에 의존하고 싶지 않아서  
하지만 다음의 문제가 존재함을 인지

1. zip파일로 기록이 남으니 버전관리가 가능한 것은 맞지만 일관된 환경을 제공해 줄 수 있는지
2. 의존성을 줄이고자 함은 생산성을 높이는 방법이기 때문인데 과연 S3 , CodeDploy를 사용하는 방식이 생산성이 더 높은지 , S3,CodeDeploy를 쓰는 조합이 Docker로 이미지 올리고 Pull 땡기는것보다 더욱 복잡하다는 생각이 듬

다음의 이유로 Docker기반으로 배포 라인을 구축할 것 , 또한 Private Subnet의 경우 NAT Gateway를 설정하도록 하겠음










