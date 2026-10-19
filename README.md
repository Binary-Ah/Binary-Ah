# 이진아 (Jina Lee)

숭실대학교 AI소프트웨어학부 4학년이고, ADSL 연구실에서 학부연구생으로 의료 데이터와 자연어 처리를 공부하고 있습니다.

MIMIC-IV 퇴원요약지로 사망을 예측하는 모델을 만들었을 때 AUROC가 0.99를 넘었습니다. 기뻐하기 전에 모델이 중요하게 본 단어를 열어 보니 `expired`, `deceased`, `time of death`였습니다. 환자 상태를 이해한 게 아니라 답이 적힌 문장을 읽고 있었던 것입니다. 그 뒤로는 점수를 받으면 먼저 "이 숫자가 왜 나왔는지"부터 확인합니다. 아래 프로젝트들도 대부분 그 질문에서 출발했습니다.

<br>

## 모델이 실제로 무엇을 보고 맞히는가

**[mimic-iv-note-leakage](https://github.com/Binary-Ah/mimic-iv-note-leakage)** · KSC2025 학부생 논문 경진대회 장려상 (제1저자)
위에서 말한 문제를 정리한 연구입니다. 퇴원요약지에서 결과를 암시하는 섹션과 문장을 단계적으로 걷어내며 성능과 상위 피처가 어떻게 바뀌는지 비교했습니다. 섹션만 지웠을 때도 `comfort care`(완화의료) 같은 단어가 남아 답을 흘리고 있었습니다. 입원 시점에 쓰인 섹션만 골라내는 방식(White-list)으로 바꾼 뒤에야 저혈압, 삽관처럼 임상적으로 말이 되는 단어가 위로 올라왔습니다.

**[mimic-iv-hf-readmission](https://github.com/Binary-Ah/mimic-iv-hf-readmission)** · 빅데이터분석 팀 프로젝트
심부전 환자의 30일 재입원과 재원 기간을 예측했습니다. 코호트를 직접 만들고 40GB짜리 chartevents를 나눠 읽어 첫 24시간 바이탈을 집계했습니다. 재원 기간 모델의 R²가 이상하게 높게 나와 확인해 보니, 퇴원 이후에야 알 수 있는 컬럼이 섞여 있었습니다. 그 컬럼을 빼고 다시 보고했습니다.

## 평가를 설계하고, 결과를 쪼개 보기

**[mmmu-eval-qwen3vl](https://github.com/Binary-Ah/mmmu-eval-qwen3vl)** · 멀티모달딥러닝 팀 프로젝트 중 제 담당 부분
Qwen3-VL-4B를 MMMU 벤치마크에 공식 설정 그대로 돌렸더니 논문 수치보다 6점 낮게 나왔습니다. 이 차이가 어디서 오는지 생성이 잘린 문항, 주관식, 이미지 유형별로 나눠 봤고, 주관식 문항에서 프롬프트를 바꿨을 때 실제로 달라지는지 같은 문항끼리 짝지어 검정했습니다. 다른 실험의 기준점이 되도록 실행 환경과 설정을 모두 기록해 두었습니다.

**[promptguardlite-eval](https://github.com/Binary-Ah/promptguardlite-eval)** · 2026 AI소프트웨어공모전 우수상 (평가 담당)
LLM 앱 코드의 보안 취약점을 찾는 정적 분석기를 팀으로 만들었고, 저는 그 분석기를 어떻게 평가할지를 맡았습니다. 취약한 코드와 거의 똑같지만 안전한 코드를 짝으로 만들어 오탐을 확인했고, 튜닝에 쓰지 않은 테스트셋을 따로 떼어 두었습니다. 놓친 한 건이 왜 놓쳤는지도 README에 남겼습니다.

**[koaltq-alttext-quality](https://github.com/Binary-Ah/koaltq-alttext-quality)** · KISTI 2026 DATA·AI 분석 경진대회
웹 이미지의 대체텍스트가 적절한지 7가지 유형으로 판정하는 문제입니다. 가이드라인 규칙, 가벼운 분류기, Qwen3-VL 제로샷을 각각 만들고 합쳤습니다. 유형별로 보니 "장식 이미지에 설명을 단 경우"나 "이미지와 무관한 설명"은 규칙과 가벼운 분류기로는 거의 못 맞혀서, 이미지 내용을 실제로 이해하는 모델이 필요한 부분이라는 걸 확인했습니다.

## 데이터를 직접 만들고 고친 프로젝트

**[la-review-cultural-gap](https://github.com/Binary-Ah/la-review-cultural-gap)** · USC IMSC Hackathon 2026 ([TranslEAT](https://github.com/Binary-Ah/translEAT-data))
같은 LA 식당을 한국어 리뷰어와 영어 리뷰어가 다르게 평가하는지 봤습니다. 처음에는 한국어 리뷰가 너무 적게 잡혔는데, 원인은 데이터에 원문과 구글 번역문이 한 필드에 섞여 있어서 언어 감지기가 영어로 판단한 것이었습니다. 이 필드를 분리하자 한국어 리뷰가 열 배로 늘었습니다. 가게 자체의 차이를 통제하려고 같은 가게 안에서 순열 검정을 했고, 업종이 많아 다중비교 보정도 했습니다.

**[LSTM Chiplet Thermal Map](https://github.com/Binary-Ah/LSTM-Based-Chiplet-Structure-Thermal-Map-Prediction-System)** · 2024 AI반도체 아이디어/설계 경진대회 우수상 (팀장, 3인)
칩렛 반도체의 온도 분포를 센서 없이 실시간으로 추정하자는 아이디어였습니다. 학습 데이터가 없어서 gem5 시뮬레이터에 SoC를 직접 구성해 워크로드별 성능 지표를 뽑는 것부터 시작했습니다.

**[ssu-library-datathon-2024](https://github.com/Binary-Ah/ssu-library-datathon-2024)** · **[ssu-datathon-2025-paper-trends](https://github.com/Binary-Ah/ssu-datathon-2025-paper-trends)** · 숭실대 데이터톤
2024년에는 도서관 대출 기록으로 앞으로 덜 빌려갈 책을 예측해 보존서고로 옮길 기준을 제안했습니다. 2025년에는 사회과학 논문 5만여 건을 토픽과 인용 관계로 묶어, 뉴스에서 많이 다루는 사회 이슈와 실제 연구 주제 사이에 어떤 간극이 있는지 봤습니다.

**[mureobonong-farmbti](https://github.com/Binary-Ah/mureobonong-farmbti)** · 2025 ICT프로젝트 챌린지 최우수상
흩어진 귀농 정책 문서를 검색해 주는 RAG 챗봇입니다. 저는 팀원과 정책 문서 검색 파이프라인을 만들었고, 사용자 성향 설문(농Bti)으로 맞는 지역을 추천하는 기능과 작물 수익 계산기를 맡았습니다.

## 수업에서 만든 것들

모델 바깥쪽이 어떻게 돌아가는지 알고 싶어서 시스템 쪽 수업도 꽤 들었습니다.

| | |
|---|---|
| [cuda-video-digit-recognition](https://github.com/Binary-Ah/cuda-video-digit-recognition) | 영상에서 숫자를 검출해 cuDNN으로 분류. 추론이 느린 원인이 매번 알고리즘을 다시 탐색하는 데 있다는 걸 찾아 고정 (2인) |
| [cuda-gpu-programming-basics](https://github.com/Binary-Ah/cuda-gpu-programming-basics) | 벡터 덧셈부터 cuBLAS 행렬곱까지 CPU와 비교. 문제가 작으면 GPU가 오히려 느린 이유도 기록 |
| [tidypi-edge-recycling](https://github.com/Binary-Ah/tidypi-edge-recycling) | 라즈베리파이와 Edge TPU로 쓰레기의 재질과 오염 여부를 판별해 서보로 분류하는 장치 (2인) |
| [xv6-syscall-priority-scheduler](https://github.com/Binary-Ah/xv6-syscall-priority-scheduler) | xv6에 nice 시스템콜과, 오래 기다린 프로세스가 굶지 않도록 aging을 넣은 우선순위 스케줄러 |
| [llvm-program-analysis-passes](https://github.com/Binary-Ah/llvm-program-analysis-passes) | 추상 해석으로 변수 부호를 추론하는 LLVM 패스 등 |
| [fuzzing-labs](https://github.com/Binary-Ah/fuzzing-labs) | AFL++ 실습 문제와, 커버리지를 보고 입력을 바꾸는 작은 퍼저를 직접 구현 |
| [f1tenth-platooning-ros2](https://github.com/Binary-Ah/f1tenth-platooning-ros2) | ROS2 시뮬레이터에서 앞차를 따라가는 군집주행 제어기를 단계별로 설계 |
| [clickbait-news-kobart](https://github.com/Binary-Ah/clickbait-news-kobart) | 낚시성 기사 판별용 KoBART 요약 모듈과 요약 모델 비교 실험 (팀 프로젝트 중 제 담당) |
| [cifar100-resnet-swin](https://github.com/Binary-Ah/cifar100-resnet-swin) | CIFAR-100에서 ResNet-18 베이스라인과 Swin-Tiny 전이학습 비교 |

<br>

## 그 밖에

- 서울대 IMSI 의료 AI 연구실에서 치아 배열 연구의 figure와 학회 포스터 제작을 돕고 있습니다 (2026.06~)
- USC Viterbi IMSC SW Pioneer Program 2026 수료 (AI · Data Science)

**Stack** · Python, PyTorch, Hugging Face, vLLM, scikit-learn, XGBoost, Pandas, OpenCV, CUDA, Linux GPU 서버

**Contact** · mayjin@soongsil.ac.kr
