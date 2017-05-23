
# 0. docker 설치 
* docker 설치 환경 구축을 위한 다운로드(윈도우즈는 버전의 문제로 docker toolbox를 설치해야 할 수 있다)
  - https://www.docker.com/

# 1. 슬로우ML의 PyTorch 실습을 위한 image pulling & container 실행
* 실습을 위한 이미지는 다음과 같다. 
  - stepankuzmin/pytorch-notebook (실습이 진행됨에 따라 버전이 올라갈 수 있음)
  - 이를 직접 pulling(다운로드)해도 된다.
  - (터미널에서 이 명령 실행) docker pull stepankuzmin/pytorch-notebook
* 그리고 contatiner를 생성하여 실행시켜야 되지만...
* 편하게 docker-compose를 써보자.(2번으로 바로 넘어가서 쭉 해보면 된다)

# 2. 실습을 위한 바벨파이 깃헙 레파지토리 cloning 
* 저장소 주소 
  - https://github.com/psygrammer/SlowML.git
* 자기 컴퓨터로 가져온다. 
  - 1) 직접 터미널에서 명령어로 
    - git clone https://github.com/psygrammer/SlowML.git
  - 2) 혹은 관련 클라이언트로 
  - 3) 혹은 그냥 소스 다운로드 
  - (위의 어떤 방식으로 해도 상관없지만, 기왕이면 1)이나 2)로 하길 추천)
  
# 3. docker-compose 스크립트를 실행시킨다.
* 터미널을 통해서 클로닝한 SlowML 하위 디렉토리 pytorch/docker 안으로 이동한다.
  - cd (설치경로)/SlowML/pytorch/docker
* 디렉토리 안에 docker-compose.yml 파일이 있다.
* 다음의 명령어를 실행 
  - docker-compose up
* 그러면 터미널창에서 노트북이 실행되면서 로그인 토큰까지 결합된 접속 주소가 로그에 나타난다.  
* 여기까지 했으면 해당 url을 통해 jupyter notebook에 접근할 수 있게 된다.
  - 예시) http://localhost:8888/?token=770b8c18096b35053ee827f5d16f830762bf29d4f6374e4b
  - 만약 docker toolbox로 환경을 구축한 사람들은 해당 가상 아이피:8888 로 접속해야 한다.
