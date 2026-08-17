# Lab 17 – Submission

## Trả lời câu hỏi

Trong bộ test này, long-term memory là lớp quan trọng nhất vì E02, E03, E08 và E09 đều yêu cầu nhớ preference, open loop, cập nhật recency và tách namespace theo user. E07 cũng cần long-term để lấy preference Python của Minh trước khi kết hợp với hướng dẫn retry.

Zep cung cấp Context Block, user graph, thread và provenance đã được quản lý sẵn nên phù hợp cho cross-session memory. Redis/Qdrant local cho phép tự kiểm soát hạ tầng và dễ thử nghiệm, nhưng phải tự xây ingestion, ranking, namespace, freshness và deletion; vì vậy chi phí vận hành và rủi ro rò rỉ dữ liệu cao hơn.

Guardrail chống memory poisoning gồm: chỉ ghi memory khi user đã consent, giảm thiểu PII trước ingestion, giới hạn loại dữ liệu được ghi, lưu provenance/source, tách `user_id`, ưu tiên fact mới nhưng giữ lịch sử conflict, và không cho heartbeat tự thêm quyền hay instruction mới vào durable memory.

## Phân tích benchmark

Sau khi chạy benchmark, layer có hit rate thấp nhất và case retrieve nhiều token nhất được ghi trong `reports/benchmark.md`. E07 cần kết hợp long-term memory để lấy preference Python và semantic memory để lấy marker `Idempotency-Key`. Token reduction đo lượng context đã giảm so với full source context; no-memory đôi khi giảm nhiều token vì gần như không trả evidence, nhưng hit rate thấp vì thiếu thông tin cần thiết.

E08 minh họa recency và scope: TypeScript/NestJS là preference mới cho BLUEBIRD-42, còn Python vẫn đúng cho ORCHID-27. E10 minh họa compaction: durable note giữ constraint `REVIEW-DEADLINE-1600`, `Friday` và `16:00` dù các filler turns đã bị loại khỏi recent window.
