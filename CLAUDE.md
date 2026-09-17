# 픽온(PICKON) 마케팅 프로젝트



##  프로젝트 설명

-업종: 1인 사업자 온라인 스마트스토어 운영
-타겟: 25세~40세 직장인 여성,  남성
-주요 채널: 스마트스토어, 블로그, 인스타그램, 스레드
-이번 분기 목표: 스마트스토어 수익 월 50만원, 블로그 검색 유입 월 3,000회

## 공통 규칙

-모든 콘텐츠는 brand-voice 톤을 따른다
-결과물은 output 폴더에 날짜를 붙여 저장한다
 -파일명: 'YYYY-MM-DD-종류-주제.md' (예: '2026-08-12-blog-1인사업자-ai-마케팅-트렌드.md')
 -종류: blog  ·  sns  ·  newsletter  ·  ad  · research
-검증되지 않은 숫자나 통계는 인용하지 않는다
-경쟁 서비스를 깎아내리지 않는다
-트렌드 조사 · 경쟁 분석 등은 발행용 콘텐츠가 아니라 조사 참고용 내부자료(research)다


## 조사 참고 자료(research) 규칙
-발행용이 아닌 내부 참고용이며, 그대로 블로그 · SNS 등에 발행하지 않는다
-output 폴더에 저장하되 파일명 앞에 날짜, 뒤에 접미사 `-research`를 붙인다 (예: `2026-09-01-competitor_analysis-research.md`)
-문서 첫머리에 조사일 · 조사 도구 · 출처를 명시한다
-발행물에 활용할 때는 반드시 seo-checklist 검수를 거친다



## 라우팅 규칙
-블로그 글(SEO · 검색 유입 목적, PICKON 고객 대상) → blog-writer 스킬
-SNS 캡션 → sns-caption
-뉴스레터 → email-newsletter
-광고 카피 → ad-copy
-발행 전 검수 → seo-checklist
-뷰티 인스타 릴스 · 블로그(30대 여성 타겟) → beauty-writer 서브에이전트 (.claude/agents/beauty-writer.md, 스킬이 아님)
-경쟁사 · 시장 조사 → researcher 서브에이전트 (.claude/agents/researcher.md, 스킬이 아님)
-리서치 자료 기반 블로그(1인 사업가 대상, 새 정보 추가 없이 리서치 자료만 사용) → blog-writer-research 서브에이전트 (.claude/agents/blog-writer-research.md, 스킬이 아님. blog-writer 스킬과 이름이 비슷하니 혼동하지 말 것)
-맞춤법 · 문장 구조 · 톤 교정(내용 변경 없이 다듬기만) → editor 서브에이전트 (.claude/agents/editor.md, 스킬이 아님)
-output/의 승인된 초안을 blog/articles로 발행(사본 저장, 내용 변경 없음, output 원본 유지) → publisher 서브에이전트 (.claude/agents/publisher.md, 스킬이 아님)


## 모델 배정
각 스킬의 frontmatter 'model' 필드로 적용되어 있다. 스킬을 쓰면 해당 모델로 자동 전환된다.

-조사 · 정리 → Haiku (seo-checklist, researcher 서브에이전트)
-글 작성 → Sonnet (blog-writer, blog-writer-research, beauty-writer, sns-caption, email-newsletter, ad-copy)
-교정 → Sonnet (editor 서브에이전트)
-발행(파일 저장) → Haiku (publisher 서브에이전트)
-전략 · 기획: Opus (스킬 없이 전행하는 기획 대화)

## 참고

-'content/' 폴더의 악세러리 관련 글은 이전 브랜드의 자료다. 현재 기준과 다르므로 참고하지 않는다.

