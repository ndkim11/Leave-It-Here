# 만들어야 할 것들
## Web (Dictor)
NFC 태그 관리, 기기 원격 관리, 반납 현황 관리, 일일 병력 현황 또는 생활관 명단 관리

### 프론트엔드
- 태그 관리 : CRUD, 해당 태그의 사용자 정보로 생활관 명단으로 Jump 가능하게
- 기기 관리 : CRUD, 실시간 기기정보 가져오기, 기기에 반납된 태그 목록
- 반납 기록 관리 : 반납 기록을 태그, 기기 별로 필터링하여 볼 수 있게
- 병력 관리 : 생활관 별로 병력 명단 CRUD

### 백앤드
- 관리해야할 Model : NFC 태그 (반납 상태, 부착된 기기 정보, 사용자 정보, 고유 번호, 인증서), 기기 (기기 상태, 연결 상태), 반납 기록, 생활관 명단 (사용자 정보와 연동)
- 프론트를 위한 엔드포인트 노출
- 기기를 위한 엔드포인트 노출 (인증서등을 통한 자격 증명 방안 필요)

###
## IoT (ndkim11)
휴대폰 불출/반납 상태 송신, 반납함 모델링, 휴대폰 정상반납 여부확인

### 기기 하드웨어 제작
- 반납함 외함 제작: Tinkercad 모델링 - NFC 리더, 전면에 손잡이 달린 문, 뒷면에 프로세서와 통신기 보관함
- 반납함 내부 회로: NFC 리더, Wifi 모듈, FSR, 개폐센서

## 기기 소프트웨어 제작
- 웹과 통신: 와이파이 모듈 통해 명령 수신, 결과 반환
- 태그 인식: 해당 사용자의 ID 파악, 상태 갱신으로 이동
- 상태 갱신: 태그, 반납 확인 명령에 따른 반납함 상태확인, 갱신
- 정상 반납 판단: 각 기기 무게 체계와 비교, 미반납 여부 확인
