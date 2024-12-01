# 📝 AI 모델을 활용한 회의 지원 솔루션 서비스 (Clerker - AI Team)
<img src="Picture Folder/Clerker_image.png" alt="Clerker" width="900"/>

## 🔍 프로젝트 소개  
- AI 모델을 활용한 회의 지원 솔루션 서비스 **Clerker**는 음성 및 화상 회의 내용을 자동으로 요약하여 직관적이고 효율적인 보고서를 생성하는 혁신적인 서비스입니다.  
  - Clerker 플랫폼 내에서 온라인 회의 (Google Meet)를 생성하면 화면 녹화 기능을 통해 해당 회의를 녹화합니다.
  - 녹화된 회의 영상을 바탕으로 회의록을 텍스트 및 다이어그램으로 요약합니다.
  - 회의만 해도 자동으로 보고서가 도출되는 편리한 서비스를 경험해보세요.


## 🤖 모델 관련  
STT, Diagram Recommendation / Generation, Keyword Extraction, Summarization, Chunking 등의 AI 기술을 통해, 회의 요약 보고서와 추천 다이어그램을 구현했습니다.

- **STT 모델**  
  - Naver Clova API (CSR) 활용
  - 도메인 맞춤형 키워드 사전 제작
  - STT의 품질을 높이기 위해 주파수 필터링, 속도 조절, Noise Reduction, 정규화 등의 전처리 과정 수행

- **청크 모델**
  - LangChain의 Semantic Chunking과 Recursive Chunking 알고리즘을 사용
  - 화자분리된 텍스트 파일을 주제에 맞게 적절한 청크로 분리
  - 키워드 추출 및 시각화 데이터 자동 생성
 
- **요약 모델**  
  - LLM을 활용하여 다이어그램 생성을 위한 청크별 요약 파일 생성
  - 보고서 생성을 위한 청크별 제목, 주요 키워드, 요약 3문장으로 정리

- **다이어그램 생성**  
  - LLM을 통해 각 청크의 다이어그램화 여부를 결정
  - 각 요약에 대한 다이어그램 종류 추천
  - Mermaid Code 기반 다이어그램 생성


## 🎯 주요 성과  
- 회의 요약 보고서

- 요약 다이어그램 (프로젝트 로직)
<img src="Picture Folder/Diagram_example.png" alt="Clerker" width="900"/>


## 🚀 향후 계획  
- **실시간 회의 요약**  
  - 실시간 텍스트 변환 및 요약 기능 추가  
- **시각화 도구 강화**  
  - 더욱 정교한 다이어그램 및 데이터 시각화 기능 제공  
- **모바일 앱 개발**  
  - 모바일 환경에서도 회의 요약 서비스 사용 가능  


## 📚 참조  
- **참고 논문**: [llama](https://arxiv.org/abs/2302.13971)
