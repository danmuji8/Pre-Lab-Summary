# Cloud Platfrom Eng. 영역 Pre-Lab PaaS_AWS 과정

- **개요**
  - 본 예제는 GitOps기반 SRE과정을 위한 클라우드 플랫폼 환경구축과 마이크로서비스 전 라이프사이클(분석/설계, 구현, DevOps 툴체인(파이프라인)을 통한 배포, 운영/모니터링)을 커버하도록 구성된 예제입니다. 
  - 분석/설계/구현을 포함한 클라우드 플랫폼기반 운영(컨테이너 오케스트레이션, 모니터링, 로깅, etc) 중심으로 예제 프로젝트는 전개됩니다.
  - PreLab 기간동안 주어진 마이크로서비스 리소스를 사용하거나, 새로운 도메인 모델을 선정 후 설계/구현/배포/운영/모니터링을 적용해도 됩니다.
 
- **진행내역** 
  - MSA 아키텍처 구성
  ![image](https://user-images.githubusercontent.com/86272090/174928889-b6e9d184-3632-436d-8af2-2b1e7c15f6c2.png)
  
  
  - Cloud Platform 프로비저닝
    - EKS 생성
      ![image](https://user-images.githubusercontent.com/86272090/174931479-31ad8210-346e-46ee-ae97-6f4055a5680e.png)
      ![image](https://user-images.githubusercontent.com/86272090/174934173-32ddb4d1-27be-4ca0-a84b-e52b7f1fce60.png)
    - ECR 생성
    - ![image](https://user-images.githubusercontent.com/86272090/174934535-462fb32b-a6c8-4a36-a87e-9917d4d6eff3.png)
    - Docker Login to ECR
    - ![image](https://user-images.githubusercontent.com/86272090/174935084-f3d0b4a3-62e0-49f1-bcac-0b0b9211ac43.png)
    - Metric Server 설치
    - ![image](https://user-images.githubusercontent.com/86272090/174935276-5f89fd5d-8384-4312-b4c9-512fd786546e.png)


  - DevOps Toolchain 구축 
    - 프로젝트 별 ECR 생성
    - ![image](https://user-images.githubusercontent.com/86272090/174936592-b5d44c63-03a8-4a81-91da-7aeec5396afe.png)
    - 프로젝트 별 CodeBuild 생성
    - ![image](https://user-images.githubusercontent.com/86272090/174979131-6be71a3d-93ba-461b-9760-2ef7703f0420.png)
    - CodeBuild 상세
    - ![image](https://user-images.githubusercontent.com/86272090/174979460-9d766f1c-f9dc-43c5-a59a-d0bcfc64d1fd.png)
    - ![image](https://user-images.githubusercontent.com/86272090/174979584-1538436e-3f73-458e-8589-d35d9a894bfc.png)
    - ![image](https://user-images.githubusercontent.com/86272090/174979731-069ef006-5b8a-484c-b7c4-b719e11b8114.png)
    - buildspec-kubectl.yml 상세
    - ![image](https://user-images.githubusercontent.com/86272090/174980351-c5ab4f39-7661-41fb-94a9-357e1aa87c20.png)
    - ![image](https://user-images.githubusercontent.com/86272090/174980633-cb43ed83-e887-4556-a834-b48ef0371693.png)
    - ![image](https://user-images.githubusercontent.com/86272090/174980728-ee1f5a98-5b03-491a-aec8-cf6e54c6294b.png)
    - EKS Connection 설정
    - ![image](https://user-images.githubusercontent.com/86272090/174970155-9eb2e488-7f27-4d55-a8e8-8779528a4071.png)
    - EKS 배포된 서비스 확인
    - ![image](https://user-images.githubusercontent.com/86272090/175186367-c9d5df98-1e0f-4112-ad41-bd4b71061598.png)


  - 분산 메시징 플랫폼 구성 
    - Kafka 설치
    - ![image](https://user-images.githubusercontent.com/86272090/175186158-6ace7af4-2c40-4158-b776-7da882f318a1.png)
    - ![image](https://user-images.githubusercontent.com/86272090/175186224-2999e010-6589-4b00-b3c6-528e5fddd48c.png)
    - ![image](https://user-images.githubusercontent.com/86272090/175186261-6bdb8a90-2a5b-44e9-b1bf-ec1c8a102ca9.png)


  - SLA 운영 - 오토 스케일아웃(Auto Scale-out) 
  - SLA 운영 - 무정지 배포(Zero downtime Deploy) 
  - Service Mesh 인프라 구축
  - Service Mesh 기반 마이크로서비스 Resilience 적용
  - 마이크로서비스 통합 모니터링
  - 마이크로서비스 통합 로깅
  - 분산 메시징 플랫폼 모니터링
