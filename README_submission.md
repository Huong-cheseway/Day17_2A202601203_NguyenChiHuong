# Lab 17 — Submission

## Kết quả và phân tích

Trong bộ test này, **long-term memory** quan trọng nhất vì bao phủ bốn case E02, E03, E08, E09 và còn tham gia E07. Nó duy trì preference, open loop, cập nhật theo scope và user isolation qua nhiều session. Benchmark student đạt **11/11 (100%)**; vì vậy không có layer nào có hit rate thấp nhất riêng lẻ — tất cả cùng đạt 100%. E08 retrieve nhiều nhất với **802 token**.

E07 phải kết hợp long-term và semantic: long-term cung cấp preference **Python** của Minh, còn semantic cung cấp quy tắc **Idempotency-Key**. Memory-enabled giảm trung bình **20,8%** token so với full source nhưng vẫn đạt 100%. No-memory giảm tới **81,8%** vì gần như không retrieve gì, song chỉ đạt 2/11; do đó token reduction chỉ có ý nghĩa khi đi cùng evidence hit rate.

Ở E08, recency không đơn giản ghi đè mọi preference: **BLUEBIRD-42** dùng TypeScript/NestJS, còn Python vẫn hợp lệ cho ORCHID-27. Scope, timestamp và provenance giúp giải quyết conflict đúng ngữ cảnh. Ở E10, sliding window đã loại raw turn cũ nhưng durable note vẫn giữ `REVIEW-DEADLINE-1600`, Friday và 16:00. Buffer không đủ bền vì token tăng tuyến tính; compaction cần ưu tiên constraint, state, decision và TODO.

## Trade-off và guardrail

Zep Context Block cung cấp cross-session context, graph search, provenance và xử lý relevance dưới dạng managed service, đổi lại có network latency, chi phí và ít quyền kiểm soát hạ tầng hơn. Redis + Qdrant cho quyền kiểm soát dữ liệu và vận hành local, nhưng nhóm phát triển phải tự xây ingestion, embedding, recency/conflict resolution, user isolation và deletion verification.

Để chống memory poisoning, hệ thống phải yêu cầu opt-in, giảm PII, tách namespace theo `user_id`, lưu source/timestamp/provenance và không biến nội dung retrieve thành instruction có quyền cao hơn. Fact mâu thuẫn cần validation và recency theo scope; dữ liệu nhạy cảm phải hỗ trợ forget rồi verify trên mọi user-scoped store.
