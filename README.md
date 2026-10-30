# pie-court

**AI 법정으로 협업 지분을 나눈다.**

개인 게임 개발자가 협업을 원해도 지분 나누기는 넘기 힘든 벽입니다. pie-court는 사람끼리 얼굴 붉히며 협상하는 대신, 팀이 합의한 규칙에 따라 AI 법정이 기여도를 판정하고 지분을 계산하는 웹 앱입니다.

## 컨셉

목표는 고정된 "정답"이 아닙니다. 기여를 보는 기준은 유동적이므로, 그 기준을 붙잡아 **팀의 다수가 납득할 절충안**을 만드는 것이 목표입니다. 기여가 인정받고 눈에 보이게 해 **기여자들의 열의를 끌어올리는 것**도 함께 노리는 목표입니다.

1. **품질 기여가 기준**: 투입 시간이 아니라 **최종 결과물 품질에 얼마나 기여했는지**를 평가합니다. 시간은 점수에서 제외합니다.
2. **증거**: Git 커밋이 기본 증거입니다. 줄 수나 커밋 수가 아니라 AI가 커밋 내용(diff)을 읽고 평가하고, 커밋별 활동 요약을 남겨 재평가의 근거로 씁니다.
3. **정기 실시간 재판**: 기본 2주에 한 번(주기는 다수결로 변경 가능), 브라우저의 법정 화면에 모든 당사자가 동시에 접속해 직접 주장하거나 AI 변호인의 도움을 받고, AI 판사가 판결합니다. 판결 뒤에는 짧은 이의 제기 기간이 있습니다.
4. **입법**: 판정 기준은 팀의 "법"이며 제안과 투표로 개정합니다. 법은 기계적 공식이 아니라 **기준**이어서, 진짜 법정처럼 그 기준에 근거한 주장과 반박에 따라 판결이 유연하게 달라집니다. 법이 바뀌면 결과론적으로 과거 기여 전체를 다시 평가·재계산합니다.
5. **지분 원장**: 판결이 누적되며 지분이 재계산되고, 재계산 이력은 스냅샷으로 남습니다. Slicing Pie에서는 이 원장 아이디어만 빌리고, 시간·금액 시장가치 공식은 쓰지 않습니다.

자세한 설계: **[docs/DESIGN.md](docs/DESIGN.md)**

## 참고한 프로젝트

- [PyDriller](https://github.com/ishepard/pydriller), [git-fame](https://github.com/casperdcl/git-fame): 커밋·diff·소유권 데이터 수집
- [Slicing Pie](https://slicingpie.com): 누적·재계산 지분 원장 아이디어만 차용 (시간·금액 공식은 미사용)
- [LangGraph](https://github.com/langchain-ai/langgraph): 재판 절차 오케스트레이션
- [ChatEval](https://github.com/thunlp/ChatEval), [Multi-Agents-Debate](https://github.com/Skytliang/Multi-Agents-Debate): 멀티에이전트 토론·판정 설계 (아이디어 참고)
- [Deep Funding](https://github.com/deepfunding/dependency-graph): AI 제안 + 사람 무작위 검증 구조
- [SplitSettl](https://github.com/flip18731/SplitSettl): LLM diff 채점 가중치와 근거 리포트 형식

## 라이선스

MIT
