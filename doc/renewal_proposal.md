# Ryu Clinic 웹사이트 리디자인 제안서

사용자님은 **12년 차 소프트웨어 엔지니어**이자 **13년 차 한의사**라는 매우 독보적인 배경(Unique Value Proposition)을 가지고 계십니다. 따라서 웹사이트는 일반적인 로컬 클리닉 홈페이지를 넘어, **"데이터와 기술 기반의 신뢰할 수 있는 현대적 의료 서비스"**라는 브랜딩이 필요합니다.

기존 Jekyll 및 Github Pages 구조를 유지하면서, 향후 AI 서비스 확장을 고려한 모던한 리디자인 전략입니다.

---

### 1. 브랜드 아이덴티티 & 디자인 컨셉 (UI/UX)

**컨셉: "Rational Healing (이성적 치유)"**
따뜻한 감성의 한의학(TCM)에 차가운 이성의 기술(Tech)을 결합하여 '신뢰감'을 주는 디자인입니다.

* **Color Palette:**
  * **Primary:** Deep Teal (#006D77) - 의료의 신뢰감과 안정감.
  * **Secondary:** Slate Grey (#2F4858) - 엔지니어링, 모던함, 텍스트 가독성.
  * **Accent:** Electric Blue (#4CC9F0) - AI, 테크놀로지, 혁신 (버튼 및 하이라이트 요소).
  * **Background:** Clean White & Light Gray - 여백의 미를 살린 모던함.

* **Typography:** 가독성이 뛰어난 Sans-serif 계열 (예: **Inter** 또는 **Noto Sans KR/EN**)을 사용하여 모던하고 IT 서비스 사이트 같은 느낌을 줍니다.
* **Layout:** 카드(Card) UI와 그리드 시스템을 활용하여 향후 개발될 앱/서비스를 쇼케이스 형태로 보여주기 쉽게 구성합니다.

### 2. 사이트 아키텍처 (Sitemap Structure)

기존 클리닉 정보와 미래의 테크 서비스를 자연스럽게 연결하는 구조입니다.

1. **Home:**
   * **Hero Section:** "Engineering Better Health" (가제). 한의사이자 개발자가 운영하는 데이터 기반 클리닉임을 한 줄로 명시.
   * **Hybrid Feature:** [진료 예약하기] 버튼과 [Ryu Lab/Projects] 버튼의 듀얼 액션.

2. **About (The Hybrid Practitioner):**
   * 한의사로서의 경력 + 소프트웨어 엔지니어로서의 경력 스토리텔링.
   * 마라톤 러너로서의 경험을 녹여 '스포츠 의학/퍼포먼스 향상' 전문성 강조.

3. **Services (Clinical):**
   * 통증 치료, 내과 질환 등 기존 진료 과목.
   * *SEO 포인트:* 밴쿠버 지역명 + 증상 키워드 최적화.

4. **R-Lab (또는 Tech & AI):** *(신설)*
   * 향후 개발할 AI 툴, 헬스케어 앱, 데이터 분석 도구를 소개하는 섹션.
   * 현재는 "Coming Soon" 또는 개발 철학(Vision)을 담고, 추후 각 서비스의 랜딩 페이지로 연결.

5. **Blog/Insights:**
   * 건강 정보(TCM) + 헬스 테크(Tech) 관련 글을 혼합하여 발행.
   * 구글 검색 상위 노출(SEO)을 위한 핵심 엔진 역할.

6. **Contact/Booking:**
   * Janeapp 연동 예약, 위치(Google Maps), 진료 시간.

### 3. 기술 스택 및 구현 전략 (Jekyll + Github Pages)

기존 `Github Pages` 호스팅을 유지하면서 디자인과 확장성을 현대화합니다.

* **CSS Framework: Tailwind CSS**
  * **이유:** 기존의 무거운 테마를 벗어던지고, 빠르고 커스터마이징이 쉬운 유틸리티 퍼스트 CSS를 도입합니다. Jekyll 플러그인이나 PostCSS로 빌드 타임에 통합 가능합니다. 모바일 반응형 구현이 매우 쉽습니다.

* **Template Engine: Liquid (Jekyll Native)**
  * **Layout 분리:** `_layouts/default.html`, `_layouts/post.html`, `_layouts/project.html` (신규 앱 소개용) 등으로 템플릿을 모듈화합니다.

* **Data Management: `_data` 폴더 활용**
  * `services.yml`, `projects.yml` 등으로 콘텐츠를 데이터 파일로 관리하여, 추후 AI 서비스가 추가될 때 HTML 수정 없이 YAML 파일만 업데이트하면 리스트에 자동 반영되도록 설계합니다.

### 4. SEO (검색 엔진 최적화) 전략

구글 검색 상위 노출을 위한 기술적 SEO를 적용합니다.

* **JSON-LD (Schema Markup) 강화:**
  * `LocalBusiness` (한의원) 스키마와 `SoftwareApplication` (개발할 앱) 스키마를 동시에 적용합니다. 구글이 이 사이트를 "진료도 하고 소프트웨어도 개발하는 곳"으로 명확히 인식하게 합니다.

* **Performance (Core Web Vitals):**
  * Jekyll은 정적 사이트라 속도가 빠르지만, 이미지 포맷(WebP 사용)과 Tailwind의 PurgeCSS를 사용하여 로딩 속도를 극대화합니다. (검색 랭킹 중요 요소)

* **Keyword Strategy:**
  * Primary: "Vancouver Acupuncture", "Coquitlam TCM", "Korean Herbal Medicine Vancouver".
  * Secondary (Niche): "AI Healthcare Solutions", "Data-driven TCM", "Sports Medicine Engineering".

### 5. 구현 예시 (디렉토리 및 코드 구조)

기존 Jekyll 구조에 `projects` 컬렉션을 추가하는 것이 핵심입니다.

**`_config.yml` 설정 추가:**

```yaml
collections:
  projects:
    output: true
    permalink: /lab/:path/

# SEO 설정
title: Ryu Clinic & Lab
description: Evidence-based Acupuncture and AI-driven Healthcare Solutions in Vancouver.
plugins:
  - jekyll-seo-tag
  - jekyll-sitemap
```

**`_data/projects.yml` (미래의 앱 서비스 관리):**

```yaml
- name: "ChartAI (가칭)"
  status: "In Development"
  description: "AI-powered SOAP note generator for TCM practitioners."
  tech_stack: ["Python", "OpenAI API", "JaneApp Integration"]
  image: "/assets/img/project-ai.jpg"
```

**메인 페이지 (`index.html`) 섹션 구성안:**

```html
<section class="bg-white dark:bg-slate-900">
  <div class="container px-6 py-16 mx-auto text-center">
    <h1 class="text-4xl font-bold text-gray-800 dark:text-white">
      Traditional Healing, <span class="text-blue-500">Enhanced by Technology</span>
    </h1>
    <p class="mt-4 text-gray-500">
      소프트웨어 엔지니어링의 정밀함으로 완성하는 류 클리닉의 맞춤형 한방 치료
    </p>
    <div class="flex justify-center mt-8 gap-4">
        <a href="https://ryu.clinic/booking" class="px-6 py-2 text-white bg-teal-600 rounded-lg hover:bg-teal-500">진료 예약하기</a>
        <a href="/lab" class="px-6 py-2 text-gray-700 border border-gray-300 rounded-lg hover:bg-gray-100">R-Lab 프로젝트</a>
    </div>
  </div>
</section>
```

### 6. 실행 로드맵

1. **Backup & Branch:** 현재 리포지토리에서 `dev-2026-renew` 브랜치 생성.
2. **Clean Up:** 기존 테마 의존성 제거 및 Tailwind CSS 설치.
3. **Layout Refactoring:**
   * Header: 로고, 네비게이션 (Clinic / Lab / Blog / Contact).
   * Body: 위에서 제안한 섹션별 컴포넌트화.
4. **New Content:** 'About Me' 페이지를 엔지니어+한의사 융합 관점으로 재작성.
