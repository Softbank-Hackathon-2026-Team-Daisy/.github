# 🌼 Team Daisy — One Action, Infinite Clouds

**AI 기반 온프레미스·퍼블릭 클라우드 원터치 배포 시스템**
SoftBank Hackathon 2026 in Korea 예선 (Term1)

배포 환경만 선택하면 AI가 환경별 인프라 코드(Terraform)를 생성·검증해서, **같은 애플리케이션을 온프레미스와 퍼블릭 클라우드에 동시에 배포**해요.

```
main merge → GitHub Actions 이미지 빌드 (커밋 해시 태그)
→ 환경 선택 (온프레미스 · AWS · GCP)
→ AI가 deploy.yaml로 환경별 Terraform 생성
→ validate · plan · 위험 설정 검사 (실패 시 AI 수정, 최대 3회)
→ 사람이 plan 승인 → 환경별 병렬 apply
```

핵심 키워드는 **이식성**이에요. 한 번 빌드한 같은 이미지를 모든 환경에 같은 상태로 올려요.

## Repositories

| 레포 | 설명 |
|---|---|
| [`daisy`](../../daisy) | 우리 배포 시스템 (웹 대시보드 · Swift 앱 · 배포 서비스 · 환경별 기준 Terraform 모듈) |
| [`sample-monolith`](../../sample-monolith) | 배포 대상 샘플 앱 — 모놀리스 + GitHub Actions 이미지 파이프라인 |
| [`sample-msa`](../../sample-msa) | 배포 대상 샘플 앱 — 서비스 2개짜리 MSA |
| [`.github`](../../.github) | 조직 공통 이슈·PR 템플릿, 이 소개 페이지 |

## Tech

| 영역 | 스택 |
|---|---|
| Web | React · Vite · TypeScript · Tailwind |
| iOS | Swift |
| Server | `[미정]` Spring Boot / TypeScript / FastAPI |
| IaC | Terraform |
| 대상 환경 | 온프레미스 (Docker) · AWS (ECS · ALB · RDS) · GCP (Cloud Run · Cloud SQL) |
| CI | GitHub Actions |

## Team

| 이름 | 역할 |
|---|---|
| 김도영 | 팀장 · Web FE · CI |
| 박승준 | Web FE · iOS |
| 하은현 | Web BE (API · 흐름) |
| 김승환 | Web BE (AI · 검증) |
| 황지환 | Infra · 온프레미스 |
| 임채준 | Infra · 클라우드 |
