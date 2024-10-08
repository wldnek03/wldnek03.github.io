---
title: 데이터베이스를 활용한 전주 맛집 추천 웹사이트
date: 2024-05-01
image:
  focal_point: "top"
---

전주에 숨은 맛집들을 소개하는 웹사이트를 개발했습니다. 
이 프로젝트는 약 80개의 지역 맛집 데이터를 모아 사용자들이 다양한 식사 옵션을 발견하고 탐색할 수 있도록 하는 것을 목표로 했습니다.

**데이터베이스 설계 및 구현**
맛집 추천 게시판, 맛집 정보, 사용자 리뷰와 같은 기능을 지원하기 위해, recommend_board, restaurants, reviews의 세 가지 주요 테이블로 구성된 데이터베이스를 설계하고 구현했습니다.

**사용자 인터페이스 및 경험**
홈 화면 상단에는 식당 이름을 검색하는 창과 동별로 맛집을 모아볼 수 있는 섹션, 음식 종류별로 모아볼 수 있는 섹션이 구현되어 있습니다. 그 아래에는 맛집 추가 및 추천 게시판 섹션이 있습니다.

예를 들어, 중화산동을 선택하면 각 식당의 이름, 음식 종류, 메뉴가 표시되는 목록을 볼 수 있습니다. 마찬가지로 음식 종류별 맛집에서 일식을 선택하면, 각 식당의 이름과 위치, 메뉴를 확인할 수 있는 화면이 나옵니다.

특정 식당을 클릭하면 깐쇼새우와 같은 상세 화면이 나타납니다. 이 화면에서는 식당의 위치, 카테고리, 메뉴, 간단한 소개와 대표 메뉴의 사진이 제공됩니다. 또한, 아래쪽에서 리뷰를 읽고 작성할 수 있는 기능이 마련되어 있습니다. 리뷰 작성 버튼을 클릭하면 평점과 코멘트를 작성할 수 있는 화면으로 이어집니다.

**추가 기능**
추천 게시판 섹션을 구현하여 사용자들이 자신이 좋아하는 맛집을 다른 사용자들에게 추천하는 글을 작성할 수 있도록 하였습니다. 또한, 맛집 추가 기능도 구현하여 사용자들이 맛집 이름, 위치, 음식 종류, 특징, 소개를 입력하고 이미지를 첨부하여 새로운 맛집을 추가할 수 있습니다.

**소프트웨어 및 개발 환경**
- 프론트 엔드 : css, javascript, html

- 백엔드 : Express

- 데이터베이스 : Mysql
<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>