# MemoPing 메모핑 📒✨

> 메모를 간단히 기록할 수 있는 메모핑! 메모가 어렵다구? 메모핑과 함께 간단하고 쉽게 메모할 수 있어!  
실시간 동기화를 통해 누구나 쉽게 메모를 관리할 수 있는 간단한 웹 애플리케이션입니다.  
프로젝트를 시작한 계기: https://devpearl.tistory.com/15 

# MemoPing Backend 🛠️

> Express와 MongoDB를 사용한 간단한 메모 API 서버.  
실시간 동기화를 통해 메모 데이터를 관리할 수 있는 RESTful API 서버입니다.  

## Overview

A backend server for MemoPing built with Node.js, Express, and MongoDB. The server handles memo data and synchronizes it in real-time using MongoDB's capabilities.

## Features

- 📝 **Create Memo**: API to add new memos.
- 📄 **Read Memo**: Retrieve a list of all memos.
- 🗑️ **Delete Memo**: Remove specific memos by ID.
- ✅ **Test-Driven Development**: TDD methodology applied with Vitest for backend testing.

## Tech Stack

- **Backend**: Node.js, Express
- **DataBase**: MongoDB
- **Testing**: Vitest

## Development Timeline

### **V0.0.2: 서버 구축 및 MongoDB 연결**
> **목표**: Express 서버와 MongoDB 데이터베이스 설정, API 라우트 작성 및 데이터베이스 연동, Vitest로 TDD 방식의 서버 검증.

- **기능 구현**:
  - Express 서버 설정 및 기본 라우트 구축.
  - MongoDB 연결 및 Mongoose 스키마 정의.
  - CRUD API 엔드포인트 구현 (`POST /memos`, `GET /memos`, `DELETE /memos/:id`).
  - 서버 및 데이터베이스 관련 단위 테스트 작성 (Vitest).
- **완료 목표**: `2024-`

---

### **V0.0.5: EC2 배포 및 성능 최적화**
> **목표**: AWS EC2 인스턴스에 기본적인 메모 기능과 사용자 인증 시스템이 완비된 상태에서 첫 번째 프로덕션 환경 배포.
- **기능 구현**:
  - EC2 인스턴스 설정 및 배포 환경 구성.
  - AWS RDS를 통한 MongoDB 연결 설정.
  - 기본 메모 기능과 사용자 인증을 포함한 API 안정화.
  - Nginx 또는 Apache를 사용한 리버스 프록시 설정.
  - 배포 후 기본 테스트 및 성능 모니터링 설정.
- **완료 목표**: `2024-`

---

### **V0.0.6: 사용자 피드백에 따른 기능 개선**
> **목표**: 사용자 피드백을 반영하여 메모 검색 기능, 해시태그 추가, 알림 기능을 구현해 사용자 경험을 향상.
- **기능 구현**:
  - 메모 내용과 제목을 기준으로 하는 검색 기능 (`GET /memos?search=keyword`).
  - 해시태그 기능 추가 및 관련 필터링 (`GET /memos?tags=tag1,tag2`).
  - 새로운 메모 작성 및 수정 시 실시간 알림 기능 구현.
  - 개선된 기능에 대한 테스트 작성 및 API 문서화.
- **완료 목표**: `2024-`

---

### **V1.0.1: 사용자 인증 및 세션 관리**
> **목표**: 사용자 인증 시스템 구현, 회원가입 및 로그인 기능을 통해 사용자의 접근을 제한하고 사용자 기반의 메모 관리 구현.
- **기능 구현**:
  - 사용자 등록 기능 (`POST /register`).
  - 사용자 로그인 기능 (`POST /login`).
  - JWT 또는 세션을 이용한 인증 관리.
  - 인증된 사용자만 메모 작성 및 조회 가능하도록 API 보호.
  - Vitest를 통한 인증 관련 테스트 작성.
- **완료 목표**: `2024-`

---

### **V1.0.3: MongoDB Change Stream 및 WebSocket 설정**
> **목표**: 사용자가 메모를 작성하거나 수정할 때 MongoDB Change Stream과 WebSocket을 사용하여 실시간 데이터 동기화.
- **기능 구현**:
  - MongoDB Change Stream 설정.
  - WebSocket 서버 설정 및 클라이언트 통신 처리.
  - 메모 CRUD 시 Change Stream을 통한 실시간 데이터 전송.
  - Vitest를 이용한 실시간 데이터 동기화 테스트 작성.
- **완료 목표**: `2024-`

---

### **V1.0.4: GraphQL 서버 적용**
> **목표**: GraphQL을 통해 더 유연한 데이터 요청 및 처리, MongoDB Change Stream과 GraphQL의 통합.
- **기능 구현**:
  - GraphQL 서버 설정 및 스키마 정의.
  - MongoDB Change Stream을 GraphQL 구독(subscription)과 통합.
  - 메모 CRUD 작업을 GraphQL로 구현.
  - Vitest를 통한 GraphQL API 테스트 작성.
- **완료 목표**: `2024-`

## **Backend Timeline Summary**


| 단계       | 목표                                      | 완료 목표     |
|------------|-----------------------------------------|---------------|
| **V0.0.2** | 서버 구축 및 MongoDB 연결 (TDD)             | `2024-`       |
| **V0.0.5** | EC2 배포 및 성능 최적화                         | `2024-`       |
| **V0.0.6** | 사용자 피드백에 따른 기능 개선 (검색, 해시태그, 알림) | `2024-`       |
| **V1.0.1** | 로그인 및 회원가입 기능 추가 및 세션 관리   | `2024-`       |
| **V1.0.3** | Change Stream 및 WebSocket 실시간 동기화   | `2024-`       |
| **V1.0.4** | GraphQL 서버 적용                         | `2024-`       |

## API Documentation


### **Endpoints**

- `POST /memos`: Create a new memo.
- `GET /memos`: Retrieve all memos.
- `GET /memos?search=keyword`: Search for memos by keyword.
- `GET /memos?tags=tag1,tag2`: Filter memos by hashtags.
- `DELETE /memos/:id`: Delete a memo by its ID.
