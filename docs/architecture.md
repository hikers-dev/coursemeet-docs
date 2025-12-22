# Architecture

## 1. 시스템 구조도

코스밋은 **Client / Server 분리 구조**를 기반으로 동작합니다.

```text
[ Client Application ]
        |
        |  API Communication
        |
[ Server Application ]
        |
        |  Data Access
        |
[ Database ]
```

## 2. 파일 구조

**역할과 책임을 기준으로 디렉토리를 분리**하여 UI, 상태 관리, 비즈니스 로직이 서로 독립적으로 유지되도록 구성했습니다.

이 구조는 다음 원칙을 기반으로 합니다.

- 화면(UI)과 비즈니스 로직의 명확한 분리
- 상태 관리 로직의 책임 범위 구분
- 재사용 가능한 컴포넌트 중심 설계

```text
src/
 ├─ apis        # 서버 API 요청 정의
 ├─ auths       # 인증/인가 관련 로직
 ├─ components  # 재사용 가능한 UI 컴포넌트
 ├─ constants   # 공통 상수 및 설정 값
 ├─ contexts    # React Context 기반 전역 상태
 ├─ hooks       # 커스텀 훅
 ├─ navigators  # 화면 이동 및 네비게이션 설정
 ├─ pages       # 화면 단위 컴포넌트
 ├─ queries     # 데이터 조회 및 캐싱 로직
 ├─ services    # 비즈니스 로직 계층
 ├─ stores      # 전역 상태 관리
 ├─ utils       # 공통 유틸리티 함수
 └─ App.js      # 애플리케이션 진입점
```

## ⚙️ 기술 스택

<table>
  <thead>
    <tr>
      <th>분류</th>
      <th>기술 스택</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>프론트엔드</td>
      <td>
        <img src="https://img.shields.io/badge/React_Native-%2320232a.svg?logo=react&logoColor=%2361DAFB"/>
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=000"/>
        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white"/>
        <img src="https://img.shields.io/badge/styled--components-DB7093?logo=styledcomponents&logoColor=fff"/>
        <img src="https://img.shields.io/badge/zustand-orange?style=flat&logo=zustand&logoColor=white"/>
      </td>
    </tr>
    <tr>
      <td>백엔드</td>
      <td>
        <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white"/>
        <img src="https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white"/>
        <img src="https://img.shields.io/badge/Gradle-02303A?style=flat&logo=gradle&logoColor=white"/>
      </td>
    </tr>
    <tr>
      <td>데이터베이스</td>
      <td>
        <img src="https://img.shields.io/badge/Postgres-%23316192.svg?logo=postgresql&logoColor=white"/>
        <img src="https://img.shields.io/badge/Redis-%23DD0031.svg?logo=redis&logoColor=white"/>
      </td>
    </tr>
    <tr>
      <td>인프라</td>
      <td>
        <img src="https://custom-icon-badges.demolab.com/badge/AWS-%23FF9900.svg?logo=aws&logoColor=white"/>
        <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=fff"/>
      </td>
    </tr>
  </tbody>
</table>

---

> 🏡 [README](../README.md)<br>[⬅️ Core Features](core-features.md)<br> [➡️ Roadmap](roadmap.md)
