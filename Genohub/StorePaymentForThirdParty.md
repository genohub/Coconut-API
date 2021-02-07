# GHD 결제 내역 저장

- API : https://n3x65ok2dd.execute-api.us-east-2.amazonaws.com/StorePaymentForThirdParty (POST)


- Request

Phone, Email 전부 사용하는 경우 : { "Email": "rlackstjdsla@naver.com", "PhoneNumber" : "821041139274", "Caller" : "Genohub", "GHDUsage" : "1", "GHDBalance" : "100", "StoreInfo" : "Familymart", "Timestamp" : "1590934319" }

Phone만 사용하는 경우 : { "PhoneNumber" : "821041139274", "Caller" : "Genohub", "GHDUsage" : "1", "GHDBalance" : "100", "StoreInfo" : "Familymart", "Timestamp" : "1590934319" }

Email만 사용하는 경우 : { "Email": "rlackstjdsla@naver.com", "Caller" : "Genohub", "GHDUsage" : "1", "GHDBalance" : "100", "StoreInfo" : "Familymart", "Timestamp" : "1590934319" }

  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  PhoneNumber | Genohub 회원 휴대폰번호 | String/필수
  Email | Genohub 회원 이메일 | String/필수
  Caller | Caller Service | String/필수
  GHDUsage | GHD 사용량 | String/필수
  StoreInfo | 가맹점 정보 | String/필수
  Timestamp | 결제일시  | String/필수
    
- Response Success

  * Sample : 
  {
      "status": 3000,
      "response": "OK"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 
