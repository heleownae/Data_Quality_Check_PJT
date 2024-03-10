# ⌛ 이커머스 데이터 품질 검사

이커머스 데이터 품질을 검사하고,

태블로 대시보드를 제작하여 이상치를 지속 트래킹합니다 🚨

</br>

## 👩🏻‍💻 팀원

<table>
  <tbody>
    <tr>
      <td align="center"><a href="https://github.com/"><img src="https://avatars.githubusercontent.com/u/157770169?v=4" width="100px;" alt="박나영"/><br /><sub><b>박나영</b></sub></a><br /></td>
      <td align="center"><a href="https://github.com/ssoheeL"><img src="https://avatars.githubusercontent.com/u/157769708?v=4" width="100px;" alt="이소희"/><br /><sub><b>이소희</b></sub></a><br /></td>
      <td align="center"><a href="https://github.com/gabrietofu"><img src="https://avatars.githubusercontent.com/u/157769636?v=4" width="100px;" alt="이정희"/><br /><sub><b>이정희 (팀장)</b></sub></a><br /></td>
      <td align="center"><a href="https://github.com/heleownae"><img src="https://avatars.githubusercontent.com/u/152258170?v=4" width="100px;" alt="이해원"/><br /><sub><b>이해원</b></sub></a><br /></td>
    </tr>
  </tbody>
</table>

</br>

## 📊 분석 내용

### 1. event 테이블 데이터 품질 검사

- unique user가 2명 이상인 세션

- city가 2개 이상인 유저 수

- 일별 user id가 없는 이벤트 수
  - 🚨 이상치 발견: 500~700건 사이의 일관적 값, 엔지니어링 단계의 오류로 판단

- 위 세 항목 월별 집계

</br>

![Dashboard1](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/53603b73-f216-47e5-892e-270459cf3ae2)
![Dashboard2_EDA](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/3853cbc1-7dea-4089-ae60-8a02782febfd)

</br>

### 2. event & order items 테이블 데이터 품질 검사

- event가 발생하지 않은 유저-상품 쌍 여부

- 구매 시각과 event 발생 시각 비교

- 30분 경과로 인한 session 종료 여부와 원인 파악
  - 🚨 이상치 발견: 전체 데이터의 11%가 세션 종료 존재하며, event type이 purchase인 경우에만 발생

</br>

![Dashboard3_sessionover30m](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/d7358419-a42a-4b48-88fd-d4bcb7a00dbb)

</br>

### 3. 세션 종료 원인 분석 & 액션 플랜
![over30m1](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/c0b40312-a396-44e1-a109-ad56e383f287)
![over30m2](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/5611b1bd-b4ff-4e7e-a9f5-a8218f8714da)
![over30m3](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/bcd5bed1-e0cc-49d9-8387-54ef442bf1ad)
![over30m4](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/a87aa33a-9fe7-4a64-a3c8-0668d96028ed)
![over30m5](https://github.com/gabrietofu/B01_Data_Quality_Check/assets/152258170/b39c1ae7-a649-4bd2-879e-ad7ecb0f6495)

</br>

