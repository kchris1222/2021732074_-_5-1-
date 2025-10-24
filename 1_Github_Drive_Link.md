# GitHub 생성 및 Google Drive 연동 기록
작성자: 2021732074 000
저장소: 2021732074_kimyonghyeon

## 저장소 생성
- GitHub에서 새 저장소 생성
- 이름: 2021732074_kimyonghyeon
- Public, README 생성

[스크린샷 삽입 위치]
- Screenshot/step1_repo_create.png

## 로컬(구글 드라이브 폴더) 연동
- 로컬 경로: 내 구글 드라이브 폴더

```bash
cd "내_구글드라이브_경로"
git clone https://github.com/kchris1222/2021732074_kimyonghyeon.git
cd 2021732074_kimyonghyeon
```

[스크린샷 삽입 위치]
- Screenshot/step2_drive_clone.png

## 초기 커밋 업로드
- Week5_Summary.md와 이 파일 포함하여 커밋

```bash
git add .
git commit -m "초기 세팅: 요약본 및 연동 기록 추가"
git push origin main
```

[스크린샷 삽입 위치]
- Screenshot/step3_first_push.png
