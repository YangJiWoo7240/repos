# DLIP-2025 Custom Dataset Download Guide

Date: 2025-07-09

Author: Jiwoo-Yang / Chang-Min An

---

## 1. Custom Dataset List

1. **TEAM1_FootballAnalytics_Dataset**
2. **TEAM3_DefectDetectionSystemForMetalNuts_Dataset**
3. **TEAM4_corn_Dataset**
4. **TEAM7_MicroVibration_Dataset**
5. **TEAM8_Eye-Control_Dataset**
6. **TEAM9_AutomaticWasteClassifier_Dataset**
7. **TEAM10_SmartTrash_Dataset**

## 2. Process

#### 0) WI-FI Setting

* HGU-WLAN을 제외한 교내 와이파이 환경에서 실행가능

#### 1) 명령프롬프트 관리자 권한으로 실행

* 명령프롬프트 검색 및 관리자권한 실행

  ![intro](./img/cmd.png)



<img width="722" height="362" alt="" src="https://github.com/user-attachments/assets/d17e322f-b9c3-49e0-aa0b-7f01575bbde1" />



#### 2) 서버 원격 접속

* 아래 코드 실행

  ```bash
  sftp -P 7777 DLIP_DATASET@220.149.109.49:<해당년도>
  ```
  **예시)**

  ```bash
  sftp -P 7777 DLIP_DATASET@220.149.109.49:2025
  ```

  * 처음 실행 때, 아래의 보안키 설정관련 내용이 나옴 > **Yes 타이핑 후 Enter(타이핑 안보임)**

    ```
    The authenticity of host '[220.149.109.49]:7777 ([220.149.109.49]:7777)' can't be established.
    ED25519 key fingerprint is SHA256:TqnafxOy2h1y+zEw13W+ckvH8Md1h/M0STrjRzuSE8k.
    This key is not known by any other names.
    Are you sure you want to continue connecting (yes/no/[fingerprint])?
    Warning: Permanently added '[220.149.109.49]:7777' (ED25519) to the list of known hosts.
    ```

![intro](./img/code_run.png)

* 패스워드 입력**( PW: dlip )** 

  * **패스워드 입력 안보임 > 입력 후 Enter**

![intro](./img/PW.png)

![intro](./img/connect_complet.png)

#### 3) 데이터셋 리스트 확인

* `ls` 명령어를 통해 데이터셋 리스트 확인

![intro](./img/ls.png)

#### 4) 데이터셋 다운로드

* 필요한 데이터셋 다운로드

  ```bash
  get <데이터셋>.zip <로컬PC 폴더경로>
  ```

* 예시

  ```bash
  get TEAM8_Eye-Control_Dataset.zip C:\Users\wldn7\Downloads
  ```

  ![intro](./img/download.png)
  
  ![intro](./img/result.png)

