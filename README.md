# 🎙️ 실시간 음성 인식 웹 애플리케이션 (Flask + Whisper)

이 프로젝트는 **Flask 웹 프레임워크**와 **OpenAI의 Whisper 모델**을 이용하여, 사용자의 마이크 입력을 실시간으로 받아 음성을 텍스트로 변환해주는 **웹 애플리케이션**입니다.  
WebSocket 기반 통신을 통해 **지연 없이 텍스트 결과를 화면에 출력**하며, Colab에서도 테스트 가능하도록 **Ngrok 연동**을 제공합니다.

---

## 📷 데모 화면

<img width="1193" alt="image" src="https://github.com/user-attachments/assets/7cc358e2-ab85-447e-a845-f23b9bda41b8" />


---

## 🚀 실행 방법

### 1. 로컬 환경에서 실행
```bash
# 패키지 설치
pip install flask flask-cors flask-sock openai-whisper pyngrok soundfile

# 서버 실행
python app.py
```

### 2. 구글 코랩에서 실행
```bash
# Ngrok 토큰 등록
!ngrok authtoken <your_token>

# run_server.py 실행
!python run_server.py
```


---
## 💡 핵심 기능
### 🎤 브라우저 마이크 접근 및 오디오 스트림 수집 (JavaScript)

### 🌐 WebSocket 통신으로 Flask 서버에 실시간 오디오 전송

### 🤖 Whisper Turbo 모델로 .wav 음성 인식

### 📝 텍스트 결과를 실시간 화면 출력

### 🔄 Ngrok을 통한 외부 테스트 지원



---
## 🧩 기술 스택
| 영역     | 사용 기술                                               |
| ------ | --------------------------------------------------- |
| 백엔드    | Python, Flask, flask-sock (WebSocket), pyngrok      |
| 음성 인식  | OpenAI Whisper (Turbo 모델)                           |
| 프론트엔드  | HTML, JavaScript (MediaRecorder API, WebSocket API) |
| 오디오 처리 | soundfile, io.BytesIO                               |
| 테스트 환경 | Google Colab, Ngrok                                 |



---
## 📁 디렉토리 구조
```bash
├── app.py                  # Flask 서버 (WebSocket + Whisper)
├── run_server.py           # Colab용 서버 자동 실행 스크립트
├── www/
│   └── index.html          # 프론트엔드 UI (HTML + JS)
    └── styles.css
    └── app.js  
```



---
## 🛠 향후 개선 방향
### 스트리밍 방식으로 Whisper 처리 최적화
### 음성 언어 자동 감지 기능 추가
### 인식 결과 저장 및 다운로드 기능
### 사용자 UI 개선 (Dark Mode, 반응형 디자인 등)


---
## 🧑‍💻 개발자
### 👤 최기영
### 고급 웹 프로그래밍 과제 프로젝트
