# 디벗 양품화 메뉴얼

콜센터 상담 참고용 정적 매뉴얼입니다. 순수 HTML·CSS·JavaScript로 구성되어 별도 패키지나 빌드 도구 없이 로컬에서 열거나 GitHub Pages에 배포할 수 있습니다.

## 사이트 열기

[디벗 양품화 메뉴얼 열기](https://hyunjaegit.github.io/yangwiki/)

위 주소는 현재 GitHub 저장소(origin)의 기본 Pages 주소입니다. GitHub Actions 배포가 한 번 성공한 뒤 사용할 수 있습니다.

## GitHub Pages 배포

.github/workflows/deploy-pages.yml이 main 브랜치에 push될 때 자동으로 배포합니다. GitHub 저장소의 Actions 탭에서 Deploy static site to GitHub Pages를 선택해 수동 실행할 수도 있습니다.

최초 배포 전 저장소 Settings → Pages → Build and deployment → Source가 GitHub Actions로 설정되어 있는지 확인하세요. 배포가 끝나면 Actions 실행의 deploy 작업에 표시되는 주소에서 사이트를 엽니다.

배포에는 index.html, pages/, assets/만 포함됩니다. 원본 자료가 있는 reference/, 내부 검토 기록 docs/, 저장소 설정과 기타 파일은 사이트 산출물에 포함하지 않습니다. 공개가 필요한 자료가 생기면 개인정보와 게시 권한을 별도로 검토하세요.

## 로컬 실행 및 확인

- 가장 간단한 방법은 index.html을 브라우저에서 여는 것입니다.
- 정적 서버로 보려면 프로젝트 폴더에서 python -m http.server 8000을 실행한 뒤 http://localhost:8000/을 엽니다. Python은 로컬 미리보기에만 선택적으로 사용하며 사이트 빌드에는 필요하지 않습니다.
- 첫 화면의 두 업무 영역과 학교 7단계 링크, 상세 페이지 메뉴·이전/다음 이동을 확인합니다.
- 전체 페이지 검색 예시: 수리동의서, USB 차단. 결과를 선택해 해당 페이지로 이동합니다.
- 모바일 너비에서 목차와 가로 스크롤 표를 확인하고, 현재 페이지 인쇄 기능을 확인합니다.

## 페이지 구성

- 사업 안내: 사업 개요·전체 흐름, 수거 품목, 현장 점검·판정, 양품화·관리전환·배부
- 학교 업무: 수거 전 준비, OS별 준비, 일정 확인·변경, 수거 당일, 수거확인서, 명렬표·관리전환, 배부·설치 확인
- 문의 경로: 문의 유형별 안내 및 최신 정보 확인 항목
- 공통 자산: assets/css/common.css, assets/js/common.js
- 자료 대조 기록: docs/phase-4-review.md (공개 사이트에는 배포하지 않음)

## 자료와 운영 안내

업무 내용은 제공된 원본 자료와 사용자가 확정한 안내를 바탕으로 작성했습니다. 원본 간 차이나 현재 운영 확인이 필요한 항목은 페이지에서 확인 필요로 안내합니다. 대표번호, 일정, 메뉴명, 학교별 수량 등 변경 가능한 정보는 최신 공문과 시스템을 확인하세요.

학교명·학생명·실제 계정 및 비밀번호, 공식 로고·직인은 게시하지 않습니다. 검색 색인은 현재 공개 HTML 본문을 정적으로 담으므로 HTML 본문·제목·경로를 변경하면 assets/js/common.js의 색인도 함께 갱신해야 합니다.

## 참고 문서

- 프로젝트 작업 지침: AGENTS.md
- 자료 대조·수정·남은 확인 사항: docs/phase-4-review.md
