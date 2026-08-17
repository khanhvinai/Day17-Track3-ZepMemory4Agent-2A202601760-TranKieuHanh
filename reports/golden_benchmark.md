# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1518.2 ms**
- Average token reduction vs full source context: **4.2%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 10.7 | 227 | 0.0% |  |
| G02 | short_term | PASS | 1.1 | 133 | 0.0% |  |
| G06 | long_term | PASS | 2505.8 | 802 | 0.0% |  |
| G09 | semantic | PASS | 424.1 | 418 | 8.9% |  |
| G10 | semantic | PASS | 309.2 | 270 | 41.2% |  |
| G14 | mixed | PASS | 1852.5 | 581 | 0.0% |  |
| G03 | long_term | PASS | 2013.8 | 1415 | 0.0% |  |
| G04 | long_term | PASS | 1980.4 | 1414 | 0.0% |  |
| G07 | episodic | PASS | 437.8 | 387 | 0.0% |  |
| G08 | episodic | PASS | 493.6 | 405 | 0.0% |  |
| G11 | mixed | PASS | 2069.1 | 581 | 0.0% |  |
| G13 | mixed | PASS | 724.2 | 500 | 11.5% |  |
| G15 | mixed | PASS | 2613.9 | 831 | 0.0% |  |
| G16 | mixed | PASS | 2159.8 | 581 | 0.0% |  |
| G17 | mixed | PASS | 2089.6 | 581 | 0.0% |  |
| G18 | mixed | PASS | 861.0 | 500 | 11.5% |  |
| G19 | mixed | PASS | 2664.7 | 581 | 0.0% |  |
| G05 | long_term | PASS | 1940.6 | 1422 | 0.0% |  |
| G12 | mixed | PASS | 3058.7 | 560 | 11.4% |  |
| G20 | mixed | PASS | 2153.2 | 756 | 0.0% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`<USER_SUMMARY> The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend examples and do not use Python for backend examples. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples`

### G09 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, epis`

### G10 - semantic

`EPISODE: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marke`

### G14 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend examples and do not use Python for backend examples. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 09:14:50     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Lan uu tien stack backend nao cho LOTUS-88?   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples.   - Created At: 2026-08-01 11:00:00     Source: m`

### G03 - long_term

`<USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the company proje`

### G04 - long_term

`<USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the company proje`

### G07 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh l`

### G08 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: Toi se uu tien timeline khi giai thich coroutine va Task. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection ch`

### G11 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G13 - mixed

`<EPISODIC> EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: `

### G15 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G18 - mixed

`<EPISODIC> EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: Toi se uu tien timeline khi giai thich coroutine va Task. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout thresho`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G05 - long_term

`<USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the company proje`

### G12 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. They need to complete a benchmark report named LAB-REPORT-1600 before Friday at 16:00. The user is currently debugging async HTTP, specifically connection churn. Increasing the timeout was ineffective, but reusing an aiohttp ClientSession and setting concurrency to 20 resolved the issue for the ASYNC-FIX-20 incident. They have been asked to check the connection pool, client lifecycle, and concurrency.  The user likes Python and dislikes Java. They prefer short examples when code is explained. For the c`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`
