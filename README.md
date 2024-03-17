## 🎮 Capstone Design 2020 🎮

**\- Team Members :** 팀 Edu-Unit [구자빈, 맹현영, 박세은, 손민국, 안형모]

**\- Title :** Unity를 이용한 VR 교육용 프로그램 : Ver. COVID-19

**\- 개발 툴 :** Unity 3D 

**\- 스토리 :** VR로 진행되며, 상황에 맞게 주어진 문제를 모두 해결하면 바이러스에 감염되지 않고 탈출하는 게임

**\- 게임 구성 :**

|<img width="300" alt="코로나" src="https://user-images.githubusercontent.com/101172040/228178696-059a5b8a-2c64-43db-92f3-317f9864954f.png">|<img width="304" alt="교회" src="https://user-images.githubusercontent.com/101172040/228178677-0e8a4139-708b-4918-b22b-688f35a4c6b7.png">|<img width="304" alt="UMA" src="https://user-images.githubusercontent.com/101172040/228178715-ba13df48-f556-4317-a510-97c53f751671.png">|
|:----:|:----:|:-----:|
|#시작 Scene|#퀴즈 장면 Scene|#UMA 활용|
게임 설명+흥미 유발|각 장소에서 5개의 퀴즈 해결,</br>오답 시 생명(하트) 감소|사람을 표현할 수 있는 기술|

## 주요 구현 기능

1. GoogleVR Prefabs를 이용한 시선 조절

<img width="331" alt="스크린샷1" src="https://user-images.githubusercontent.com/101172040/228178732-d1cccd12-4f9e-4e6a-8ed2-479116d2776f.png">

2. 텍스트를 부드럽게 나오게 하는 간단한 API 활용

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img width="299" alt="스크린샷2" src="https://user-images.githubusercontent.com/101172040/228178750-6235d130-0c4c-4607-a263-ae283cbacc6e.png">

3. Object 상호작용 발생 코드
<details>
  <summary>코드</summary>
  
  
  ```cs
  time += Time.deltaTime;           
  RaycastHit hit;               
  Vector3 forward = mainCam.transform.TransformDirection(Vector3.forward);              
  Debug.DrawRay(this. transform.position, forward*100, Color.green);              
  CursorGaugeImage. fillAmount = GaugeTimer;
  ```
  
  
  </details>
4. 퀴즈 Object 유->뮤 제어 코드
<details>
  <summary>코드</summary>
  
  ```cs
  if (GaugeTimer >= 1.0f && (hit. transform. tag. Equals( "ok5" )))
  {
  ok5.gameObject .SetActive( false) ;
  StartCoroutine(wait50))
  HpManager3.hp -= 1;
  }
  lEnumerator wait5()
  {
  yield return new WaitFor Seconds(4.0f); quiz5.gameObject. SetActive(false) ;
  ```

  </details>
  
## 프로젝트 목적

\- Unity를 이용한 VR 교육용 프로그램 개발        
\- 코로나 바이러스에 대한 정보와 예방수칙 전파 및 코로나 바이러스의 확산 방지         

## 활용방안/기대효과

1. 많은 사람들 중에서도 미취학 아동과 청소년들을 타겟       
2. 단순 주입식 교육보다 직접 보고 체험하는 것으로서 좀 더 효과적        
3. 학교나 공공기관에서 교육용으로 많이 활용 가능
4. 코로나 바이러스에 대한 경각심을 심어 주고, 확산 방지에 기여 할 수 있을 것
5. 이후에 또 다른 감염 위험이 있는 바이러스가 생겨났을 때에도 동일한 효과를 발휘할 것
