# Aticaa Tech View — M5 vs M5 Pro vs M5 Max 완전 비교

Apple이 3월 3일 M5 Pro/Max를 발표했다.
M5 base는 2025년 10월 출시로 실측 데이터까지 확보된 상태.
이번 세대의 키워드는 단 하나 — **AI 성능**.

> **데이터 기준일**: 2026-03-04
> **출처**: Apple 공식, Geekbench 6

---

## Product Verdict

- 🟢 **Strong Buy**: M5 — SC 4,263 (역대 1위), $1,599 (₩2,390,000). 가성비 최강
- 🟡 **Buy**: M5 Pro — 18코어 CPU + 20코어 GPU, 64GB, 307 GB/s. 전문가 최적
- 🟠 **Wait**: M5 Max — 40코어 GPU, 128GB, 614 GB/s. 압도적이나 실측 미검증

---

## 핵심 스펙 비교

### CPU

- **M5**: 10코어 (4 Performance + 6 Efficiency)
- **M5 Pro**: 최대 18코어 (6 Super + 12 Performance) — Super Core 최초 도입
- **M5 Max**: 18코어 (6 Super + 12 Performance)

> M5 Pro/Max에는 **Efficiency 코어가 없다**. 모든 코어가 성능 중심.
> "Super Core"는 이번에 새로 생긴 계층 — Apple 최초 **3단계 CPU**.

### GPU

```
GPU 코어 수:
█████ M5 10
██████████ M5 Pro 20
████████████████████ M5 Max 40 ★
```

모든 GPU 코어에 **Neural Accelerator** 내장.
GPU 코어 수 = AI 가속기 수.

### 메모리

```
대역폭 (GB/s):
█████ M5 153
██████████ M5 Pro 307
████████████████████ M5 Max 614 ★
```

- **M5**: 최대 32GB
- **M5 Pro**: 최대 64GB (+33% vs M4 Pro)
- **M5 Max**: 최대 128GB

> 대역폭이 1:2:4 비율로 정확히 스케일링.
> AI 추론 토큰 속도는 대역폭에 거의 비례한다.

### 아키텍처

- **M5**: 싱글 다이 (3nm N3P)
- **M5 Pro/Max**: **듀얼 다이 Fusion Architecture** — Apple 최초 멀티 다이 소비자 칩

```
┌────────────────────────
│ Fusion Architecture
│
│ Die A ←→ Die B
│ Super+GPU  Perf+Mem
│
│ Unified Memory
│ (최대 128GB)
└────────────────────────
```

두 개의 3nm 다이를 하나로 결합.
AMD chiplet과 유사하지만 Unified Memory가 차별점.

---

## 벤치마크 성능

### Geekbench 6 싱글코어

```
싱글코어:
███████████████ M4 Pro 3800
█████████████████ M5 4263 ✓
██████████████████ M5 Pro ~4400
██████████████████ M5 Max ~4500 ★
```

> 셋 다 **~6% 차이**. 일상 체감 속도는 거의 동일.

### Geekbench 6 멀티코어

```
멀티코어:
████████████ M5 17.9K ✓
███████████████ M5 Pro ~23.8K
████████████████████ M5 Max ~31K ★
```

> M5 Max는 M5 대비 **+73%**. 코어 수(10 vs 18) 차이가 반영.

### GPU Metal (추정)

```
GPU Metal:
██████ M5 ~80K
███████████ M5 Pro ~160K
██████████████████ M5 Max ~258K ★
```

> M5 Max: M4 Max (191K) 대비 **+34%**.
> Geekbench 6 GPU 최초 **250K 돌파** 가능.

### M4 대비 향상률

- **싱글코어**: M5 +12% / M5 Pro +16% / M5 Max +18%
- **멀티코어**: M5 +15% / M5 Pro **+30%** / M5 Max **+35%**
- **GPU AI 연산**: 전 라인업 **4x** (각 전작 대비)
- **메모리 대역폭**: Pro/Max **+28%** (240→307 / 480→614)

---

## AI 성능 — 이번 세대의 핵심

### GPU Neural Accelerator가 게임 체인저

기존 M4는 Neural Engine만 AI 전담.
M5는 **GPU 코어마다** Neural Accelerator가 내장되어 GPU에서도 AI 연산 가능.

```
┌────────────────────────
│ M4: GPU → 렌더링만
│     NE  → AI만
│
│ M5: GPU+NA → AI+렌더링
│     NE    → AI (병행)
└────────────────────────
```

결과: GPU 기반 AI 작업(이미지 생성, LLM 추론)이 **4배 빨라짐**.

### AI 하드웨어 절대 비교

```
Neural Accelerator 수:
█████ M5 10
██████████ M5 Pro 20
████████████████████ M5 Max 40 ★
```

> Apple의 "4x AI"는 **각 칩이 자기 전작 대비** 4배.
> 절대 비교에서 M5 Max는 M5의 **4배 AI 하드웨어**.

### 로컬 LLM 실행 능력

- **7B 파라미터 모델** (Llama 3 Small)
  - M5: ✅ 가능 / M5 Pro: ✅ 쾌적 / M5 Max: ✅ 매우 쾌적

- **70B 파라미터 모델** (Llama 3 Large)
  - M5: ❌ 32GB 메모리 부족
  - M5 Pro: ⚠️ 64GB로 Q4 양자화 가능
  - M5 Max: ★ **128GB + 614 GB/s로 최적**

> 70B+ 모델 로컬 실행이 목표라면 M5 Max가 유일한 선택.
> M5 Pro 64GB도 양자화(Q4) 모델은 가능하나 속도 차이 큼.

### Apple ML Research 데이터

- LLM 프롬프트 처리: **4x 빠름** (vs M4)
- FLUX-dev 이미지 생성 (12B 파라미터): **3.8x 빠름**
- 토큰 생성 속도: 대역폭에 거의 **선형 비례**

---

## 가격 비교

### MacBook Pro 시작 가격

**14인치**
- **M5**: $1,599 (₩2,390,000)
- **M5 Pro**: $2,199 (₩3,290,000 추정)
- **M5 Max**: $3,599 (₩5,390,000 추정)

**16인치**
- **M5 Pro**: $2,699 (₩3,990,000 추정)
- **M5 Max**: $3,899 (₩5,790,000 추정)
- **M5 Max 풀옵션**: $7,349 (₩10,990,000 추정)

> 환율: $1 ≈ ₩1,450 (2026년 3월). 한국 프리미엄 ~3%.

### 가성비 (MC 점수 / $1,000)

```
가성비:
████████████████████ M5 11.17 ★
███████████████████ M5 Pro 10.82
██████████████ M5 Max 7.95
```

> 달러당 멀티코어 성능은 M5 base가 최고.
> M5 Max는 **메모리 대역폭에 대한 프리미엄**을 지불하는 구조.

### M4 대비 가격 변동

- **Base 14"**: $1,599 → $1,599 (동일)
- **Pro 14"**: $1,999 → $2,199 (**+$200, +10%**)
- **Max 16"**: $3,499 → $3,899 (**+$400, +11%**)

> Pro/Max 가격 인상. Fusion Architecture 제조 원가 + AI 프리미엄 반영.

---

## 인사이트

**1. "4x AI"는 상대치 — M5 Max의 절대 AI 하드웨어는 M5의 4배**

Apple은 전 라인업 "4x AI"라고 하지만, 각 칩이 자기 전작 대비 4배라는 뜻. M5 Max(40 Neural Accel.)는 M5(10개)의 4배 하드웨어. 70B+ LLM 로컬 실행에서 이 차이는 결정적.

**2. 메모리 대역폭이 진짜 차별화 — SC는 6%, 대역폭은 4배**

싱글코어 4,263–4,500 (6% 차이) vs 대역폭 153–614 GB/s (4배 차이). LLM 토큰 속도는 대역폭에 비례. **구매 결정의 핵심은 CPU가 아닌 대역폭**.

**3. Fusion Architecture = Apple의 chiplet — 혁신이지만 1세대 리스크**

Apple 최초의 듀얼 다이 소비자 칩. AMD가 서버에서 증명했지만 초기엔 다이 간 지연·발열 이슈가 있었다. Unified Memory가 해결책인지는 실측이 나와봐야 안다.

**4. Super Core = 3단계 CPU 계층의 시작**

M5 base: P+E (2단계). M5 Pro/Max: **S+P** (E 없음). Super Core가 싱글코어 우위(~4,400–4,500 vs 4,263)의 근거. 모든 코어가 성능 중심인 건 Pro/Max 사용자에겐 좋은 소식.

**5. 한국 프리미엄 ~3.1% — 역대 최소 수준**

M5 14" ₩2,390,000 / 환율 적용가 ₩2,318,550 = +3.1%. 과거 5–8%에서 크게 줄었다. 원화 약세가 역설적으로 실질 가격 격차를 줄이는 효과.

---

## Reality Check

> M5 Pro/Max는 발표 다음 날 기준. 실측 미검증.

### M5 (Base) — 실측 확인 ✅

- **Geekbench SC**: 4,263 (역대 1위) ✅
- **Geekbench MC**: 17,862 (+15% vs M4) ✅
- **GPU AI 4x**: 실측 3.5–4x 확인 ✅

### M5 Pro / M5 Max — 검증 대기 ⏳

- MC "30% 향상": ⏳ 출시 후 1–2주
- GPU "34% 향상": ⏳ 출시 후 1–2주
- "4x AI 연산": ⏳ 출시 후 1개월
- Fusion 안정성: ⏳ 출시 후 3개월
- 발열/쓰로틀링: ⏳ 출시 후 1–2주

> ⚠️ M5 Pro/Max 추정치는 Apple 마케팅 + M5 실측 기반.
> 독립 벤치마크와 다를 수 있음.

### 업데이트 예정

- 📅 3월 말: 실제 Geekbench 반영
- 📅 4월: 발열/배터리 리뷰 종합
- 📅 6월: Product Verdict 재평가

---

## 레퍼런스

- [Apple Newsroom — M5 발표](https://www.apple.com/newsroom/2025/10/apple-unleashes-m5-the-next-big-leap-in-ai-performance-for-apple-silicon/)
- [Apple Newsroom — M5 Pro/Max 발표](https://www.apple.com/newsroom/2026/03/apple-debuts-m5-pro-and-m5-max-to-supercharge-the-most-demanding-pro-workflows/)
- [Geekbench 6 — M5 실측](https://browser.geekbench.com/v6/cpu/14591329)
- [Apple ML Research — M5 GPU LLM 탐색](https://machinelearning.apple.com/research/exploring-llms-mlx-m5)

> 환율: $1 ≈ ₩1,450 / ¥150 (2026년 3월)
> 이 글은 구매 조언이 아닙니다. 공식 리뷰 확인 후 결정하세요.

#AppleSilicon #M5 #M5Pro #M5Max #FusionArchitecture #MacBookPro #AI성능 #AticaaTechView
