# 바닐라 JS 프로젝트 성능 개선

- url: https://front-5th-chapter4-2-basic-vert.vercel.app/

## 성능 개선 보고서

### 1. 개선 이유

- 퍼포먼스 점수(72%)가 낮고, LCP(14.48s)가 매우 느린 편으로, 페이지 로딩 속도가 느려 사용자 이탈률이 높을 것으로 예상
- 접근성 점수가 82%로 다양한 환경의 사용자들이 웹사이트 이용에 불편을 겪을 수 있음
- Best Practices 점수가 75%로 웹 표준 및 보안, 코드 품질 등에서 미흡한 부분이 있음
- SEO 점수(82%)가 낮아 검색 엔진에서 신규 방문자 유입이 어려워보임

### 2. 개선 방법

- **이미지 리소스**: .webp 변경, 압축 및 사이즈 조정
- **이미지 로딩**: lazy loading 적용
- **콘솔 오류 해결**: cookieconsent 콘솔 오류 해결
- **불필요한 함수 제거**: product.js 파일 내 실제 기능 없는 코드 제거
- **SEO 개선**: meta 설명 태그 추가

### 3. 개선 후 향상된 지표

- Lighthouse 점수
  | 카테고리 | 개선 전 | 개선 후 | 개선율 |
  |----------|------|------|-------|
  | Performance | 72% | 97% | &uparrow; 25% |
  | Accessibility | 82% | 95% | &uparrow; 13% |
  | SEO | 82% | 100% | &uparrow; 18% |

- Core Web Vitals (2024)
  | 메트릭 | 설명 | 개선 전 | 개선 후 | 개선율 |
  | ------ | -------------------- | ------ | ------- | ---- |
  | LCP | Largest Contentful Paint | 14.48s | 2.48s | &downarrow; 12s |

- PageSpeed 분석 이미지
  - 개선 전
    ![before](/PageSpeed_before.png)
  - 개선 후
    ![after](/PageSpeed_after.png)

### 4. 결과

이미지 리소스 최적화 및 SEO 개선 작업을 통해 Lighthouse 주요 점수와 LCP 지표가 향상되어 사용자 경험과 검색 엔진 최적화 수준을 높임
