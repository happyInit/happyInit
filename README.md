### 김봉수 · 클라우드 인프라 엔지니어

프론트엔드 개발을 2년 하다가 인프라로 넘어왔습니다.
팀 프로젝트에서 서비스를 컨테이너로 만들고, 물리 서버 3대에 온프레미스 Kubernetes를 올린 뒤, 같은 구성을 AWS EKS로 옮기는 작업을 인프라 담당으로 맡았습니다.

- 포트폴리오: https://bongsu.cloud
- 자격: CKA (2026.09)
- 메일: kbs48631@gmail.com

#### 밀플래닝 · 월 식비 예산 기반 식단 서비스

2026.06–08 · 5명 · 인프라 리드 · 더존비즈온 최우수상 · [app.mealbong.cloud](https://app.mealbong.cloud)

| 레포 | 내용 |
|---|---|
| [food-budget-app](https://github.com/happyInit/food-budget-app) | 앱 소스(13개 서비스), Terraform · Ansible, 설계 문서와 결정 기록 |
| [mealplanning-config](https://github.com/happyInit/mealplanning-config) | ArgoCD가 배포하는 K8s 매니페스트 (온프렘 · EKS 오버레이) |

먼저 보면 좋은 곳

- 카나리 배포와 자동 분석 · 롤백: [Rollout](https://github.com/happyInit/mealplanning-config/blob/main/services/account/base/rollout.yaml) · [AnalysisTemplate](https://github.com/happyInit/mealplanning-config/blob/main/services/account/base/analysistemplate.yaml) · [결정 기록](https://github.com/happyInit/food-budget-app/blob/main/docs/adr/0001-deployment-strategy-canary.md)
- EKS 인프라 Terraform (VPC · EKS · Karpenter · ALB · WAF): [infra/terraform/aws-platform](https://github.com/happyInit/food-budget-app/tree/main/infra/terraform/aws-platform)
- AWS 이관 때 내린 결정과 이유: [mp_aws_prep_checklist.md](https://github.com/happyInit/food-budget-app/blob/main/docs/mp_aws_prep_checklist.md)

두 레포 모두 팀 프로젝트라 팀원 작업도 함께 들어 있습니다. 제가 맡은 부분은 [포트폴리오](https://bongsu.cloud)에 정리했습니다.
