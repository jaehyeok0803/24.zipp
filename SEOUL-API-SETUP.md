# 24zip 서울시 복지서비스 API 연결

## Vercel 환경변수

- `SEOUL_API_KEY`: 서울 열린데이터광장에서 발급받은 인증키 (필수)
- `SEOUL_RENT_SERVICE_NAME`: `welfareServiceList` (선택; 기본값이 이미 `welfareServiceList`)

Vercel Settings → Environment Variables에서 저장하고 Deployments에서 Redeploy하세요.

## 작동 방식

`/api/seoul-rent-support`가 서울 열린데이터광장 `welfareServiceList`의 첫 100개 행을 요청하고, 주거 관련 키워드가 포함된 항목을 보여줍니다. 기존 웹사이트의 입력 보증금/월세를 표시하며, 별도 입력한 나이/소득/무주택 여부는 아직 자동 자격 판정에 사용하지 않습니다.

**중요:** 전체 목록 검색, 서비스 상세조회 연계, 정책별 수치 조건 판정 및 AI API 연동은 구현되지 않았습니다. 검색 결과가 0건이어도 지원사업이 없다는 의미가 아닙니다. 실제 API 응답 스키마 및 정상 작동 여부는 인증키로 배포 후 확인해야 합니다.

공식 자료: https://data.seoul.go.kr/dataList/OA-23013/S/1/datasetView.do
