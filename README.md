# Study Back-End Service

AWS 환경에서 전체적인 서비스 인프라를 구축하고, 프론트엔드와 백엔드 간의 유기적인 연동을 구현한 프로젝트입니다.

## 프로젝트 개요
본 프로젝트는 **AWS 클라우드 인프라를 활용하여 전체 서비스 배포 파이프라인을 경험**하는 데 중점을 두었습니다. 프론트엔드 자동 배포 파이프라인과 백엔드의 RDS 데이터베이스를 연동하여, 실제 사용자가 도메인을 통해 안정적으로 접근할 수 있는 풀스택 서비스 환경을 구축하였습니다.

## 관련 프로젝트 및 배포 아키텍처
* **프론트엔드 배포 저장소**: [aws-s3-cloudfront-deploy](https://github.com/Leegijun11/aws-s3-cloudfront-deploy)
* **상세 구현 및 블로그 정리**: [Day78 - 백엔드 배포 및 구현 기록](https://myblog73329.tistory.com/100)

## 시연 화면
![시연 화면](이미지_경로_입력)

---

## 서비스 배포 아키텍처 (Full-Stack Deployment)

본 서비스는 프론트엔드와 백엔드가 AWS 인프라 위에서 유기적으로 통신하도록 구성되어 있습니다.


* **Frontend**: GitHub Actions를 통한 S3 & CloudFront 자동 배포 파이프라인 구축
* **Backend**: AWS EC2 내 컨테이너 환경 배포 및 AWS RDS(MySQL)와의 안정적인 데이터 연동
* **Integration**: 프론트엔드 배포 파이프라인과 백엔드 서버를 결합하여 사용자에게 완성된 서비스 경험 제공

---

## 배포 파이프라인 주요 경험
1. **인프라 통합**: S3/CloudFront 기반의 정적 사이트 배포와 EC2 백엔드 서버의 네트워크 연동 구현
2. **데이터베이스 관리**: RDS 환경 설정
3. **자동화 구축**: GitHub Actions를 활용한 지속적인 통합 및 배포(CI/CD) 환경 학습

---

## 보안 안내
본 저장소는 보안을 위해 실제 환경변수(`.env`) 파일을 제외하고 관리하고 있습니다. 서비스 환경 설정을 위해 아래 항목을 참고하시기 바랍니다.

```text
# .env.example
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=your_rds_endpoint
DB_PORT=3306
DB_NAME=studydb
