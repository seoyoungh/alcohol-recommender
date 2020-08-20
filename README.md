# alcohol-recommender
본 프로젝트는 IT 동아리 **TAVE**에서 진행되었습니다. 사용자의 취향을 반영한 주류 추천 앱 '술고래'를 개발해 이 프로젝트로 IT 동아리 TAVE 컨퍼런스 1위를 수상했습니다.

## Overview
* 주류 추천 어플리케이션 a.k.a **술고래**!
* 술에 대한 정보를 제공하고 추천 기능을 제공합니다.
  - 술 검색 및 정보 기능
    - 술 검색
    - 원하는 술에 대한 상세 정보 제공
    - 좋아하는 술 즐겨찾기
  - 술 추천 기능
    - 사용자가 선택한 술과 유사한 술을 추천
    - 전체 주종 내에서 추천 → 와인이면 비슷한 풍미를 가진 막걸리, 맥주 추천
    - 선택한 술과 같은 주종 내에서만 추천 → 와인이면 비슷한 와인 추천

### Data
웹에서 주류 정보를 크롤링해 자체 주류 데이터를 수집했습니다.

* Class 대분류 (총 7개)
  - wine / makgeoli / beer / vodka / soju / whisky / korean (전통주)
* Category 중분류 (총 24개)
  - 와인-레드 / 와인-화이트 / 위스키-American / 위스키-Irish / 맥주-IPA / 맥주-라거 등

### How it works?
* Content-based
  - 아이템의 내용을 분석하여 비슷한 아이템을 추천
  - 적은 정보만으로도 좋은 추천 가능

* 도수 유사도는 Euclidean distance로 구했고, 풍미 및 기타 정보의 유사도는 Cosine similarity로 구했다.
  - 텍스트의 코사인 유사도를 구하기 위해 변수를 텍스트화
  - BOW(bag of words) 활용

### 발표 자료
* [Conference Presentation](/conference_presentation.pdf)

## Developers
* [Seoyoung Hong](https://github.com/seoyoungh)
* 민지웅
* 박명진
* 안유진
* 김동현
