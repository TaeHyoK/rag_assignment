# RAG Assignment

LangChain을 사용한 RAG(Retrieval-Augmented Generation) 시스템 구현 과제입니다.

## 프로젝트 구조

- `rag_assignment.ipynb`: RAG 시스템 기본 구현
- `rag_v2.ipynb`: 개선된 RAG 시스템 (3개 LLM 비교 분석 포함)
- `pdf/`: 학습 문서 저장 디렉토리

## 주요 기능

- PDF 문서 로딩 및 전처리
- OpenAI Embeddings를 사용한 벡터화
- Chroma 벡터 데이터베이스
- 3개 LLM 모델 비교 (GPT-3.5-turbo, GPT-4o-mini, Gemini-2.0-flash)

## 설치 방법

```bash
pip install langchain_community tiktoken langchain-openai langchainhub chromadb langchain langchain-cohere langchain-upstage langchain-google-genai langchain-huggingface pypdf python-dotenv pypdfium2
```

## 환경 변수 설정

`.env` 파일을 생성하고 다음 키를 설정하세요:

```
OPENAI_API_KEY=your_openai_api_key
GOOGLE_API_KEY=your_google_api_key
LANGCHAIN_API_KEY=your_langchain_api_key
```

## 사용 방법

1. PDF 파일을 `pdf/` 디렉토리에 배치
2. Jupyter Notebook 실행
3. 셀을 순서대로 실행

## 문제 해결

### 출력이 두 번씩 나오는 경우
- Kernel > Restart Kernel 실행
- 모든 셀을 처음부터 순서대로 다시 실행

### PDF 로딩 오류 (unhashable type)
- 메타데이터 처리 코드가 자동으로 처리합니다
- 실패한 파일은 대체 로더로 재시도됩니다
