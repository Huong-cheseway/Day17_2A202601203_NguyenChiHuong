# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1261.8 ms**
- Average token reduction vs full source context: **6.3%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.3 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G08 | long_term | PASS | 1718.2 | 852 | 0.0% |  |
| G09 | long_term | PASS | 1930.3 | 1665 | 0.0% |  |
| G12 | semantic | PASS | 1059.8 | 418 | 8.9% |  |
| G14 | semantic | PASS | 274.6 | 270 | 30.2% |  |
| G15 | semantic | PASS | 569.0 | 270 | 41.2% |  |
| G19 | mixed | PASS | 1832.4 | 581 | 0.0% |  |
| G03 | long_term | PASS | 2153.8 | 1668 | 0.0% |  |
| G04 | long_term | PASS | 1794.1 | 1657 | 0.0% |  |
| G05 | long_term | PASS | 1726.3 | 1655 | 0.0% |  |
| G10 | episodic | PASS | 566.1 | 1327 | 0.0% |  |
| G11 | episodic | PASS | 380.2 | 1330 | 0.0% |  |
| G13 | semantic | PASS | 269.4 | 416 | 26.4% |  |
| G16 | mixed | PASS | 2215.1 | 581 | 0.0% |  |
| G18 | mixed | PASS | 570.1 | 500 | 11.5% |  |
| G20 | mixed | PASS | 2471.5 | 831 | 0.0% |  |
| G06 | long_term | PASS | 1571.0 | 1663 | 0.0% |  |
| G07 | long_term | PASS | 2019.3 | 1651 | 0.0% |  |
| G17 | mixed | PASS | 2114.9 | 581 | 8.1% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G08 - long_term

`<USER_SUMMARY> Lan's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python in that capacity.  Lan prefers to use Java and Spring Boot for backend development, and explicitly avoids using Python for backend tasks. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 05:28:39     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Minh la Lan, minh dang muon them retry cho phan goi payment trong san pham cua minh va minh muon vi du code hop voi dung stack ma minh dang dung ch`

### G09 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G12 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal `

### G14 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G15 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> Lan's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python in that capacity.  Lan prefers to use Java and Spring Boot for backend development, and explicitly avoids using Python for backend tasks. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 1`

### G03 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G04 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G05 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G10 - episodic

`EPISODE: Minh con open loop hay deadline nao chua hoan thanh? EPISODE: Toi se uu tien timeline khi giai thich coroutine va Task. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay chon huong dan code retry payment phu hop voi preference ca nhan cua Minh. EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPIS`

### G11 - episodic

`EPISODE: Voi demo ca nhan cua Minh, ngon ngu uu tien la gi? EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay chon huong dan code retry payment phu hop voi preference ca nhan cua Minh. EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang t`

### G13 - semantic

`EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data witho`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tas`

### G18 - mixed

`<EPISODIC> EPISODE: Backend cua BLUEBIRD-42 bat buoc dung stack gi? EPISODE: Voi demo ca nhan cua Minh, ngon ngu uu tien la gi? EPISODE: Toi se uu tien timeline khi giai thich coroutine va Task. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay chon huong dan code retry payment phu hop voi preference ca nhan cua Minh. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: Da ghi nhan traject`

### G20 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tas`

### G06 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G07 - long_term

`<USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tasks. </USER_S`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh's personal project is ORCHID-27, for which they prefer Python. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used.  Minh prefers Python and dislikes Java. For company projects like BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python should not be used for this specific project. Minh still prefers Python for personal demos, such as with ORCHID-27.  When explaining code, use short examples, prioritizing Python and avoiding Java. When explaining async/await and coroutines versus Tasks, use a timeline format. The AI assistant will prioritize timelines when explaining coroutines and Tas`
