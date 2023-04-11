# 🏆 Level 1 Projects :: STS(Semantic Text Similarity)
>의미 유사도 판별(Semantic Text Similarity, STS)이란 두 문장이 의미적으로 얼마나 유사한지를 수치화하는 자연어처리 태스크입니다.

## 🧑🏻‍💻 Team Introduction & Members 

> 네이버까지 들어가조 [ NLP 11조 ] 

### Members
강민재|김주원|김태민|신혁준|윤상원|
:-:|:-:|:-:|:-:|:-:
<img src='https://avatars.githubusercontent.com/u/39152134?v=4' height=80 width=80px></img>|<img src='https://avatars.githubusercontent.com/u/81630351?v=4' height=80 width=80px></img>|<img src='https://avatars.githubusercontent.com/u/96530685?v=4' height=80 width=80px></img>|<img src='https://avatars.githubusercontent.com/u/96534680?v=4' height=80 width=80px></img>|<img src='https://avatars.githubusercontent.com/u/38793142?v=4' height=80 width=80px></img>
[Github](https://github.com/mjk0618)|[Github](https://github.com/Kim-Ju-won)|[Github](https://github.com/taemin6697)|[Github](https://github.com/jun048098)|[Github](https://github.com/SangwonYoon)
kminjae618@gmail.com|kjwt1124@hufs.ac.kr|taemin6697@gmail.com|jun048098@gmail.com|iandr0805@gmail.com

## 💻 Baseline Code 사용법
```bash
#학습 명령어 
python3 code/train.py
#예측 명령어 output.csv 생성
python3 code/inference.py 
```

## 📐 Github Push Ground Rule

1. git add 이전에 repository에 올라가면 안되는 파일들(데이터)이 `.gitignore`안에 들어있는지 확인하기
    -  만약 `.gitignore`에 없으면 파일을 추가해주세요. 
    - 기본적으로 data안에 들어가 있는 모든 파일들은 push 했을 때 remote 주소로 올라가지 않으니 train, test, dev 파일들은 생성시 data폴더를 만들어 해당 폴더 내부에 넣어주시는 걸 추천합니다.

2. `git commit` 이전에 본인의 branch가 맞는지 확인해주세요. (branch가 본인의 initial과 같은지 확인) 만약 아니라면 아래 명령어를 통해 본인의 브랜치로 반드시 변경해주세요.
```bash
# git checkout [본인브랜치 이름(이니셜)]
# 예시 
git switch KJW
```

3. 이번 프로젝트의 commit 단위는 **한번 submission**할 때 마다  커밋 하는 것을 원칙으로 합니다. 아래 예시를 보고 **코드 수정 내용, 점수, 제출 시간**이 들어가도록 commit 해주시면 됩니다. 

```bash
# git commit -am [코드 수정 사항] [public score 점수] [시간(연도.월.일 시간:분)]
# 예시 : 
git commit -am "Use HuggingFace Alectrica model score 97 23.04.11 18:50"
```

## 📁 프로젝트 구조
```
level1_semantictextsimilarity-nlp-11
 ┣ code
 ┣ data
 ┃ ┣ dev.csv
 ┃ ┣ test.csv
 ┃ ┗ train.csv
 ┣ .gitignore
 ┗ Readme.md
 ```


## 🗓️ 프로젝트 일정
- 프로젝트 전체 기간 (2주) : 4월 10일 (월) 10:00 ~ 4월 20일 (목) 19:00
  - 팀 병합 기간 : 4월 11일 (화) 16:00 까지
    - 팀명 컨벤션 : 도메인팀번호(2자리)조 / ex) CV_03조, NLP_02조, RecSys_08조
  - 리더보드 제출 오픈 : 4월 12일 (수) 10:00
  - 최종 리더보드 (Private) 공개 : 4월 20일 (목) 19:00
- GPU 서버 할당 : 4월 10일 (월) 10:00
- GPU 서버 회수 : 4월 28일 (금) 16:00

## 💯 평가 방법 : 

- 피어슨 상관 계수(Pearson Correlation Coefficient ,PCC)는 두 변수 X 와 Y 간의 선형 상관 관계를 계량화한 수치로, 보통 상관관계라 함은 피어슨 상관관계를 칭합니다.

- 코시-슈바르츠 부등식에 의해 -1~1 사이의 값을 가지며, +1은 완벽한 양의 선형 상관 관계, 0은 선형 상관 관계 없음, -1은 완벽한 음의 선형 상관 관계를 의미합니다

- 피어슨 상관 계수는 정답과 예측이 일치하지 않더라도 증감율이 일치하면 1에 가까운 값을 보입니다.

- 반대로 정답값과 예측이 근사하더라도 증감율이 다르면 -1에 가까운 값을 보일 수 있습니다.

- 이는 정답을 정확히 예측하는 것 보다, 높은 값은 확실히 높게, 낮은 값은 확실히 낮게, 즉 전체적인 경향을 잘 예측하는 것이 중요함을 의미합니다.

## 📚 프로젝트 소개

보고서나 논문 등의 정보 전달 목적의 글을 쓰다보면, 같은 말을 반복해서 쓰게 되는 경우가 많습니다. 중복된 문장들은 가독성을 떨어뜨리는 요인 중 하나로써, 글의 퀄리티가 낮아지게 만들죠. 이런 경우 인간은 교정 작업을 하며, 의미적으로 중복된 문장을 인지하고 수정하게 됩니다. 그렇다면 기계의 경우 서로 구조적으론 다르지만, 의미가 유사한 것을 어떻게 구별할 수 있을까요?

- 이런 경우에 사용할 수 있는 Task가 바로, Semantic Text Similarity (STS)입니다. STS란 두 텍스트가 얼마나 유사한지 판단하는 NLP Task입니다. 일반적으로 두 개의 문장을 입력하고, 이러한 문장쌍이 얼마나 의미적으로 서로 유사한지를 판단합니다.

- 관계를 예측한다는 점에서 Textual Entailment (TE)와 헷갈릴 수 있습니다. 두 문제의 가장 큰 차이점은 ‘방향성’입니다. STS는 두 문장이 서로 동등한 양방향성을 가정하고 진행되지만, TE의 경우 방향성이 존재합니다. 예를 들어 자동차는 운송수단이지만, 운송수단 집합에 반드시 자동차만 있는 것은 아닙니다. 또한 출력 형태에 대해서도 차이가 있습니다. TE, STS 모두 관계 유사도에 대해 참/거짓으로 판단할 수 있지만, STS는 수치화된 점수를 출력할 수도 있습니다.

- 이처럼 STS의 수치화 가능한 양방향성은 정보 추출, 질문-답변 및 요약과 같은 NLP 작업에 널리 활용되고 있습니다. 실제 어플리케이션으로는 데이터 증강, 챗봇의 질문 제안, 혹은 중복 문장 탐지 등에 응용되고 있습니다.

우리는 STS 데이터셋을 활용해 두 문장의 유사도를 측정하는 AI모델을 구축할 것입니다. 유사도 점수와 함께 두 문장의 유사함을 참과 거짓으로 판단하는 참고 정보도 같이 제공하지만, 최종적으로 0과 5사이의 유사도 점수를 예측하는 것을 목적으로 합니다!

학습 데이터셋 9,324개, 검증 데이터셋 550개, 평가 데이터는 1,100개가 제공됩니다. 평가 데이터의 50%는 Public 점수 계산에 활용되어 실시간 리더보드에 표기가 되고, 남은 50%는 Private 결과 계산에 활용되어 대회 종료 후 평가됩니다.

본 대회의 최종 결과물은 CSV 확장자 파일을 제출하게 됩니다.

- input : 두 개의 문장과 ID, 유사도 정보가 담긴 CSV 파일
- output : 평가데이터에 있는 각 문장쌍에 대한 ID와 유사도 점수가 담긴 CSV 파일


## 📏 대회 룰

- **[대회 참여 제한]** NLP 도메인을 수강하고 있는 캠퍼에 한하여 리더보드 제출이 가능합니다.

- **[팀 결성 기간]** 팀 결성은 대회 시작 2일차 화요일 오후 4시까지 필수로 진행합니다. 팀이 완전히 결성되기 전까지는 리더보드 제출이 불가합니다.

- **[일일 제출횟수]** 일일 제출횟수는 팀 단위 10회로 제한합니다. (일일횟수 초기화는 자정에 진행)

- **[외부 데이터셋 규정]** 본 대회에서는 외부 데이터셋 사용을 금지합니다. (외부 데이터에 의존하는 것이 아니라, 주어진 데이터셋을 기반으로 모델링 성능 개선에 집중해 보시길 바랍니다)

- **[기학습 가중치 사용]** 저작권상 사용이 불가한 경우를 제외하고는 모든 기학습 가중치 사용은 허용됩니다.

- **[테스트셋 활용 가능 여부]** 참가자는 모델 학습에 테스트셋을 활용하거나, 테스트셋의 정보를 학습에 활용하여 최종 결과를 낼 수 없습니다.

- **[데이터 증강]** Train/Dev 데이터에 한해 증강 가능합니다. 다만 기술적/통계적 근거가 존재해야하며, 누구나 동일한 증강 결과물을 생성할 수 있어야 합니다.

- **[데이터셋 저작권]** 대회 데이터셋은 '캠프 교육용 라이선스' 아래 사용 가능합니다. 저작권 관련 세부 내용은 부스트코스 공지사항을 반드시 참고 해주세요.

### AI Stages 대회 공통사항

- **[Private Sharing 금지]** 비공개적으로 다른 팀과 코드 혹은 데이터를 공유하는 것은 허용하지 않습니다.코드 공유는 반드시 대회 게시판을 통해 공개적으로 진행되어야 합니다.

- **[최종 결과 검증 절차]** 리더보드 상위권의 경우 추후 최종 코드 검수가 진행됩니다. 반드시 결과가 재현될 수 있도록 최종 코드를 정리해 주세요! 부정행위가 의심될 경우에는 결과 재현을 요구할 수 있으며, 재현이 어려울 경우 리더보드 순위표에서 제외될 수 있습니다.

- **[공유 문화]** 공개적으로 토론 게시판을 통해 모델링에 대한 아이디어 혹은 작성한 코드를 공유하실 것을 권장 드립니다. 공유 문화를 통해서 더욱 뛰어난 모델을 대회 참가자 분들과 같이 개발해 보시길 바랍니다.

- **[대회 참가 기본 매너]** 좋은 대회 문화 정착을 위해 아래 명시된 행위는 지양합니다.
  - 대회 종료를 앞두고 (3일 전) 높은 점수를 얻을 수 있는 전체 코드를 공유하는 행위
  - 타 참가자와 토론이 아닌 단순 솔루션을 캐내는 행위
