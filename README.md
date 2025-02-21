# 🎵 Andante - 악기 연습을 위한 SNS 플랫폼

<a href="https://www.adte.site/" target="_blank">
<img src="https://github.com/user-attachments/assets/6e382b3d-e578-4139-8163-5ca022566f81" alt="" width="800">
</a>
<br/>
<br/>
<br/>

## 📹영상 포트폴리오
<a href="https://www.youtube.com/watch?v=tuLfJ0rAK-c" target="_blank">

[![YouTube 영상](https://img.youtube.com/vi/tuLfJ0rAK-c/maxresdefault.jpg)](https://www.youtube.com/watch?v=tuLfJ0rAK-c)

</a>

<br/>
<br/>

## 📌 소개  
**Andante**는 음악 연습을 지속할 수 있도록 돕는 **악기 연습 기반의 SNS 플랫폼**입니다.  
사용자는 자신의 연주 영상을 업로드하고, **원곡과 비교하여 점수를 제공**받으며, 이를 공유하고 피드백을 받을 수 있습니다.  
게이미피케이션 요소(뱃지, 레벨, 챌린지 시스템)를 통해 성취감을 높이고, 꾸준한 연습을 유도합니다.

## 🧐 기획 배경  
🎼 "나도 악기 하나쯤은…" 하지만 꾸준한 연습은 어렵다.  
🎼 즉각적인 성취감을 느끼기 힘들고, 성장 과정을 시각적으로 확인하기 어렵다.  
🎼 비슷한 수준의 연습자들과 교류할 기회가 적다.

Andante는 이러한 문제를 해결하기 위해 **연습 공유 & 피드백, 게이미피케이션, 맞춤형 큐레이션** 기능을 제공합니다.


## 👨‍💻 팀원 소개  
| 이재백 | 배성훈 | 박성문 | 
|:------:|:------:|:------:|
| <img src="https://github.com/user-attachments/assets/fe698c35-ac76-4097-85f8-9dbe4f6d63b1" alt="이재백" width="200"> | <img src="https://github.com/user-attachments/assets/bcb3f8d5-fa81-4859-9dec-2e38e1a6aadf" alt="배성훈" width="200"> | <img src="https://github.com/user-attachments/assets/33151352-cf18-4c5e-9e70-610b7810aa21" alt="박성문" width="200"> |
| FE(Leader) | FullStack <br> Infra | FullStack <br> Principal Research Engineer |
| [GitHub](https://github.com/beak1sin) | [GitHub](https://github.com/baehoonbae) | [GitHub](https://github.com/SungMoonPark) |

| 이주현 | 윤병희 | 오상하 | 
|:------:|:------:|:------:|
| <img src="https://github.com/user-attachments/assets/3b8cdfce-3502-4e1d-a84b-a5b9844d92a1" alt="이주현" width="200"> | <img src="https://github.com/user-attachments/assets/5761aec8-84ad-46bd-a55e-b3d9156009fc" alt="윤병희" width="200"> | <img src="https://github.com/user-attachments/assets/63789b81-19eb-4cd5-8e3c-f8335fd2eb82" alt="오상하" width="200"> |
| BE <br> Development Team Leader | BE <br> Video Editor | BE <br> DBA |
| [GitHub](https://github.com/column-wise) | [GitHub](https://github.com/Dylan-yoon) | [GitHub](https://github.com/tkdgk1204) |


---

## 🔥 핵심 기능  

### 🎯 **1. 챌린지 기능**  
- 연주 영상 업로드 후 원곡과 비교하여 점수 부여  
- AI 기반 **음원 분석 (Librosa)** 을 통해 **템포, 피치, 음색 유사도 측정**  
- 챌린지 성공 시 **스트릭 유지 및 경험치/뱃지 획득**  

### 📝 **2. 피드 시스템**  
- 연주 영상을 피드에 공유하고, 댓글 & 좋아요로 소통  
- 인기 챌린지 및 맞춤형 추천 기능  

### 🏆 **3. 게이미피케이션**  
- **스트릭(Streak) 시스템**: 연속 연습 시 보상  
- **레벨 & 뱃지 시스템**: 성취도에 따른 시각적 보상 제공  

### 📢 **4. 추천 시스템**  
- AI 기반 **선호도 분석**을 활용하여 맞춤형 챌린지 추천  

---

## 🛠️ 기술 스택  

| 분야       | 사용 기술  |
|------------|-----------|
| **Frontend** | React, TypeScript |
| **Backend**  | Spring Boot, JPA |
| **Database** | MySQL, Redis |
| **AI 분석**  | Python Librosa (음원 분석) |
| **Storage**  | AWS S3 (Presigned URL) |
| **Messaging** | Redis Stream (Message Queue) |
| **Communication** | Server-Sent Events (SSE) |

---


## 🏗️ 시스템 아키텍처  

### 🔗 **1. 사용자(User)와 인증 시스템**
- **네이버, 카카오 인증 연동**  
  - 사용자는 네이버, 카카오 소셜 로그인을 통해 인증 가능.  
  - 인증된 사용자는 **React 프론트엔드**와 상호작용하여 서비스를 이용.  

### 🎨 **2. 프론트엔드 (React)**
- **주요 기술 스택**  
  - **React**: UI 프레임워크  
  - **TypeScript**: 안정적인 타입 기반 개발  
  - **Redux** (or Zustand 등): 상태 관리  
  - **Axios**: API 통신
  - **Styled-components** 또는 Tailwind: UI 스타일링  

- **역할**  
  - 사용자 인터페이스를 제공하고, 백엔드 API와 통신.  
  - **AWS S3**에 영상 파일을 업로드할 수 있도록 Presigned URL 사용.  

### 🛠 **3. 백엔드 (Spring Boot)**
- **주요 기술 스택**  
  - **Spring Boot**: 전체 서버 애플리케이션을 관리.  
  - **Spring Security**: 인증 및 보안 관리.  
  - **JPA (Hibernate)**: MySQL과 데이터 연동.  
  - **JWT**: 사용자 인증 및 세션 유지.  

- **역할**  
  - 프론트엔드 요청을 처리하고, 유사도 분석 요청을 메시지 큐(Redis Stream)로 전달.  

### 🗄 **4. 데이터 저장소 (AWS S3 & MySQL)**
- **AWS S3**  
  - 사용자가 업로드한 연주 영상을 저장.  
  - Presigned URL을 활용하여 트래픽을 최적화.  

- **MySQL**  
  - 사용자 정보, 챌린지 기록, 점수 데이터를 저장.  

### 🚀 **5. 유사도 분석 시스템 (Redis Stream & AI 분석)**
#### 🔴 **Redis Stream (Message Queue)**
- **Spring Boot에서 Redis Stream으로 유사도 분석 요청을 전송**하면, 여러 개의 AI 분석 서버가 이를 소비(Consume)하여 결과를 생성.  

- **특징**  
  - 요청을 **비동기 처리**하여 서버 부하를 줄임.  
  - 여러 개의 **Consumer(유사도 분석 서버)** 가 병렬로 작업하여 성능 최적화.  

#### 🔵 **유사도 분석 AI (Python)**
- **Librosa, Numpy 등의 라이브러리를 사용하여 유사도 분석** 수행.
- **빠른 실시간 처리**, **구간 별 유사도** 등을 통해 유저 경험을 개선   
- **유사도 분석 방법론**  
  1. **Onset Detect**: 템포 분석.
  2. **Chroma, Piptrack**: 피치 분석.  
  3. **DTW(Dynamic time warping), Overlap**: 시간 축 보정.

- 분석 결과는 **Redis Stream을 통해 전달**되고, 이후 백엔드(Spring Boot)가 최종 결과를 클라이언트(React)로 전송.  

---

## 🎯 **아키텍처의 강점**
✅ **비동기 유사도 분석**: Redis Stream을 활용하여 빠른 응답 처리.  
✅ **확장성 높은 설계**: AI 분석 서버를 늘려 부하 분산 가능.  
✅ **클라우드 스토리지 (AWS S3) 활용**: 안정적인 영상 업로드.  
✅ **사용자 친화적 인증 시스템**: 네이버/카카오 로그인 지원.  

---

## 📈 기대 효과  

✅ **성취감을 통한 연습 지속성 향상**  
✅ **음악 커뮤니티 형성 & 사용자 간 교류 활성화**  
✅ **AI 기반 데이터 추천으로 개인 맞춤형 챌린지 제공**  

---

## 🚀 향후 개선 방향  

📌 **유사도 분석 알고리즘 개선**  
📌 **다양한 악기 추가 지원**  
📌 **대중 가요 챌린지 도입 (저작권 계약 진행)**  
📌 **사용자 피드백을 반영한 UI/UX 개선**  
📌 **글로벌 시장 진출 고려**  

---

## 📢 Q&A  

**Q. 유사도 분석 정확도는?**  
A. 음원 업로드 시 30~50%, 연주 영상 업로드 시 60~90% 정확도를 가집니다.

**Q. 수익 모델은?**  
A. 유사도 분석 요청 시 광고를 시청하도록 하는 방식입니다.

**Q. 업로드 용량 제한은?**  
A. 최대 500MB로 설정되어 있으며, 8분 길이의 연주도 지원됩니다.
