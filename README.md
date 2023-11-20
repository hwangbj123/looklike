> # LOOKLIKE
온라인 쇼핑몰을 주제로 한 Spring Project 입니다

> # Description
- 기간 : 23.06.19 ~ 23.07.11
- 인원 : 4 명
- 사용 기술

  ![그림8](https://github.com/hwangbj123/looklike/assets/136680186/0479e94f-0318-489b-83cf-d950ee567c6e)
  ![그림2](https://github.com/hwangbj123/looklike/assets/136680186/1d88c213-ee27-4020-945a-2df01b899db7)
  ![그림4](https://github.com/hwangbj123/looklike/assets/136680186/3510fc77-82e7-4dc1-9f51-25c2d020ed3f)
  ![그림6](https://github.com/hwangbj123/looklike/assets/136680186/bd405b34-a493-4038-ad20-50486a9d5b83)
  ![그림5](https://github.com/hwangbj123/looklike/assets/136680186/53759f1a-4f49-4f44-88b5-3e0867ac2731)
  ![그림7](https://github.com/hwangbj123/looklike/assets/136680186/6cbb67b3-08c1-4914-a830-69350d9c295e)

  \+ myBatis, JavaScript(JQuery, Ajax)
> # 담당 파트

#### 로그인 & 회원가입
1. 회원가입 시 ID, Email 중복 및 유효성 검사
2. ID, Email 정보로 비밀번호 찾기 시 Email 인증 번호 발송 및 확인, 임시 비밀번호 발급 처리
3. 회원 개인정보 수정 및 탈퇴
4. kakao 와 Naver API 를 활용한 소셜 로그인 기능
5. 로그인 정보를 저장해 로그인을 유지할 수 있도록 세션 기능 구현
#### 마이페이지
1. 회원 정보 조회 및 수정
2. 장바구니, 관심내역, 결제내역, 문의내역 확인
3. 배송 중, 환불완료 등의 주문내역 현황 확인
#### 장바구니 & 관심내역
1. 상품 정보를 저장할 수 있는 장바구니 기능
2. 장바구니에 추가한 다수의 상품을 한 번에 구매
3. 상품 정보를 저장할 수 있는 관심내역(위시리스트) 기능
4. 장바구니와 관심내역 모두 해당 상품의 상세 사이트로 이동할 수 있으며, 목록에서 삭제
#### 결제
1. 아임포트 플랫폼에서 KICC, 카카오페이 결제 API 코드를 받아 결제 기능
2. 결제 정보를 통한 환불 기능
3. 결제 및 환불 시 해당 상품 거래 개수만큼 상품 테이블의 재고 개수 처리

> # Views
### 메인 페이지

https://github.com/hwangbj123/looklike/assets/136680186/259a78af-3b85-4b91-8b16-4491db035c35

- JavaScript 환경에서 bxSlider 라이브러리를 활용하여 이미지 슬라이드
- JQuery 및 CSS 를 활용하여 메뉴 확장 애니메이션 구현

### 로그인 페이지

https://github.com/hwangbj123/looklike/assets/136680186/6ddca53b-3886-4994-8101-c31a80c96450

- JQuery 및 CSS 를 활용하여 로그인/회원가입 UI 분리
- 네이버 및 카카오 로그인 API 연동
- 아이디 찾기
  + 이메일과 이름을 통해 아이디 확인 가능
- 비밀번호 찾기
  + 아이디와 이메일로 회원 정보 확인
  + 회원 정보 확인될 경우 해당 이메일로 인증번호 발송
  + 인증번호 확인 후 임시 비밀번호 공지 및 적용

### 상품 상세 페이지

![그림10](https://github.com/hwangbj123/looklike/assets/136680186/83049845-0f75-4216-95a3-5adc60bdd017)

### 장바구니

![그림12](https://github.com/hwangbj123/looklike/assets/136680186/2b80530f-1b56-47b0-bf2f-6050ccd2a468)

- 상품 상세 페이지에서 장바구니에 상품 추가
- Ajax 를 활용하여 개수 조정 시 실시간 DB 적용

### 결제

![그림13](https://github.com/hwangbj123/looklike/assets/136680186/8023798f-bef1-44d3-965d-0d4590a0b544)
![그림14](https://github.com/hwangbj123/looklike/assets/136680186/c1623de7-8824-473c-a684-57719c1b88ce)

- 상품 상세 페이지에서 해당 상품 단일 결제
- 장바구니 페이지에서 장바구니 목록 일괄 결제
- 상품 명 표시, 다수 상품 결제 시 상품명 \+ '외 n개'
- 개수 조정 시 총 합산 가격 자동으로 계산하여 표시

![그림15](https://github.com/hwangbj123/looklike/assets/136680186/aa73ee20-f75f-4f2b-babf-be9dcb4a79c7)

- 카카오페이 & KICC 결제 API 적용

### 결제내역

![그림16](https://github.com/hwangbj123/looklike/assets/136680186/c594eb7c-c340-4650-ab8e-f68034b6992d)

- 결제한 내역 표시
- 환불 신청이 가능하며 결제 완료일 경우 바로 환불 처리, 그 외에는 환불 신청 시 관리자가 환불 처리 후 문구 변경

![그림16](https://github.com/hwangbj123/looklike/assets/136680186/f07add0f-be63-4851-98d5-3f565aa87210)
![그림17](https://github.com/hwangbj123/looklike/assets/136680186/0b3ac55b-7b01-475a-9367-f1c6b3396f0c)

- 배송 완료일 경우 결제 내역 상세 페이지에서 상품 리뷰 작성 가능

### 마이페이지

![그림18](https://github.com/hwangbj123/looklike/assets/136680186/338f8161-9b86-4f10-bdb2-b73b513e1958)
![그림19](https://github.com/hwangbj123/looklike/assets/136680186/b9db3bab-2371-4b9d-97d9-0887e8599e83)

- 장바구니, 관심내역, 결제내역, 문의내역 확인
- 회원 정보 수정 및 탈퇴
- 탈퇴 시 비밀번호 재확인 후 탈퇴
