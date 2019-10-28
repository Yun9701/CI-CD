# CI/CD란 무엇인가?
--------------------
# 목차

## 1. <a href='#devops'>Devops</a>  
## 2. <a href='#cicd'>CI/CD</a> 
## 3. <a href='#cicdtool'>CI/CD Tool</a> 

--------------------
<br><br>
<a name='devops'></a>
# 1. Devops
CI/CD가 무엇인지 알기전에, CI/CD가 필요한 이유에 대해서 알아보자.  
Devops란 시작은 개발조직과 운영조직의 벽을 최소화하자는 개념에서 시작하였고, 현재는 비즈니스 조직과 IT 조직의 협업을 강화하자는 개념으로 쓰인다. 즉, 고객과 업무를 가장 잘 이해하고 있는 비즈니스 조직의 생각과 아이디어가 실제적인 IT 서비스로 빠르게 구현되기 위함이다.  
Devops에서 중요한 것은 speed와 iteration이다. 이는 비즈니스 조직의 요구에 빠르게 대처하고 지속적으로 개선을 할 수 있어아야한다는 것을 의미한다. 따라서, 이를 가능하게 하기 위해 CI/CD 자동화가 필요하다. 그럼 이제 CI/CD가 무엇인지 알아보자.


--------------------
<br><br>
<a name='cicd'></a>
# 2. CI/CD  
 - CI/CD 파이프라인  
CI/CD 파이프라인은 코드 통합, 테스트, 릴리즈, 배포하는 과정을 자동화하고, 모니터링이 가능하도록 하는 것이다. 이를 자동화하는 것은 개발자가 애플리케이션에 코드변경을 하면 몇분이내에 애플리케이션에서 실행될 수 있도록 하는 것을 의미한다.

## - CI(continuous integration)  
CI는 "지속적인 통합"으로 개발자를 위한 통합준비 및 통합 자동화 프로세스이다.  
보통, 개발은 팀을 이뤄 진행하게 된다. 개발조직은 적게는 5명부터 많게는 100명까지 많은 조직원들로 팀을 이루게 된다. 하나의 어플리케이션내에서 여러 조직원들이 개발을 하게 되면 하루에 수십개의 코드 변경이 일어난다. 그러다보니 코드 변경 사항이 공유 레퍼지토리에 병함될 때 서로 충돌이 일어나게 된다. 하지만, CI는 애플리케이션에 대한 새로운 코드 변경 사항이 정기적으로 빌드 및 테스트되어 공유 레포지토리에 병합이는 방식이므로 CI를 성공적으로 구현하게 되면 여러 명의 개발자가 동시에 한 애플리케이션에 대한 코드 작업을 할 경우에 일어나는 충돌 문제를 해결할 수 있다.

## - CD(continuous delivery)
CD 중 Continuous Delivery는 "지속적인 서비스 제공"으로 운영팀을 위한 배포준비 자동화 프로세스이다.  
이 지속적인 제공 프로세스는 최소한의 노력으로 새로운 코드를 배포하는 것을 목표로한다. 즉, 프로덕션 환경으로 배포할 준비가 완료된 코드를 확보하는 것이다.  
이 프로세스는 개발자들이 변경한 사항이 버그테스트를 거쳐 레포지토리에 자동으로 릴리즈되는 방식이고, 이 지속적인 제공 프로세스를 완료하면 운영팀이 보다 빠르고 쉽게 개발된 애플리케이션을 프로덕션으로 배포할 수 있다. 이는 개발자는 개발에만 몰두하고 운영팀은 쉽게 배포를 할 수 있다는 점에서 개발팀과 비즈니스팀 간의 커뮤니케이션 문제를 해결해준다.  

## - CD(continuous deployment)
CD 중 Continuous Deployment는 "지속적인 배포"로 운영팀을 위한 배포 자동화 프로세스이다.  
이 프로세스는 레퍼지토리에서 고객이 사용 가능한 프로덕션 환경까지 자동으로 릴리즈하는 방식으로, CI/CD 파이프라인의 마지막 단계이다.

<img width="800" alt="CICD사진2" src="https://user-images.githubusercontent.com/28242106/67655949-c316b780-f995-11e9-955d-1e7d2db3d353.PNG"> 

--------------------
<br><br>
<a name='cicdtool'></a>
# 3. CI/CD Tool
## - Jenkins
Java로 작성된 오픈소스 소프트웨어로 가장 오래되고 인기 있는 CI tool이다. 개발자가 직접 CI/CD 환경을 설정할 수 있고, Subversion, Git, Mercurial, Maven과 같은 버전 제어 도구를 지원한다. 문서화가 잘 되어 있고, 블루오션이라는 새로운 인터페이스와 수천개의 플러그 인으로 인해 매우 유연하고 확장성이 높다. 따라서, 맞춤화가 필요한 대형 프로젝트에 효과적이다.

## - Travis CI
Travis CI은 최초의 호스팅 CI서버이고 자체적 서버도 제공한다. Github 프로젝트를 위해 특별히 호스팅된 서버로 시작하기가 편하다. 그리고 다양한 언어를 지원하며 수많은 다른 빌드 툴 및 배포 대상과 통합된다.  


<img width="600" alt="CICDtool" src="https://user-images.githubusercontent.com/28242106/67656051-083ae980-f996-11e9-834d-4314669cf461.png">  

그림출처 - <https://www.altexsoft.com/blog/engineering/comparison-of-most-popular-continuous-integration-tools-jenkins-teamcity-bamboo-travis-ci-and-more/>



