# Starbucks 디자인 토큰 (Design Tokens)

> 출처: [starbucks.com](https://www.starbucks.com/) 및 공식 브랜드/디자인 시스템 자료를 기반으로 추출.
> Figma의 토큰(Variables/Styles) 구조에 맞춰 Color / Typography / Spacing / Radius / Shadow / Breakpoint 그룹으로 정리했습니다.
> 라이선스 안내: 색상·폰트 값은 사실 정보이며, 수치는 공개 자료를 참고해 재정리했습니다(라이선스 준수를 위해 내용 재구성). Starbucks 브랜드 자산은 상업적 사용 시 공식 가이드라인 확인이 필요합니다.

---

## 1. Color (색상)

### 1.1 Primary — Brand Green (4단계 그린 시스템)
스타벅스의 핵심은 단일 "브랜드 그린"이 아니라, 역할별로 분화된 네 단계의 그린입니다.

| Token | HEX | RGB | 용도 (Role) |
|---|---|---|---|
| `color.primary.starbucks` | `#006241` | `0, 98, 65` | 헤딩/핵심 브랜드 그린 |
| `color.primary.accent` | `#00754A` | `0, 117, 74` | 주요 CTA 버튼, 강조 요소 |
| `color.primary.house` | `#1E3932` | `30, 57, 50` | 깊은 feature 밴드, 다크 섹션 배경 |
| `color.primary.uplift` | `#2B5148` | `43, 81, 72` | 장식/보조 그린, 데코레이션 |

> 참고: 로고/인쇄용 클래식 그린은 `#00704A` (Pantone 3425 C 계열)로도 널리 통용됩니다.

### 1.2 Surface — Canvas (배경면)
배경은 순백색이 아니라, 카페 재질(냅킨/벽/원목)을 연상시키는 따뜻한 크림 톤입니다.

| Token | HEX | RGB | 용도 |
|---|---|---|---|
| `color.surface.cream` | `#F2F0EB` | `242, 240, 235` | 기본 배경 (warm cream) |
| `color.surface.ceramic` | `#EDEBE9` | `237, 235, 233` | 약간 어두운 보조 배경 (ceramic) |
| `color.surface.white` | `#FFFFFF` | `255, 255, 255` | 카드/모달 등 순백 표면 |

### 1.3 Neutral — Text & Structure (중성)
| Token | HEX | RGB | 용도 |
|---|---|---|---|
| `color.neutral.black` | `#000000` | `0, 0, 0` | 최대 대비 텍스트 |
| `color.neutral.ink` | `#27251F` | `39, 37, 31` | 기본 본문 텍스트 (warm black) |
| `color.neutral.white` | `#FFFFFF` | `255, 255, 255` | 반전 텍스트 |

### 1.4 Accent — Ceremony (강조)
| Token | HEX | RGB | 용도 |
|---|---|---|---|
| `color.accent.gold` | `#CBA258` | `203, 162, 88` | Rewards 등급 등 '의식적(ceremony)' 강조 전용 (범용 금지) |

### 1.5 Semantic (상태) — 권장 기본값
공식 범용 상태 색이 별도로 공개되지 않아, 브랜드 톤에 맞춘 권장값으로 제안합니다.

| Token | HEX | 용도 |
|---|---|---|
| `color.semantic.success` | `#00754A` | 성공 (브랜드 그린 재사용) |
| `color.semantic.error` | `#D62B1F` | 오류 |
| `color.semantic.warning` | `#CBA258` | 경고 (gold) |
| `color.semantic.info` | `#1E3932` | 정보 |
| `color.semantic.link` | `#00754A` | 인라인 링크 |

---

## 2. Typography (타이포그래피)

- **Font Family**: `SoDo Sans` (스타벅스 전용 서체). 대체 폰트 스택:
  `"SoDo Sans", "Lander", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- **Letter-spacing (tracking)**: 전반적으로 타이트하게 `-0.16px` 적용

| Token | Size | Weight | Line-height | 용도 |
|---|---|---|---|---|
| `type.display` | 48px | 700 | 1.1 | 대형 히어로 헤드라인 |
| `type.h1` | 36px | 700 | 1.15 | 페이지 제목 |
| `type.h2` | 28px | 700 | 1.2 | 섹션 제목 |
| `type.h3` | 22px | 600 | 1.25 | 서브 섹션 |
| `type.body.lg` | 18px | 400 | 1.5 | 큰 본문 |
| `type.body` | 16px | 400 | 1.5 | 기본 본문 |
| `type.body.sm` | 14px | 400 | 1.45 | 작은 본문 |
| `type.caption` | 12px | 400 | 1.4 | 캡션/주석 |
| `type.button` | 16px | 600 | 1 | 버튼 라벨 |

> 모든 토큰 공통: `letter-spacing: -0.16px`

---

## 3. Spacing (간격)

rem 기반 스케일, 기준 `1.6rem = 16px`. 4의 배수 리듬.

| Token | rem | px |
|---|---|---|
| `space.xs` | 0.4rem | 4px |
| `space.sm` | 0.8rem | 8px |
| `space.md` | 1.2rem | 12px |
| `space.base` | 1.6rem | 16px |
| `space.lg` | 2.4rem | 24px |
| `space.xl` | 3.2rem | 32px |
| `space.2xl` | 4.8rem | 48px |
| `space.3xl` | 6.4rem | 64px |

---

## 4. Border Radius (모서리 반경)

| Token | 값 | 용도 |
|---|---|---|
| `radius.pill` | 50px | 버튼(풀 필 형태) — 시그니처 스타일 |
| `radius.card` | 12px | 카드/패널 |
| `radius.circle` | 9999px | 원형 요소 (Frap 플로팅 CTA 등) |

---

## 5. Shadow / Elevation (그림자)

| Token | 값(권장) | 용도 |
|---|---|---|
| `shadow.sm` | `0 1px 2px rgba(0,0,0,0.08)` | 미세 구분 |
| `shadow.card` | `0 2px 8px rgba(0,0,0,0.10)` | 카드 |
| `shadow.float` | `0 8px 24px rgba(0,0,0,0.18)` | 플로팅 CTA(Frap 원형 버튼 등) 레이어드 그림자 |

---

## 6. Component Tokens (대표 컴포넌트)

| 컴포넌트 | 속성 | 값 |
|---|---|---|
| Primary Button | 배경 / 반경 / 액티브 | `#00754A` / `radius.pill(50px)` / `transform: scale(0.95)` |
| Floating Frap CTA | 크기 / 색 / 형태 | `56px` / `#00754A` / `radius.circle` + `shadow.float` |
| Feature Band | 배경 | `#1E3932` (House Green) |
| Rewards Pill | 테두리 | `#CBA258` (gold outline) |

> 시그니처 마이크로 인터랙션: 버튼 누름 시 `transform: scale(0.95)`.

---

## 7. Breakpoints (반응형 분기점) — 권장값

| Token | 값 | 대상 |
|---|---|---|
| `bp.sm` | 480px | 모바일 |
| `bp.md` | 768px | 태블릿 |
| `bp.lg` | 1024px | 소형 데스크톱 |
| `bp.xl` | 1280px | 데스크톱 |

---

## 참고 출처
- [Starbucks 공식 사이트](https://www.starbucks.com/)
- [Starbucks Design System 정리 (shadcn.io)](https://www.shadcn.io/design/starbucks)
- [Starbucks Creative Expression — Color](https://creative.starbucks.com/color/)
- 브랜드 컬러 HEX 참고: usbrandcolors.com, brandpalettes.com, color-name.com

*일부 수치(semantic, breakpoint, shadow)는 공식 공개값이 아닌 브랜드 톤 기반 권장값이며, 그 외 색상/타이포/radius 값은 공개 자료를 재정리한 것입니다. 내용은 라이선스 준수를 위해 재구성되었습니다.*
