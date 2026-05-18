---
title: Joo Movie (Netflix 클론)
date: 2024-08-01
image:
  focal_point: 'top'
---

[🎬 Live Demo](https://joomovie.netlify.app/) ・ [🐙 GitHub Repository](https://github.com/wldnek03/jiwoo.github.io)

## 프로젝트 개요

Netflix의 UI와 기능을 클론한 웹 애플리케이션입니다. **React**를 사용해 개발했으며, 사용자 인터페이스는 Netflix와 유사하게 구성했습니다. 학습 목적으로 만들어진 프로젝트이며, 배포는 **Netlify**를 사용했습니다.

## 기능

- **로그인**: 로그인 ↔ 회원가입 전환 시 애니메이션 적용, 로그인 시 헤더의 로그인 표시가 이메일의 첫 부분과 로그아웃 표시로 변경, 로그인 시 패스워드는 TMDB에서 발급받은 API 사용
- **홈 화면**: 배너에 인기 영화 포스터·제목·상세 설명 표시 및 재생/상세 설명 버튼, 배너 밑으로 인기 영화 및 다양한 TV 프로그램 목록 표시, 포스터 클릭 시 하트 표시와 함께 위시리스트에 저장
- **인기작**: 그리드 뷰와 리스트 뷰로 인기 영화 표시, 그리드 뷰는 스크롤 차단 + 페이지네이션 기능, 리스트 뷰는 무한 스크롤 기능, top 버튼으로 맨 위로 이동, 포스터 클릭 시 위시리스트 저장
- **검색 기능**: 영화 및 TV 프로그램 검색, 포스터 클릭 시 상세정보 및 트레일러 확인, 최신 검색 기록 저장, 장르 · 평점 · 언어 · 정렬 기준에 따라 정렬, 초기화 버튼으로 기본 인기영화 목록 복원
- **상세 페이지**: 각 영화 및 TV 프로그램에 대한 세부 정보 및 트레일러 제공
- **위시리스트**: 홈 화면과 인기작에서 저장한 포스터들 표시
- **반응형 디자인**: 다양한 디바이스에서 최적화된 UI 제공

## 홈페이지

🔗 [Joo Movie — joomovie.netlify.app](https://joomovie.netlify.app/)

## 기술 스택

- **Frontend**: React, JavaScript, HTML, CSS
- **상태 관리**: React Hooks (`useState`, `useEffect`)
- **스타일링**: CSS
- **API**: TMDB API (영화 데이터 제공)
- **배포**: Netlify
<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>
