# infra-server
#CI/CD 용

# 3가지 배포 전략
1.  수동 트리거
  - Readme 수정등을 통해 배포하는 전략
2. 배포 트리거를 각 서비스에서 요청
  - 각 github actions에 infra server 원격 트리거 명령어를 추가하여 배포하는 전략
3. infra-server에서 직접 배포 관리
  - 각 서비스의 github action은 Dockerhub에 푸시만하고
  - 실제 배포는 infra-server에서 docker-compose 이미지 태그를 수정하며 푸시해서 배포한다.

지금은 구성도 작고 아직 완성이 아니기때문에 3번 전략을 사용하여 직접 관리를 할 것이다. 
추후 완성이 가까워지면 2번 전략을 사용하여 배포 자동화까지 구성할 예정이다.
