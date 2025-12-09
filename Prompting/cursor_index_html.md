# Index.html 파일 용도 문의
_Exported on 12/9/2025 at 11:27:59 GMT+9 from Cursor (2.1.50)_

---

**User**

@Index.html 이 파일이 무엇을 할때 쓰는 파일일까?

---

**Cursor**


파일 내용 확인 중입니다.



현재 `Index.html`은 비어 있습니다.

**Index.html**은 웹 프로젝트의 진입점(entry point)으로 사용됩니다:

1. **웹사이트의 메인 페이지**: 브라우저가 웹사이트의 루트 디렉토리를 열 때 기본으로 표시되는 파일입니다.
2. **HTML 문서의 시작점**: 웹페이지의 구조와 내용을 정의하는 HTML 마크업을 포함합니다.
3. **웹 서버의 기본 파일**: 대부분의 웹 서버는 디렉토리 요청 시 `index.html`을 자동으로 제공합니다.

일반적으로 다음과 같은 기본 구조를 포함합니다:
- `<!DOCTYPE html>` 선언
- `<html>`, `<head>`, `<body>` 태그
- 메타데이터, 제목, 스타일시트 링크
- 페이지의 실제 콘텐츠

기본 HTML 템플릿을 추가할까요?

---

**User**

“새로운시작(New Star)”을알리는신제품, 신기술홍보용웹사이트를단일페이지웹앱으로만들어줄수있을까? 흔한디자인이어도상관없어. 그리고작업후결과를Report 폴더를만든후마크다운파일로만들어저장해줘.

---

**Cursor**


"새로운시작(New Star)" 신제품/신기술 홍보용 단일 페이지 웹앱을 만들고, 작업 결과를 Report 폴더의 마크다운 파일로 저장합니다.


```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Star - 새로운 시작</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* 헤더 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* 히어로 섹션 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: move 20s linear infinite;
        }

        @keyframes move {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* 특징 섹션 */
        .features {
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        /* 기술 섹션 */
        .technology {
            background: white;
        }

        .tech-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tech-item {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        .tech-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        /* 제품 섹션 */
        .products {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* 연락처 섹션 */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        /* 푸터 */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* 스크롤 애니메이션 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- 헤더 -->
    <header>
        <nav>
            <div class="logo">New Star</div>
            <ul class="nav-links">
                <li><a href="#home">홈</a></li>
                <li><a href="#features">특징</a></li>
                <li><a href="#technology">기술</a></li>
                <li><a href="#products">제품</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>
    </header>

    <!-- 히어로 섹션 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>새로운 시작, New Star</h1>
            <p>혁신적인 기술로 미래를 만들어갑니다</p>
            <a href="#features" class="cta-button">더 알아보기</a>
        </div>
    </section>

    <!-- 특징 섹션 -->
    <section class="features" id="features">
        <h2 class="section-title fade-in">주요 특징</h2>
        <div class="features-grid">
            <div class="feature-card fade-in">
                <div class="feature-icon">🚀</div>
                <h3>혁신적인 성능</h3>
                <p>최신 기술을 활용한 뛰어난 성능으로 사용자 경험을 한 단계 끌어올립니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">✨</div>
                <h3>직관적인 디자인</h3>
                <p>사용자 중심의 깔끔하고 직관적인 인터페이스로 누구나 쉽게 사용할 수 있습니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🔒</div>
                <h3>안전한 보안</h3>
                <p>최고 수준의 보안 시스템으로 사용자의 데이터를 안전하게 보호합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">⚡</div>
                <h3>빠른 속도</h3>
                <p>최적화된 알고리즘으로 빠르고 효율적인 작업을 지원합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🌐</div>
                <h3>글로벌 지원</h3>
                <p>전 세계 어디서나 접근 가능한 클라우드 기반 서비스를 제공합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">💡</div>
                <h3>스마트 솔루션</h3>
                <p>AI 기반의 지능형 기능으로 더욱 똑똑한 업무 처리가 가능합니다.</p>
            </div>
        </div>
    </section>

    <!-- 기술 섹션 -->
    <section class="technology" id="technology">
        <h2 class="section-title fade-in">핵심 기술</h2>
        <div class="tech-list">
            <div class="tech-item fade-in">
                <h3>인공지능</h3>
                <p>머신러닝 기반 AI 기술</p>
            </div>
            <div class="tech-item fade-in">
                <h3>클라우드 컴퓨팅</h3>
                <p>확장 가능한 클라우드 인프라</p>
            </div>
            <div class="tech-item fade-in">
                <h3>빅데이터 분석</h3>
                <p>실시간 데이터 처리 및 분석</p>
            </div>
            <div class="tech-item fade-in">
                <h3>블록체인</h3>
                <p>안전한 분산 시스템</p>
            </div>
        </div>
    </section>

    <!-- 제품 섹션 -->
    <section class="products" id="products">
        <h2 class="section-title fade-in">신제품 소개</h2>
        <div class="product-grid">
            <div class="product-card fade-in">
                <div class="product-image">📱</div>
                <div class="product-info">
                    <h3>New Star Mobile</h3>
                    <p>모바일 환경에 최적화된 새로운 경험을 제공합니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">💻</div>
                <div class="product-info">
                    <h3>New Star Desktop</h3>
                    <p>강력한 성능으로 데스크톱 환경을 완전히 새롭게 만듭니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">☁️</div>
                <div class="product-info">
                    <h3>New Star Cloud</h3>
                    <p>언제 어디서나 접근 가능한 클라우드 솔루션입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 연락처 섹션 -->
    <section class="contact" id="contact">
        <div class="contact-content">
            <h2 class="section-title" style="color: white;">문의하기</h2>
            <p style="font-size: 1.2rem; margin-top: 1rem;">새로운 시작에 함께하세요</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div style="font-size: 2rem;">📧</div>
                    <div>contact@newstar.com</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📞</div>
                    <div>02-1234-5678</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📍</div>
                    <div>서울시 강남구</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 푸터 -->
    <footer>
        <p>&copy; 2024 New Star. All rights reserved.</p>
    </footer>

    <script>
        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // 스크롤 시 헤더 스타일 변경
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>

```


Report 폴더를 생성하고 작업 결과를 마크다운 파일로 저장 중입니다.



작업 결과를 마크다운 파일로 작성 중입니다.


```markdown
# New Star 웹사이트 개발 작업 보고서

## 프로젝트 개요
"새로운 시작(New Star)"을 알리는 신제품, 신기술 홍보용 단일 페이지 웹 애플리케이션 개발

## 작업 일시
2024년 12월 9일

## 작업 내용

### 1. 단일 페이지 웹 애플리케이션 구현
- **파일명**: `Index.html`
- **형식**: HTML5 단일 페이지 애플리케이션 (SPA)
- **기술 스택**: HTML5, CSS3, JavaScript (Vanilla JS)

### 2. 주요 기능 및 섹션

#### 2.1 헤더 및 네비게이션
- 고정 헤더 (Fixed Header)
- 부드러운 스크롤 네비게이션
- 반응형 디자인 지원

#### 2.2 히어로 섹션
- 그라데이션 배경
- 애니메이션 효과
- CTA(Call-to-Action) 버튼

#### 2.3 주요 특징 섹션
6가지 주요 특징을 카드 형태로 표시:
- 🚀 혁신적인 성능
- ✨ 직관적인 디자인
- 🔒 안전한 보안
- ⚡ 빠른 속도
- 🌐 글로벌 지원
- 💡 스마트 솔루션

#### 2.4 핵심 기술 섹션
4가지 핵심 기술 소개:
- 인공지능 (머신러닝 기반 AI 기술)
- 클라우드 컴퓨팅 (확장 가능한 클라우드 인프라)
- 빅데이터 분석 (실시간 데이터 처리 및 분석)
- 블록체인 (안전한 분산 시스템)

#### 2.5 신제품 소개 섹션
3가지 신제품 카드:
- New Star Mobile (모바일 환경 최적화)
- New Star Desktop (강력한 데스크톱 성능)
- New Star Cloud (클라우드 솔루션)

#### 2.6 연락처 섹션
- 이메일: contact@newstar.com
- 전화: 02-1234-5678
- 주소: 서울시 강남구

#### 2.7 푸터
- 저작권 정보 표시

### 3. 디자인 특징

#### 3.1 색상 스키마
- 주 색상: 그라데이션 (보라색 계열: #667eea → #764ba2)
- 배경: 흰색 및 연한 회색 (#f8f9fa)
- 텍스트: 진한 회색 (#333)

#### 3.2 애니메이션 효과
- 페이드인 애니메이션 (Fade-in)
- 호버 효과 (Hover effects)
- 스크롤 트리거 애니메이션
- 부드러운 스크롤 (Smooth scroll)

#### 3.3 반응형 디자인
- 모바일, 태블릿, 데스크톱 지원
- 미디어 쿼리를 통한 반응형 레이아웃
- 그리드 시스템 활용

### 4. JavaScript 기능

#### 4.1 스크롤 기능
- 부드러운 스크롤 네비게이션
- 스크롤 시 헤더 스타일 변경

#### 4.2 인터섹션 옵저버
- 스크롤 시 요소가 화면에 나타날 때 애니메이션 트리거
- 성능 최적화된 스크롤 애니메이션

### 5. 파일 구조

```
Nova/
├── Index.html          # 메인 웹 애플리케이션 파일
└── Report/
    └── 작업결과보고서.md  # 본 보고서
```

## 기술 사양

### HTML5
- 시맨틱 태그 사용
- 메타 태그 최적화
- 접근성 고려

### CSS3
- Flexbox 및 Grid 레이아웃
- CSS 변수 및 그라데이션
- 트랜지션 및 애니메이션
- 미디어 쿼리

### JavaScript
- Vanilla JavaScript (프레임워크 없이 순수 JS 사용)
- Intersection Observer API
- 이벤트 리스너
- DOM 조작

## 브라우저 호환성
- 모던 브라우저 지원 (Chrome, Firefox, Safari, Edge)
- ES6+ 문법 사용
- CSS Grid 및 Flexbox 지원 필요

## 사용 방법
1. `Index.html` 파일을 웹 브라우저에서 직접 열기
2. 또는 웹 서버에 업로드하여 배포

## 향후 개선 사항
- 다국어 지원 추가
- 더 많은 인터랙티브 요소 추가
- 성능 최적화
- SEO 최적화
- 접근성 개선 (ARIA 라벨 등)

## 작업 완료 상태
✅ 단일 페이지 웹 애플리케이션 구현 완료
✅ 반응형 디자인 적용 완료
✅ 애니메이션 효과 적용 완료
✅ Report 폴더 생성 완료
✅ 작업 보고서 작성 완료

---
**작성자**: AI Assistant  
**작성일**: 2024년 12월 9일

```


작업 완료.

## 완료된 작업

1. **Index.html** - "새로운 시작(New Star)" 신제품/신기술 홍보용 단일 페이지 웹앱 구현
   - 히어로 섹션 (그라데이션 배경, 애니메이션)
   - 주요 특징 섹션 (6가지 특징 카드)
   - 핵심 기술 섹션 (AI, 클라우드, 빅데이터, 블록체인)
   - 신제품 소개 섹션 (Mobile, Desktop, Cloud)
   - 연락처 섹션
   - 반응형 디자인 (모바일/태블릿/데스크톱)
   - 스크롤 애니메이션 및 부드러운 스크롤

2. **Report 폴더 생성** - 작업 결과 저장용 폴더 생성

3. **작업 결과 보고서** - `Report/작업결과보고서.md` 파일에 상세한 작업 내용 기록

`Index.html` 파일을 브라우저에서 열어 확인하세요. 모든 스타일과 기능이 단일 HTML 파일에 포함되어 있어 별도의 추가 파일 없이 바로 실행할 수 있습니다.

---

**User**

@https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D의 이미지를 기업이미지 배경으로 50% 투명도로 설정해줘

---

**Cursor**


Index.html을 확인해 배경 이미지를 추가합니다.



히어로 섹션에 Unsplash 이미지를 배경으로 추가하고 50% 투명도로 설정 중입니다.


```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Star - 새로운 시작</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* 헤더 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* 히어로 섹션 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: 
                linear-gradient(135deg, rgba(102, 126, 234, 0.5) 0%, rgba(118, 75, 162, 0.5) 100%),
                url('https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D') center/cover no-repeat;
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: move 20s linear infinite;
        }

        @keyframes move {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* 특징 섹션 */
        .features {
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        /* 기술 섹션 */
        .technology {
            background: white;
        }

        .tech-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tech-item {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        .tech-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        /* 제품 섹션 */
        .products {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* 연락처 섹션 */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        /* 푸터 */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* 스크롤 애니메이션 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- 헤더 -->
    <header>
        <nav>
            <div class="logo">New Star</div>
            <ul class="nav-links">
                <li><a href="#home">홈</a></li>
                <li><a href="#features">특징</a></li>
                <li><a href="#technology">기술</a></li>
                <li><a href="#products">제품</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>
    </header>

    <!-- 히어로 섹션 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>새로운 시작, New Star</h1>
            <p>혁신적인 기술로 미래를 만들어갑니다</p>
            <a href="#features" class="cta-button">더 알아보기</a>
        </div>
    </section>

    <!-- 특징 섹션 -->
    <section class="features" id="features">
        <h2 class="section-title fade-in">주요 특징</h2>
        <div class="features-grid">
            <div class="feature-card fade-in">
                <div class="feature-icon">🚀</div>
                <h3>혁신적인 성능</h3>
                <p>최신 기술을 활용한 뛰어난 성능으로 사용자 경험을 한 단계 끌어올립니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">✨</div>
                <h3>직관적인 디자인</h3>
                <p>사용자 중심의 깔끔하고 직관적인 인터페이스로 누구나 쉽게 사용할 수 있습니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🔒</div>
                <h3>안전한 보안</h3>
                <p>최고 수준의 보안 시스템으로 사용자의 데이터를 안전하게 보호합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">⚡</div>
                <h3>빠른 속도</h3>
                <p>최적화된 알고리즘으로 빠르고 효율적인 작업을 지원합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🌐</div>
                <h3>글로벌 지원</h3>
                <p>전 세계 어디서나 접근 가능한 클라우드 기반 서비스를 제공합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">💡</div>
                <h3>스마트 솔루션</h3>
                <p>AI 기반의 지능형 기능으로 더욱 똑똑한 업무 처리가 가능합니다.</p>
            </div>
        </div>
    </section>

    <!-- 기술 섹션 -->
    <section class="technology" id="technology">
        <h2 class="section-title fade-in">핵심 기술</h2>
        <div class="tech-list">
            <div class="tech-item fade-in">
                <h3>인공지능</h3>
                <p>머신러닝 기반 AI 기술</p>
            </div>
            <div class="tech-item fade-in">
                <h3>클라우드 컴퓨팅</h3>
                <p>확장 가능한 클라우드 인프라</p>
            </div>
            <div class="tech-item fade-in">
                <h3>빅데이터 분석</h3>
                <p>실시간 데이터 처리 및 분석</p>
            </div>
            <div class="tech-item fade-in">
                <h3>블록체인</h3>
                <p>안전한 분산 시스템</p>
            </div>
        </div>
    </section>

    <!-- 제품 섹션 -->
    <section class="products" id="products">
        <h2 class="section-title fade-in">신제품 소개</h2>
        <div class="product-grid">
            <div class="product-card fade-in">
                <div class="product-image">📱</div>
                <div class="product-info">
                    <h3>New Star Mobile</h3>
                    <p>모바일 환경에 최적화된 새로운 경험을 제공합니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">💻</div>
                <div class="product-info">
                    <h3>New Star Desktop</h3>
                    <p>강력한 성능으로 데스크톱 환경을 완전히 새롭게 만듭니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">☁️</div>
                <div class="product-info">
                    <h3>New Star Cloud</h3>
                    <p>언제 어디서나 접근 가능한 클라우드 솔루션입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 연락처 섹션 -->
    <section class="contact" id="contact">
        <div class="contact-content">
            <h2 class="section-title" style="color: white;">문의하기</h2>
            <p style="font-size: 1.2rem; margin-top: 1rem;">새로운 시작에 함께하세요</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div style="font-size: 2rem;">📧</div>
                    <div>contact@newstar.com</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📞</div>
                    <div>02-1234-5678</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📍</div>
                    <div>서울시 강남구</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 푸터 -->
    <footer>
        <p>&copy; 2024 New Star. All rights reserved.</p>
    </footer>

    <script>
        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // 스크롤 시 헤더 스타일 변경
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>


```


이미지가 50% 투명도로 보이도록 배경 레이어를 추가 중입니다.


```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Star - 새로운 시작</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* 헤더 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* 히어로 섹션 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: 
                linear-gradient(135deg, rgba(102, 126, 234, 0.5) 0%, rgba(118, 75, 162, 0.5) 100%),
                url('https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D') center/cover no-repeat;
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D') center/cover no-repeat;
            opacity: 0.5;
            z-index: 0;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: move 20s linear infinite;
            z-index: 1;
        }

        @keyframes move {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* 특징 섹션 */
        .features {
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        /* 기술 섹션 */
        .technology {
            background: white;
        }

        .tech-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tech-item {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        .tech-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        /* 제품 섹션 */
        .products {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* 연락처 섹션 */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        /* 푸터 */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* 스크롤 애니메이션 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- 헤더 -->
    <header>
        <nav>
            <div class="logo">New Star</div>
            <ul class="nav-links">
                <li><a href="#home">홈</a></li>
                <li><a href="#features">특징</a></li>
                <li><a href="#technology">기술</a></li>
                <li><a href="#products">제품</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>
    </header>

    <!-- 히어로 섹션 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>새로운 시작, New Star</h1>
            <p>혁신적인 기술로 미래를 만들어갑니다</p>
            <a href="#features" class="cta-button">더 알아보기</a>
        </div>
    </section>

    <!-- 특징 섹션 -->
    <section class="features" id="features">
        <h2 class="section-title fade-in">주요 특징</h2>
        <div class="features-grid">
            <div class="feature-card fade-in">
                <div class="feature-icon">🚀</div>
                <h3>혁신적인 성능</h3>
                <p>최신 기술을 활용한 뛰어난 성능으로 사용자 경험을 한 단계 끌어올립니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">✨</div>
                <h3>직관적인 디자인</h3>
                <p>사용자 중심의 깔끔하고 직관적인 인터페이스로 누구나 쉽게 사용할 수 있습니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🔒</div>
                <h3>안전한 보안</h3>
                <p>최고 수준의 보안 시스템으로 사용자의 데이터를 안전하게 보호합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">⚡</div>
                <h3>빠른 속도</h3>
                <p>최적화된 알고리즘으로 빠르고 효율적인 작업을 지원합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🌐</div>
                <h3>글로벌 지원</h3>
                <p>전 세계 어디서나 접근 가능한 클라우드 기반 서비스를 제공합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">💡</div>
                <h3>스마트 솔루션</h3>
                <p>AI 기반의 지능형 기능으로 더욱 똑똑한 업무 처리가 가능합니다.</p>
            </div>
        </div>
    </section>

    <!-- 기술 섹션 -->
    <section class="technology" id="technology">
        <h2 class="section-title fade-in">핵심 기술</h2>
        <div class="tech-list">
            <div class="tech-item fade-in">
                <h3>인공지능</h3>
                <p>머신러닝 기반 AI 기술</p>
            </div>
            <div class="tech-item fade-in">
                <h3>클라우드 컴퓨팅</h3>
                <p>확장 가능한 클라우드 인프라</p>
            </div>
            <div class="tech-item fade-in">
                <h3>빅데이터 분석</h3>
                <p>실시간 데이터 처리 및 분석</p>
            </div>
            <div class="tech-item fade-in">
                <h3>블록체인</h3>
                <p>안전한 분산 시스템</p>
            </div>
        </div>
    </section>

    <!-- 제품 섹션 -->
    <section class="products" id="products">
        <h2 class="section-title fade-in">신제품 소개</h2>
        <div class="product-grid">
            <div class="product-card fade-in">
                <div class="product-image">📱</div>
                <div class="product-info">
                    <h3>New Star Mobile</h3>
                    <p>모바일 환경에 최적화된 새로운 경험을 제공합니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">💻</div>
                <div class="product-info">
                    <h3>New Star Desktop</h3>
                    <p>강력한 성능으로 데스크톱 환경을 완전히 새롭게 만듭니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">☁️</div>
                <div class="product-info">
                    <h3>New Star Cloud</h3>
                    <p>언제 어디서나 접근 가능한 클라우드 솔루션입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 연락처 섹션 -->
    <section class="contact" id="contact">
        <div class="contact-content">
            <h2 class="section-title" style="color: white;">문의하기</h2>
            <p style="font-size: 1.2rem; margin-top: 1rem;">새로운 시작에 함께하세요</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div style="font-size: 2rem;">📧</div>
                    <div>contact@newstar.com</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📞</div>
                    <div>02-1234-5678</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📍</div>
                    <div>서울시 강남구</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 푸터 -->
    <footer>
        <p>&copy; 2024 New Star. All rights reserved.</p>
    </footer>

    <script>
        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // 스크롤 시 헤더 스타일 변경
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>


```

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Star - 새로운 시작</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* 헤더 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* 히어로 섹션 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D') center/cover no-repeat;
            opacity: 0.5;
            z-index: 0;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: move 20s linear infinite;
            z-index: 1;
        }

        @keyframes move {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* 특징 섹션 */
        .features {
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        /* 기술 섹션 */
        .technology {
            background: white;
        }

        .tech-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tech-item {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        .tech-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        /* 제품 섹션 */
        .products {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* 연락처 섹션 */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        /* 푸터 */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* 스크롤 애니메이션 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- 헤더 -->
    <header>
        <nav>
            <div class="logo">New Star</div>
            <ul class="nav-links">
                <li><a href="#home">홈</a></li>
                <li><a href="#features">특징</a></li>
                <li><a href="#technology">기술</a></li>
                <li><a href="#products">제품</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>
    </header>

    <!-- 히어로 섹션 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>새로운 시작, New Star</h1>
            <p>혁신적인 기술로 미래를 만들어갑니다</p>
            <a href="#features" class="cta-button">더 알아보기</a>
        </div>
    </section>

    <!-- 특징 섹션 -->
    <section class="features" id="features">
        <h2 class="section-title fade-in">주요 특징</h2>
        <div class="features-grid">
            <div class="feature-card fade-in">
                <div class="feature-icon">🚀</div>
                <h3>혁신적인 성능</h3>
                <p>최신 기술을 활용한 뛰어난 성능으로 사용자 경험을 한 단계 끌어올립니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">✨</div>
                <h3>직관적인 디자인</h3>
                <p>사용자 중심의 깔끔하고 직관적인 인터페이스로 누구나 쉽게 사용할 수 있습니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🔒</div>
                <h3>안전한 보안</h3>
                <p>최고 수준의 보안 시스템으로 사용자의 데이터를 안전하게 보호합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">⚡</div>
                <h3>빠른 속도</h3>
                <p>최적화된 알고리즘으로 빠르고 효율적인 작업을 지원합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🌐</div>
                <h3>글로벌 지원</h3>
                <p>전 세계 어디서나 접근 가능한 클라우드 기반 서비스를 제공합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">💡</div>
                <h3>스마트 솔루션</h3>
                <p>AI 기반의 지능형 기능으로 더욱 똑똑한 업무 처리가 가능합니다.</p>
            </div>
        </div>
    </section>

    <!-- 기술 섹션 -->
    <section class="technology" id="technology">
        <h2 class="section-title fade-in">핵심 기술</h2>
        <div class="tech-list">
            <div class="tech-item fade-in">
                <h3>인공지능</h3>
                <p>머신러닝 기반 AI 기술</p>
            </div>
            <div class="tech-item fade-in">
                <h3>클라우드 컴퓨팅</h3>
                <p>확장 가능한 클라우드 인프라</p>
            </div>
            <div class="tech-item fade-in">
                <h3>빅데이터 분석</h3>
                <p>실시간 데이터 처리 및 분석</p>
            </div>
            <div class="tech-item fade-in">
                <h3>블록체인</h3>
                <p>안전한 분산 시스템</p>
            </div>
        </div>
    </section>

    <!-- 제품 섹션 -->
    <section class="products" id="products">
        <h2 class="section-title fade-in">신제품 소개</h2>
        <div class="product-grid">
            <div class="product-card fade-in">
                <div class="product-image">📱</div>
                <div class="product-info">
                    <h3>New Star Mobile</h3>
                    <p>모바일 환경에 최적화된 새로운 경험을 제공합니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">💻</div>
                <div class="product-info">
                    <h3>New Star Desktop</h3>
                    <p>강력한 성능으로 데스크톱 환경을 완전히 새롭게 만듭니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">☁️</div>
                <div class="product-info">
                    <h3>New Star Cloud</h3>
                    <p>언제 어디서나 접근 가능한 클라우드 솔루션입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 연락처 섹션 -->
    <section class="contact" id="contact">
        <div class="contact-content">
            <h2 class="section-title" style="color: white;">문의하기</h2>
            <p style="font-size: 1.2rem; margin-top: 1rem;">새로운 시작에 함께하세요</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div style="font-size: 2rem;">📧</div>
                    <div>contact@newstar.com</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📞</div>
                    <div>02-1234-5678</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📍</div>
                    <div>서울시 강남구</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 푸터 -->
    <footer>
        <p>&copy; 2024 New Star. All rights reserved.</p>
    </footer>

    <script>
        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // 스크롤 시 헤더 스타일 변경
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>


```

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New Star - 새로운 시작</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* 헤더 */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* 히어로 섹션 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1700713400904-f5c3d71a748b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fCVFQSVCOCVCMCVFQyU5NyU4NSUyMCVFQyU5RCVCNCVFQiVBRiVCOCVFQyVBNyU4MHxlbnwwfHwwfHx8MA%3D%3D') center/cover no-repeat;
            opacity: 0.5;
            z-index: 0;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: move 20s linear infinite;
            z-index: 1;
        }

        @keyframes move {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* 특징 섹션 */
        .features {
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        /* 기술 섹션 */
        .technology {
            background: white;
        }

        .tech-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tech-item {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        .tech-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        /* 제품 섹션 */
        .products {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* 연락처 섹션 */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        /* 푸터 */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* 스크롤 애니메이션 */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- 헤더 -->
    <header>
        <nav>
            <div class="logo">New Star</div>
            <ul class="nav-links">
                <li><a href="#home">홈</a></li>
                <li><a href="#features">특징</a></li>
                <li><a href="#technology">기술</a></li>
                <li><a href="#products">제품</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>
    </header>

    <!-- 히어로 섹션 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>새로운 시작, New Star</h1>
            <p>혁신적인 기술로 미래를 만들어갑니다</p>
            <a href="#features" class="cta-button">더 알아보기</a>
        </div>
    </section>

    <!-- 특징 섹션 -->
    <section class="features" id="features">
        <h2 class="section-title fade-in">주요 특징</h2>
        <div class="features-grid">
            <div class="feature-card fade-in">
                <div class="feature-icon">🚀</div>
                <h3>혁신적인 성능</h3>
                <p>최신 기술을 활용한 뛰어난 성능으로 사용자 경험을 한 단계 끌어올립니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">✨</div>
                <h3>직관적인 디자인</h3>
                <p>사용자 중심의 깔끔하고 직관적인 인터페이스로 누구나 쉽게 사용할 수 있습니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🔒</div>
                <h3>안전한 보안</h3>
                <p>최고 수준의 보안 시스템으로 사용자의 데이터를 안전하게 보호합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">⚡</div>
                <h3>빠른 속도</h3>
                <p>최적화된 알고리즘으로 빠르고 효율적인 작업을 지원합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">🌐</div>
                <h3>글로벌 지원</h3>
                <p>전 세계 어디서나 접근 가능한 클라우드 기반 서비스를 제공합니다.</p>
            </div>
            <div class="feature-card fade-in">
                <div class="feature-icon">💡</div>
                <h3>스마트 솔루션</h3>
                <p>AI 기반의 지능형 기능으로 더욱 똑똑한 업무 처리가 가능합니다.</p>
            </div>
        </div>
    </section>

    <!-- 기술 섹션 -->
    <section class="technology" id="technology">
        <h2 class="section-title fade-in">핵심 기술</h2>
        <div class="tech-list">
            <div class="tech-item fade-in">
                <h3>인공지능</h3>
                <p>머신러닝 기반 AI 기술</p>
            </div>
            <div class="tech-item fade-in">
                <h3>클라우드 컴퓨팅</h3>
                <p>확장 가능한 클라우드 인프라</p>
            </div>
            <div class="tech-item fade-in">
                <h3>빅데이터 분석</h3>
                <p>실시간 데이터 처리 및 분석</p>
            </div>
            <div class="tech-item fade-in">
                <h3>블록체인</h3>
                <p>안전한 분산 시스템</p>
            </div>
        </div>
    </section>

    <!-- 제품 섹션 -->
    <section class="products" id="products">
        <h2 class="section-title fade-in">신제품 소개</h2>
        <div class="product-grid">
            <div class="product-card fade-in">
                <div class="product-image">📱</div>
                <div class="product-info">
                    <h3>New Star Mobile</h3>
                    <p>모바일 환경에 최적화된 새로운 경험을 제공합니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">💻</div>
                <div class="product-info">
                    <h3>New Star Desktop</h3>
                    <p>강력한 성능으로 데스크톱 환경을 완전히 새롭게 만듭니다.</p>
                </div>
            </div>
            <div class="product-card fade-in">
                <div class="product-image">☁️</div>
                <div class="product-info">
                    <h3>New Star Cloud</h3>
                    <p>언제 어디서나 접근 가능한 클라우드 솔루션입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 연락처 섹션 -->
    <section class="contact" id="contact">
        <div class="contact-content">
            <h2 class="section-title" style="color: white;">문의하기</h2>
            <p style="font-size: 1.2rem; margin-top: 1rem;">새로운 시작에 함께하세요</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div style="font-size: 2rem;">📧</div>
                    <div>contact@newstar.com</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📞</div>
                    <div>02-1234-5678</div>
                </div>
                <div class="contact-item">
                    <div style="font-size: 2rem;">📍</div>
                    <div>서울시 강남구</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 푸터 -->
    <footer>
        <p>&copy; 2024 New Star. All rights reserved.</p>
    </footer>

    <script>
        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // 스크롤 시 헤더 스타일 변경
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>


```


작업 완료. Unsplash 이미지를 히어로 섹션 배경으로 추가하고 50% 투명도로 설정했습니다.

## 변경 사항

1. **배경 이미지 추가**: 히어로 섹션에 Unsplash 이미지를 배경으로 추가했습니다.
2. **50% 투명도 적용**: `::before` 가상 요소에 이미지를 배치하고 `opacity: 0.5`로 설정했습니다.
3. **레이어 구조**:
   - 최하단: Unsplash 이미지 (50% 투명도)
   - 중간: 그라데이션 배경 (보라색 계열)
   - 상단: 애니메이션 패턴
   - 최상단: 콘텐츠 텍스트

이미지가 50% 투명도로 표시되며, 기존 그라데이션과 함께 보입니다. 브라우저에서 확인해 주세요.

---

**User**

작업한 내용을 @NOVA에 readme.md 파일에 저장해줘

---

**Cursor**


작업 내용을 정리해 `readme.md` 파일로 저장 중입니다.


```markdown
# New Star - 새로운 시작 웹사이트

## 프로젝트 개요
"새로운 시작(New Star)"을 알리는 신제품, 신기술 홍보용 단일 페이지 웹 애플리케이션입니다.

## 주요 기능

### 1. 단일 페이지 웹 애플리케이션 (SPA)
- HTML5, CSS3, Vanilla JavaScript로 구현
- 모든 기능이 하나의 HTML 파일에 포함
- 별도의 의존성 없이 바로 실행 가능

### 2. 섹션 구성

#### 히어로 섹션
- **배경 이미지**: Unsplash 이미지를 50% 투명도로 적용
- 그라데이션 오버레이 (보라색 계열: #667eea → #764ba2)
- 애니메이션 패턴 효과
- 페이드인 애니메이션

#### 주요 특징 섹션
6가지 주요 특징을 카드 형태로 표시:
- 🚀 혁신적인 성능
- ✨ 직관적인 디자인
- 🔒 안전한 보안
- ⚡ 빠른 속도
- 🌐 글로벌 지원
- 💡 스마트 솔루션

#### 핵심 기술 섹션
4가지 핵심 기술 소개:
- 인공지능 (머신러닝 기반 AI 기술)
- 클라우드 컴퓨팅 (확장 가능한 클라우드 인프라)
- 빅데이터 분석 (실시간 데이터 처리 및 분석)
- 블록체인 (안전한 분산 시스템)

#### 신제품 소개 섹션
3가지 신제품 카드:
- New Star Mobile (모바일 환경 최적화)
- New Star Desktop (강력한 데스크톱 성능)
- New Star Cloud (클라우드 솔루션)

#### 연락처 섹션
- 이메일: contact@newstar.com
- 전화: 02-1234-5678
- 주소: 서울시 강남구

## 기술 스택

- **HTML5**: 시맨틱 태그 사용
- **CSS3**: 
  - Flexbox 및 Grid 레이아웃
  - CSS 변수 및 그라데이션
  - 트랜지션 및 애니메이션
  - 미디어 쿼리 (반응형 디자인)
- **JavaScript**: 
  - Vanilla JavaScript (프레임워크 없이 순수 JS)
  - Intersection Observer API
  - 이벤트 리스너
  - DOM 조작

## 디자인 특징

### 색상 스키마
- 주 색상: 그라데이션 (보라색 계열: #667eea → #764ba2)
- 배경: 흰색 및 연한 회색 (#f8f9fa)
- 텍스트: 진한 회색 (#333)

### 애니메이션 효과
- 페이드인 애니메이션 (Fade-in)
- 호버 효과 (Hover effects)
- 스크롤 트리거 애니메이션
- 부드러운 스크롤 (Smooth scroll)

### 배경 이미지
- Unsplash 이미지 사용
- 50% 투명도 적용 (opacity: 0.5)
- 그라데이션 오버레이와 함께 사용

## 반응형 디자인
- 모바일, 태블릿, 데스크톱 지원
- 미디어 쿼리를 통한 반응형 레이아웃
- 그리드 시스템 활용

## 사용 방법

1. `Index.html` 파일을 웹 브라우저에서 직접 열기
2. 또는 웹 서버에 업로드하여 배포

## 브라우저 호환성
- 모던 브라우저 지원 (Chrome, Firefox, Safari, Edge)
- ES6+ 문법 사용
- CSS Grid 및 Flexbox 지원 필요

## 파일 구조

```
Nova/
├── Index.html          # 메인 웹 애플리케이션 파일
├── readme.md          # 본 문서
└── Report/
    └── 작업결과보고서.md  # 상세 작업 보고서
```

## 주요 구현 사항

### 배경 이미지 구현
히어로 섹션에 Unsplash 이미지를 배경으로 추가하고 50% 투명도로 설정:
- `::before` 가상 요소에 이미지 배치
- `opacity: 0.5` 적용
- 그라데이션 오버레이와 함께 사용

### 레이어 구조
1. 최하단: Unsplash 이미지 (50% 투명도)
2. 중간: 그라데이션 배경 (보라색 계열)
3. 상단: 애니메이션 패턴
4. 최상단: 콘텐츠 텍스트

### JavaScript 기능
- 부드러운 스크롤 네비게이션
- 스크롤 시 헤더 스타일 변경
- Intersection Observer를 사용한 스크롤 애니메이션

## 향후 개선 사항
- 다국어 지원 추가
- 더 많은 인터랙티브 요소 추가
- 성능 최적화
- SEO 최적화
- 접근성 개선 (ARIA 라벨 등)

## 라이선스
© 2024 New Star. All rights reserved.

---
**작성일**: 2024년 12월 9일

```


작업 내용을 `readme.md` 파일로 저장했습니다.

## 저장된 내용

`readme.md` 파일에 다음 내용을 포함했습니다:

- 프로젝트 개요
- 주요 기능 및 섹션 설명
- 기술 스택 (HTML5, CSS3, JavaScript)
- 디자인 특징 (색상, 애니메이션, 배경 이미지)
- 반응형 디자인 정보
- 사용 방법
- 브라우저 호환성
- 파일 구조
- 주요 구현 사항 (배경 이미지 50% 투명도 포함)
- 향후 개선 사항

프로젝트 루트 디렉토리(`Nova`)에 `readme.md` 파일이 생성되었습니다.

