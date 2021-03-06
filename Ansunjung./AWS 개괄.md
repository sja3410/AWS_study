## AWS란?
+ Amazon에서 제공하는 클라우드 서비스
+ 클라우드에는 **퍼블릭 클라우드**와 **프라이빗 클라우드**로 구분된다. 

## 클라우드란?
+ 컴퓨터의 계산 리소스, 스토리지 영역, 애플리케이션 처리를 네트워크 기반 서비스로 제공하는 것
+ **IaaS, PaaS, Saas**로 구분한다. 


  >#### 인프라스트럭처 서비스(IaaS)
  + **물리장치에 가장 가까운 장치, 가장아래의 장치**
  + 가상 서버 또는 스토리지 등의 리소스를 인터넷을 기반으로 제공하는 서비스
  --------------------------------
  

  >#### 플랫폼 서비스(PaaS)
  + 데이터베이스 또는 애플리케이션 서버 등의 미들웨어를 제공
  --------------------------------
  

  >#### 애플리케이션 서비스(SaaS)
  + **소프트웨어 또는 애플리케이션의 기능을 인터넷을 통해 제공한다.**
  + 메일 서비스, 큐 서비스, 업무 관리 시스템
  ----------------------------------
  


## 물리 서버와 AWS의 차이
+ **물리 서버**: 물리 머신을 한정해서 말하는 것으로, 네트워크 장치 또는 전력설비 등을 포함한다. -**On Premise**
+ 차이는 **소유자**와 **용량**이 있다.

  >**소유자**
  + On Premise : 설비를 준비한 기업이 소유 --> 초기 비용과 시간이 많이 듬
  + AWS : Amazon이 모든 리소시를 소유 --> 초기 비용이 거의 들지 않음, 초기 시간이 많이들지 않음. 
  + **소유자와 사용자가 다르다-AWS**
  
  >**용량**
  + On Premise : 용량변경을 위해서는 시간과 비용이 많이 듬 --> 많고, 적을 것에 대해 대비해야함
  + AWS : 용량변경이 쉬움 --> 많고, 적을 것에 대해 유동적으로 변경해야함 --> **적게 사용시 적은 비용**
  
  
  
  >><img src = "https://user-images.githubusercontent.com/55094745/103612904-c24dbe00-4f68-11eb-84d1-b03af401c516.png" width= "30%"></img>
  <img src = "https://user-images.githubusercontent.com/55094745/103613297-a860ab00-4f69-11eb-906f-ce9fce9c4da7.png" width= "30%"></img>
  ----------------------------------
  
## 렌탈 서버(공유 서버)와 AWS의 차이

### 렌탈서버
+ **호스팅 서버**, **공용 서버**라고도 한다.
+ **전용 서버**: 1대의 물리 서버를 모두 점유 --> 비용을 줄이고, 공용 서버에 비해서는 거의 영향을 받지 않는다.
+ **가상 전용서버**: 1대의 물리 서버 위에 가상 서버를 여러 개 만들고, 해당 가상 서버를 점유
+ 여러 사용자가 공유하기 때문에 **자유도가 낮고**, **다른 사용자의 영향이 크다** 
>> - 사용자의 권한만 부여하고, 관리자 권한이 부여되지 않아 버전 변경을 못한다. 
>> - 다른사람이 만든 애플리케이션에 취약점이 발견되면 그 취약점에 영향을 받는다.


### 렌탈 서버와 AWS의 차이
> AWS의 가상 컴퓨터 서비스 EC2는 가상 전용 서버와 비슷하지만, 기존의 렌탈 서버에 없는 기능이 많다. 즉, 추가적인 서비스를 더 제공한다는 점에서 다르다.
-------------------------------------------


## 프라이빗 클라우드와 AWS

### 클라우드의 종류
+ **퍼블릭 클라우드**: 불트정 다수의 사용자에게 제공되는 서비스
+ **프라이빗 클라우드**: 특정 기업/조직 전용으로 제공되는 서비스
+ **하이브리드 클라우드**: 퍼블릭 클라우드와 프라이빗 클라우드를 조합
+ **커뮤니티 클라우드**: 특정 업종들의 기업들이 함께 운영

> AWS에서는 VPC서비스로 가상 네트워크를 만들때 내부에서 서브넷을 생성하거나, IP 주소 범위, 라우트 테이블, 네트워크 게이트웨이 등을 자유롭게 설정 가능--> 범위를 지정해서 프라이빗하게 사용은 가능

### 서비스 종류

  > + **EC2**: 가상서버(인스턴스)
  > + **ELB**: 부하 분산 장치, 여러 개의 EC2인스턴스에 통신을 분산해줌
  > + **Auto Scaling**: CPU 또는 메모리 사용량에 따라 EC2인스턴스를 자동으로 늘리고 줄여줌
  
  <image src="https://user-images.githubusercontent.com/55094745/103615980-ead8b680-4f6e-11eb-984b-3320c8f53d5f.png" width = "50%"></img>
  
  > + **S3**: 온라인 스토리지 서비스(내구성, 가용성, 신뢰성, 안정성, 무제한적인 용량), http/https를 통한 api사용
  > + **Amazon Clacier**: 데이터 장기 보관, s3의 1/3의 비용으로 사용
  > + **EBS**: EC2에서 사용하는 외장 하드디스크
  
  > + **RDS**: 데이터베이스 PaaS
  > + **Amazon ElastiCache**: 메모리 캐시 시스템 PaaS, RDS와 같은 풀 매니지먼트 서비스
  > + **VPC**: AWS 네트워크 내부에서 논리적으로 분리되 네트워크를 생성하는 서비스
  > + **AWS Direct Connect**: VPC에 접속하기 위한 전용선 접속 서비스
  > + **Amazon CloudFront**: 콘텐츠 전송 네트워크 서비스, 콘텐츠를 엣지 로케이션이라고 부르는 전세계 거점을 기반으로 전달
  > + **Amazon Route 53**: 도메인 이름 시스템 
  > + **SQS**: 메시지 큐 서비스(메시지의 가용성, 확장성, 큐 시스템의 신뢰성)
  > + **SES**: 메일 전송 서비스
  > + **IAM**: 계정 관리 서비스
  > + **AWS CloudTrail**: AWS API 호출을 기록하는 로깅서비스
  > + **Amazon CloudWatch**: AWS의 리소스 또는 애플리케이션 모니터링 서비스
  > + **AWS Elastic Beanstalk**: 웹 애플리케이션 서버 PaaS, 서버를 구축하지 않고도 플랫폼 사용가능
  > + **AWS CloudFormation**: AWS 환경 구축 자동화 
  > + ///등등 여러 서비스 계속 추가중



  
  
