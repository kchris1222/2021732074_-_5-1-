# Collaborator, Branch, Merge 기록
작성자: 2021732074 000
협업자: dnfkdjf

## Collaborator 초대
- Settings → Collaborators → dnfkdjf 초대

[스크린샷 삽입 위치]
- Screenshot/step6_invite_collaborator.png

## Branch 생성
- 브랜치 이름 규칙: 학번 + 영문이름
- 사용: 2021732074-kimyonghyeon

```bash
git checkout -b 2021732074-kimyonghyeon
```

[스크린샷 삽입 위치]
- Screenshot/step7_create_branch.png

## 브랜치에서 수정 및 푸시
- 예: README.txt 보강, part 파일 보완

```bash
echo "브랜치 테스트용 문구 추가" >> README.txt

git add README.txt
git commit -m "브랜치에서 README 보강"
git push origin 2021732074-kimyonghyeon
```

[스크린샷 삽입 위치]
- Screenshot/step8_branch_push.png

## Pull Request 생성 및 Merge
- GitHub에서 Compare & pull request → 리뷰 후 Merge

[스크린샷 삽입 위치]
- Screenshot/step9_open_pr.png
- Screenshot/step10_merge_pr.png

## 협업자 작업 시나리오(참고)
- dnfkdjf가 본인 PC에서 Clone
```bash
git clone https://github.com/kchris1222/2021732074_kimyonghyeon.git
cd 2021732074_kimyonghyeon
git checkout -b dnfkdjf-update
# 예: Week5_Summary.md에 한 줄 보완
git add .
git commit -m "협업자: 요약 문구 1줄 보완"
git push origin dnfkdjf-update
```
- PR 생성 → 승인 후 Merge

[스크린샷 삽입 위치]
- Screenshot/step11_collab_push.png
- Screenshot/step12_collab_merge.png
