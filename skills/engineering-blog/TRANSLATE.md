# Translating a post

## Rules

- **Map to the concept, not a synonym.** "Their *Shepherd* service" → "a control plane doing leader election and shard assignment", not "their orchestrator".
- **Use the name practitioners would search for**: the term in DDIA, the SRE book, cloud provider docs, well-known papers, or common interview vocabulary.
- **Resolve internal names before guessing.** If the post doesn't define a system, check the company's other posts, talks, or open-source repos via search.
- **Label confidence**: `exact` (clearly the same concept), `close` (same idea, with a difference worth naming), `guess` (thin evidence, say why).
- **Name the difference** on every `close` mapping: "like a write-ahead log, but replicated across regions before acknowledging".
- **Never force-fit.** If no standard concept matches, mark it `novel` and state what is new about it.
- **Translate the numbers too**: put their scale in context ("40k QPS per node is high for a JVM service", "p99 of 200 ms was their SLO, not a hard limit").

## Pattern families

Prompts for recognition, not a complete catalogue. Check each family against the problem and the solution.

| Family | Problem patterns | Solution patterns |
|--------|------------------|-------------------|
| Scaling | hot partition, fan-out explosion, single-writer bottleneck | sharding, consistent hashing, read replicas, fan-out on write vs read |
| Load and traffic | thundering herd, cache stampede, retry storm, noisy neighbour | backpressure, rate limiting, load shedding, jittered backoff, request coalescing |
| Reliability | cascading failure, split brain, single point of failure | circuit breaker, bulkhead, failover, quorum, idempotency keys |
| Data consistency | lost updates, dual writes, stale reads, schema drift | transactional outbox, CDC, saga, event sourcing, expand-contract migration |
| Performance | tail latency, N+1 queries, GC pauses, lock contention | caching layers, batching, hedged requests, denormalisation |
| Data pipelines | late data, backfill pain, reprocessing cost | lambda/kappa architecture, watermarking, idempotent sinks |
| Delivery and operations | risky deploys, config drift, alert fatigue | feature flags, canary releases, GitOps, SLO-based alerting |
| Org and process | ownership gaps, migration stalls | platform teams, paved roads, strangler fig migration |
