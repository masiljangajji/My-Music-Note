#   🎶 My-Music-Note
My-Music-Note는 일기와 음악을 통한 나만의 AI친구 서비스입니다.
- URL(만료): www.musicdiaryclub.com
- [api-server-repo](https://github.com/My-Music-Note/back)



### 개발 환경
- 개발도구: Intellij IDEA - Ultimate
- 언어: Java 17 LTS<br>
- 빌드도구: Gradle
- 개발
  - Spring Boot: 3.3.4
  - Spring Data JPA
- 테스트
  - Junit5
  - AssertJ
  - Mockito
  - SonarCloud
- AWS Infra
  - VPC
  - EC2
  - ALB
  - ASG
  - NAT Gateway
- CI/CD
  - AWS S3
  - AWS CodeDeploy
  - GitHub Actions
  - Docker
- 데이터베이스
  - AWS RDS PostgreSQL 16.3
- ERD
  - ERDCloud
- ETC
   - Post Man

### 사용 기술
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=gradle&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)
<br>
![Spring Boot](https://img.shields.io/badge/Spring_Boot-%236DB33F.svg?style=for-the-badge&logo=spring-boot&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=react&logoColor=black)
<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-007396.svg?style=for-the-badge&logo=java&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C.svg?style=for-the-badge&logo=hibernate&logoColor=white)
<br>
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![AWS S3](https://img.shields.io/badge/Amazon%20S3-569A31.svg?style=for-the-badge&logo=amazon-s3&logoColor=white)
![AWS CodeDeploy](https://img.shields.io/badge/AWS%20CodeDeploy-232F3E.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon%20AWS-232F3E.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white)
<br>
![Git](https://img.shields.io/badge/Git-F05032.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=github&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
![DataGrip](https://img.shields.io/badge/DataGrip-000000.svg?style=for-the-badge&logo=datagrip&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-F3702A.svg?style=for-the-badge&logo=sonarcloud&logoColor=white)


## AWS Infra
![My-Music-Note](https://github.com/user-attachments/assets/384049f4-670b-464b-b53f-b2b6579e8622)

## 기여 내용

- **백엔드 개발**
    - 유저, 일기, GPT 관련 RESTful API 구현
- **고가용성 아키텍처 설계**
    - Auto Scaling Group과 Load Balancer를 활용한 고가용성 아키텍처 구축
    - AWS CodeDeploy를 통한 Blue/Green 배포로 무중단 서비스 제공
- **Artillery를 활용한 성능 테스트**
    - 단일 EC2
        - **타임아웃 오류: 전체 요청의 37.6%(14,766건)**
        - **작업 실패율: 가상 사용자의 54.7%(14,766명)**
    - My-Music-Note
        - **타임아웃 오류: 0%**
        - **작업 실패율: 0%**
        - **99% 요청에 대해 레이턴시 25.8ms**
- **GitHub Actions 기반 CI/CD 파이프라인 구축**
    - Gradle 및 Npm 캐싱 적용으로 CI/CD **빌드 시간 30% 이상 단축**
    - SonarCloud ,JaCoCo 연동으로 PR 단계에서 코드 품질 개선
    - Amazon Machine Image 활용으로 배포 속도 개선 및 비용 절감
- **보안 및 네트워크 강화**
    - Systems Manager 도입으로 SSH 없이 EC2 접근, Bastion Host 비용 제거 및 외부 노출 차단
    - 보안 그룹 및 ALB-ASG 연동으로 Frontend와 Backend 계층 보안 강화
- **코드 품질 관리**
    - 백엔드 서버 **Test Coverage 68.7%**
    

프로젝트 고민 및 트러블 슈팅

- [**AWS 인프라 트러블슈팅 - 배포 전략과 컨테이너 전환**](https://masiljangajji-coding.tistory.com/88)
- [**AWS Systems Manager와 SaaS로 구축한 저비용 고효율 인프라**](https://masiljangajji-coding.tistory.com/89)
- [**Artillery를 활용한 테스트, 이렇게 도입했습니다**](https://masiljangajji-coding.tistory.com/90)


## CI/CD

![CI:CD](https://github.com/user-attachments/assets/f96eb2c9-a07a-42cd-b910-4bd0344e22f2)

0. 인프라 관리비용 최소화를 위해 `Jenkins` 대신 `Github Ations` 사용
1. `S3`는 `CodeDeploy`가 실행시킬 Script를 저장
2. `CodeDeploy`를 사용하는 목적은 `Blue/Green` 배포 + `ASG`로 생성된 `EC2`배포 자동화의 목적 
3. `Docker`를 사용함으로서 동일한 환경을 제공

## SonarCloud 


![SonarCloud](https://github.com/user-attachments/assets/9ecc4c19-5c24-4a93-b7ad-4d0aa661cdc7)

