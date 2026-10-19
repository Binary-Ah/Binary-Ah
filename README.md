# 이진아 (Jina Lee)

 의료 데이터·멀티모달 모델의 **데이터 파이프라인과 평가**를 주로 다룹니다.



## Stack

`Python` `PyTorch` `Hugging Face Transformers / datasets` `vLLM` `scikit-learn` `XGBoost / LightGBM` `Pandas` `OpenCV` `Streamlit` `CUDA / cuDNN (수업)` `Linux GPU 서버` `Git`

## Featured projects

| 프로젝트 | 한 줄 | 스택 | 링크 |
|---|---|---|---|
| **MMMU Eval Pipeline (Qwen3-VL-4B)** | Qwen3-VL-4B를 공식 설정으로 MMMU-val에 재현하고, 공식 수치와의 차이를 문항 유형·이미지 유형별로 분석. 프롬프트 변경 실험으로 주관식 문항 개선 여부 검증 | vLLM, HF datasets, Python | [Binary-Ah/mmmu-eval-qwen3vl](https://github.com/Binary-Ah/mmmu-eval-qwen3vl) · 팀 레포 [Chaeeun4/MMDL](https://github.com/Chaeeun4/MMDL) |
| **MIMIC-IV Note Leakage Study** | 퇴원요약지에서 결과를 암시하는 섹션·문장을 단계적으로 제거하며, 모델이 학습하는 피처가 사망 관련 단어에서 임상 피처로 바뀌는 것을 확인 — KSC2025 장려상 (제1저자) | Bio_ClinicalBERT, XGBoost, LR | [Binary-Ah/mimic-iv-note-leakage](https://github.com/Binary-Ah/mimic-iv-note-leakage) |
| **MIMIC-IV HF Readmission** | 심부전 입원 코호트를 구성해 30일 재입원·재실기간 예측, 대용량 chartevents 청크 처리, 재실기간 모델의 누수 컬럼 제거 | pandas, XGBoost, LightGBM, scikit-learn | [Binary-Ah/mimic-iv-hf-readmission](https://github.com/Binary-Ah/mimic-iv-hf-readmission) |
| **PromptGuardLite — Eval** | LLM 앱 정적 보안 스캐너의 평가셋(취약/안전 코드 쌍, hold-out 테스트셋) 설계 및 성능 평가 — 2026 AI소프트웨어공모전 우수상 (샘플셋/평가 담당) | Python AST, Streamlit | [Binary-Ah/promptguardlite-eval](https://github.com/Binary-Ah/promptguardlite-eval) |
| **LSTM Chiplet Thermal Map** | gem5로 칩렛 SoC 성능 지표를 생성하고 LSTM으로 열맵을 예측하는 파이프라인 설계 — 2024 AI반도체 아이디어/설계 경진대회 우수상 (팀장, 3인) | gem5, PyTorch | [Binary-Ah/LSTM-Based-Chiplet-…](https://github.com/Binary-Ah/LSTM-Based-Chiplet-Structure-Thermal-Map-Prediction-System) |
| **TranslEAT — Data** | LA 식당 Google 리뷰에서 한국어·영어 리뷰의 평점 차이를 집계·검정, 원문/번역문이 섞인 필드를 분리해 한국어 리뷰 누락 문제 해결 — USC IMSC Hackathon 2026 | Python, gzip streaming, 통계 검정 | [Binary-Ah/translEAT-data](https://github.com/Binary-Ah/translEAT-data) · 앱 [14EE4/gmaps-culturate-extension](https://github.com/14EE4/gmaps-culturate-extension) |
| **CUDA Video Digit Recognition** | 영상에서 YOLO로 숫자를 검출해 cuDNN으로 분류, 추론 병목(매 호출 알고리즘 탐색)을 찾아 제거 — AI가속기 기말 (2인) | YOLO, OpenCV, cuDNN C++ | [Binary-Ah/cuda-video-digit-recognition](https://github.com/Binary-Ah/cuda-video-digit-recognition) |

## Awards & Publications

- **KSC2025 (한국정보과학회) 학부생 논문 경진대회 장려상** — MIMIC-IV 임상노트 전처리 비교 연구, 포스터 발표 (2025.12, 여수)
- **2026 AI소프트웨어공모전 우수상** — PromptGuardLite
- **2025 ICT프로젝트 챌린지 (숭실대 × 렛유인에듀) 최우수상** — RAG 기반 귀농 정책 플랫폼 '물어보농' (RAG 검색 파이프라인, 농Bti 기획·개발) (2025.08.30)
- **2024 AI반도체 아이디어/설계 경진대회 우수상 (숭실대학교 총장 명의)** — LSTM 기반 칩렛 열맵 예측 (팀장) (2025.01.23)
- USC Viterbi IMSC SW Pioneer Program 2026 수료 (AI · Data Science) 및 IMSC Hackathon 참가 — TranslEAT (2026.07)



## Contact

- mayjin@soongsil.ac.kr
