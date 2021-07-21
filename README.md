# prerequisites 

## Create S3 Bucket
먼저 training, validation 그리고 모델 output 에 사용할 s3 bucket 을 만듭니다. [Amazon S3 console](https://s3.console.aws.amazon.com/)

Create Bucket 버튼을 누르면 아래와 같은 화면이 나옵니다.
![image](https://user-images.githubusercontent.com/13167486/126520072-85a21cb8-5773-4a91-acb3-3b1b39ce42d6.png)

Region 은 Asis Pacific(Seoul) ap-northeast-2 를 선택합니다.

선택 완료 후, Create Bucket 버튼을 누릅니다.

## Create SageMaker Notebook

다음은 같은 Region 의 Amazon SageMaker console 에 접속합니다. [Amazon SageMaker Console](https://console.aws.amazon.com/sagemaker/)

왼쪽 메뉴에서 Notebook 을 확장하고 Notebook Instances 를 선택합니다.

![image](https://user-images.githubusercontent.com/13167486/126521280-38665eb0-6884-478c-9df9-6ba53dc1f26b.png)

Create Notebook instance 를 클릭합니다.

![image](https://user-images.githubusercontent.com/13167486/126521346-8099dccb-9f76-41aa-8950-59687309c466.png)

노트북 인스턴스 셋팅 화면에서 노트북 이름을 정하고 인스턴스 타입은 ml.t2.medium 을 선택합니다.

IAM Role 에서 Create a new role 을 선택합니다.

![image](https://user-images.githubusercontent.com/13167486/126525973-05bffff1-bcc7-4770-b6cf-b2b9b8994d7c.png)

Create role 을 선택하고, HOL 을 위해서 Any S3 bucket 을 선택합니다.

![image](https://user-images.githubusercontent.com/13167486/126526213-2e08ab2a-dd62-4bf3-b178-054a55589c0d.png)

IAM Role 이 만들어지면 Create Notebook instance 를 클릭합니다.

![image](https://user-images.githubusercontent.com/13167486/126526381-4dafdf9d-727c-4556-992e-9aaa14448258.png)

노트북이 만들어지면 클래식 노트북과 쥬피터 랩 중 하나를 선택할 수 있습니다.

![image](https://user-images.githubusercontent.com/13167486/126526485-b4ccc937-d8a6-4780-affb-db8b89dc2a53.png)

쥬피터 노트북이 만들어지면 New 버튼을 누르고, conda_python3 라는 커널을 선택합니다.

![image](https://user-images.githubusercontent.com/13167486/126526595-ac28c2b8-02ff-461b-acc0-97e335c03556.png)

노트북이 만들어지면 아래의 Git 명령어를 실행합니다.

!git clone https://github.com/lunarian60/direct-marketing.git

![image](https://user-images.githubusercontent.com/13167486/126526682-4dc805e6-4030-43a4-a276-eb3fe0492464.png)
