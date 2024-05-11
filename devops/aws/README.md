# AWS

## CloudWatch
- link : [Filter pattern](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html#matching-terms-events)
    - JSON로그 검색방법
        - ex
            ```
                { $.name = %아무개% } // 아무개 contain
                { $.name = 아무개 } // 아무개 equal
                { ($.name = %아무개%) && ($.age = 10) } // name 아무개 contain and age 10 equal
            ```

## S3
- link : [S3 정적 웹사이트 호스팅](https://inpa.tistory.com/entry/AWS-%F0%9F%93%9A-S3-%EC%A0%95%EC%A0%81-%EC%9B%B9-%EC%82%AC%EC%9D%B4%ED%8A%B8-%ED%98%B8%EC%8A%A4%ED%8C%85-%EB%8F%84%EB%A9%94%EC%9D%B8-%EC%84%A4%EC%A0%95Route-53)
    - link : [정적 웹사이트 호스팅에 https 적용](https://sleepybird.tistory.com/144)

## VPN 서버 구축
- link : [AWS EC2 - OpenVPN 연동기](https://elishaz.tistory.com/280)

## IAM
- link : [MFA 디바이스 할당](https://lamanus.kr/106)
- link : [개발자용 IAM 생성방법](https://ncookie21.tistory.com/18)

## EC2
- link : [aws 공식문서(연결 유휴 제한 시간)](https://docs.aws.amazon.com/ko_kr/elasticloadbalancing/latest/application/application-load-balancers.html#connection-idle-timeout)
- link : [NestJS 혹은 Express에서 간헐적으로 502 응답이 오는 경우](https://velog.io/@dramatic/NestJS-%ED%98%B9%EC%9D%80-Express%EC%97%90%EC%84%9C-%EA%B0%84%ED%97%90%EC%A0%81%EC%9C%BC%EB%A1%9C-502-%EC%9D%91%EB%8B%B5%EC%9D%B4-%EC%98%A4%EB%8A%94-%EA%B2%BD%EC%9A%B0)
- link : [AWS 502 error on ALB](https://ivorycirrus.github.io/TIL/aws-alb-502-bad-gateway/)
- link : [AWS Beanstalk 구성파일(.ebextensions)을 사용하여 환경 구성하기](https://ibks-platform.tistory.com/174)
- link : [AWS t4g 인스턴스 사용기 (with 도커)](https://velog.io/@infl_veggie/AWS-t4g-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4-%EC%82%AC%EC%9A%A9%EA%B8%B0-with-%EB%8F%84%EC%BB%A4)

### 스팟 인스턴스
- link : [스팟 인스턴스 정보](https://blog.leedoing.com/178)

## Elastic Beanstalk(EB)
- link : [9분 59초 만에 Github Action + AWS Elastic Beanstalk로 TS 프로젝트 CI/CD 파이프라인 구축하기](https://bluayer.com/46)

## CodePipeline
- link : [CodePipeline 과 CodeDeploy만으로 배포 자동화하기](https://senticoding.tistory.com/93)

## EKS
- link : [istio + NLB 삽질기](https://www.clud.me/11354dd3-48f3-454d-917f-eca8d975e034)
- link : [EKS 튜토리얼 part1](https://cwal.tistory.com/33)

## ECS
- 로그 설정하기
    - logConfiguration
    - 요 부분은 블로그에 작성하고 링크 여기 달기
- link : [ECS 톺아보기](https://blog.doctor-cha.com/ecs-in-depth#gijon-inpeura-guseong)

## RDS
- link : [RDS가 퍼블릭 서브넷에 속해있는데 퍼블릭 접근이 안되는 건에 대하여](https://repost.aws/ko/knowledge-center/rds-connectivity-instance-subnet-vpc)
- rdsadmin 권한으로 parameter 수정하기
- parameter group 수정하기
- 직접적으로 rdsadmin 으로 로그인해서 수정하는 것 불가능

## VPC
- link : [VPC 쉽게 이해하기](https://aws-hyoh.tistory.com/53)
- link : [Private IP of an EC2 instance](https://stackoverflow.com/questions/53180107/private-ip-of-an-ec2-instance)
- link : [가장쉽게 VPC 개념잡기](https://medium.com/harrythegreat/aws-%EA%B0%80%EC%9E%A5%EC%89%BD%EA%B2%8C-vpc-%EA%B0%9C%EB%85%90%EC%9E%A1%EA%B8%B0-71eef95a7098)

### Routing table
- link : [라우팅 테이블 해석하는 방법](https://stevenjsmin.tistory.com/m/195)
- link : [라우팅 테이블에 대한 이해](https://codemonkyu.tistory.com/entry/AWS-VPC-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-23)

### ACL
- link : [ACL에 대한 이해](https://rachel0115.tistory.com/entry/AWS-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-ACL-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0-NACL)

## Parameter Store
- link : [파라미터 스토어](https://gksdudrb922.tistory.com/199)