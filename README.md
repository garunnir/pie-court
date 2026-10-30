# pie-court

**AI 법정으로 협업 지분을 나눈다.**

개인 게임 개발자가 협업을 원해도 지분 나누기는 넘기 힘든 벽입니다. pie-court는 사람끼리 얼굴 붉히며 협상하는 대신, 미리 합의한 규칙에 따라 AI 법정이 기여도를 판정하고 지분을 계산합니다.

## 컨셉

1. **증거 수집**: Git 커밋을 기본 증거로 삼습니다. 줄 수나 커밋 수만 세지 않고, AI가 커밋 내용을 읽어 난이도와 영향을 평가합니다.
2. **재판**: 이의가 제기되면 검사, 변호, 판사 AI 에이전트가 공방한 뒤 판결합니다.
3. **지분 계산**: 판결된 기여를 Slicing Pie 방식의 동적 지분 공식으로 환산합니다.
4. **사람 검증**: 협업자가 AI 판결 일부를 무작위로 검증하고 보정해, AI가 독단으로 정한다는 거부감을 줄입니다.

## 참고한 프로젝트

- [PyDriller](https://github.com/ishepard/pydriller), [git-fame](https://github.com/casperdcl/git-fame): 커밋·diff·소유권 데이터 수집
- [Slicing Pie](https://slicingpie.com): 동적 지분 모델
- [LangGraph](https://github.com/langchain-ai/langgraph): 재판 절차 오케스트레이션
- [ChatEval](https://github.com/thunlp/ChatEval), [Multi-Agents-Debate](https://github.com/Skytliang/Multi-Agents-Debate): 멀티에이전트 토론·판정 설계 (아이디어 참고)
- [Deep Funding](https://github.com/deepfunding/dependency-graph): AI 제안 + 사람 무작위 검증 구조
- [SplitSettl](https://github.com/flip18731/SplitSettl): LLM diff 채점 가중치와 근거 리포트 형식

## 라이선스

MIT
