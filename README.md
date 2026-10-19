# 이진아 (Jina Lee)

 의료 데이터·멀티모달 모델의 **데이터 파이프라인과 평가**를 주로 다룹니다.



## Stack

`Python` `PyTorch` `Hugging Face Transformers / datasets` `vLLM` `scikit-learn` `XGBoost / LightGBM` `Pandas` `OpenCV` `Streamlit` `CUDA / cuDNN (수업)` `Linux GPU 서버` `Git`

## Featured projects

| 프로젝트 | 한 줄 | 스택 | 링크 |
|---|---|---|---|
| **MMMU Eval Pipeline (Qwen3-VL-4B)** | 공식 recipe로 MMMU-val 900문항 재현 61.11% (공식 67.4), 격차를 length-stop 40건·open 16.98%·이미지 유형별로 분해, CoT ablation으로 open 문항 +22.6%p (McNemar p=0.0075) | vLLM, HF datasets, Python | [Binary-Ah/mmmu-eval-qwen3vl](https://github.com/Binary-Ah/mmmu-eval-qwen3vl) · 팀 레포 [Chaeeun4/MMDL](https://github.com/Chaeeun4/MMDL) |
| **MIMIC-IV Note Leakage Study** | 퇴원요약지 329,940건에서 미래 정보를 단계적으로 제거하며 AUROC 0.9995 → 0.9552, Top 피처가 expired/deceased → hypotension/intubated로 바뀌는 것을 확인 — KSC2025 장려상 (제1저자) | Bio_ClinicalBERT, XGBoost, LR | 공개 준비 중 |
| **MIMIC-IV HF Readmission** | 심부전 입원 57,800건으로 30일 재입원 예측(재입원율 16.1%), 40 GB chartevents 청크 처리로 첫 24시간 바이탈 집계, 재실기간 회귀의 누수 컬럼 제거로 부풀려진 R² 0.614 → 0.383 정정| pandas, XGBoost, LightGBM, scikit-learn | [Binary-Ah/mimic-iv-hf-readmission](https://github.com/Binary-Ah/mimic-iv-hf-readmission) |
| **PromptGuardLite — Eval** | LLM 앱 정적 보안 스캐너의 Near-miss 샘플셋·hold-out 17개 설계, P 1.000 / R 0.889 / F1 0.941 — 2026 AI소프트웨어공모전 우수상 (샘플셋/평가 담당) | Python AST, Streamlit | [Binary-Ah/promptguardlite-eval](https://github.com/Binary-Ah/promptguardlite-eval) |
| **LSTM Chiplet Thermal Map** | gem5로 칩렛 SoC 전력 시계열을 생성하고 LSTM으로 열맵을 예측하는 파이프라인 설계 — 2024 AI반도체 아이디어/설계 경진대회 우수상 (팀장, 3인) | gem5, PyTorch | 공개 준비 중 |
| **TranslEAT — Data** | LA 식당 17,090곳·리뷰 3.5M건에서 한국어 vs 영어 평점 격차를 within-place 순열검정(p=0.001)·FDR로 검증, 파싱 버그 수정으로 한국어 리뷰 1,797 → 17,622건 — USC IMSC Hackathon 2026 | Python, gzip streaming, 통계 검정 | [Binary-Ah/translEAT-data](https://github.com/Binary-Ah/translEAT-data) · 앱 [14EE4/gmaps-culturate-extension](https://github.com/14EE4/gmaps-culturate-extension) |
| **CUDA Video Digit Recognition** | YOLO 검출 + segment 중복 제거로 등장 횟수만큼 28×28 PGM 저장, mnistCUDNN에서 cudnnFind 제거·워밍업으로 추론 수백 ms → 한 자릿수 ms — AI가속기 기말 (2인) | YOLO, OpenCV, cuDNN C++ | [Binary-Ah/cuda-video-digit-recognition](https://github.com/Binary-Ah/cuda-video-digit-recognition) |

## Awards & Publications

- **KSC2025 (한국정보과학회) 학부생 논문 경진대회 장려상** — MIMIC-IV 임상노트 전처리 비교 연구,포스터 발표 (2025.12, 여수)
- **2026 AI소프트웨어공모전 우수상** — PromptGuardLite 
- **2025 ICT프로젝트 챌린지 (숭실대 × 렛유인에듀) 최우수상** — RAG 기반 귀농 정책 플랫폼 '물어보농' (RAG 검색 파이프라인, 농Bti 기획·개발) (2025.08.30)
- **2024 AI반도체 아이디어/설계 경진대회 우수상 (숭실대학교 총장 명의)** — LSTM 기반 칩렛 열맵 예측 (팀장) (2025.01.23)
- USC Viterbi IMSC SW Pioneer Program 2026 수료 (AI · Data Science) 및 IMSC Hackathon 참가 — TranslEAT (2026.07)



## Contact

- mayjin@soongsil.ac.kr

