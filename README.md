# Hi, I'm Xavier

I build AI applications, backend services, and local-first tools.

[Contact](mailto:xavierzhou923@gmail.com) · [PicSpeak live](https://www.picspeak.art/en)

## Featured projects

### PicSpeak

AI photography critique with practical retake guidance and side-by-side progress comparisons.

- FastAPI handles asynchronous critique and image-generation tasks, with WebSocket status updates.
- PostgreSQL persists reviews and task state; S3-compatible storage holds images.

[Live product](https://www.picspeak.art/en) · [Source](https://github.com/AsaZhou923/picspeak)

### SeaweedFS Console

An independent, third-party console for SeaweedFS cluster management and image asset workflows.

- Persistent background jobs run through a standalone worker and SQLite WAL.
- Guarded writes use durable intents, stable idempotency keys, and readback verification.

[Source](https://github.com/AsaZhou923/seaweedfs-console)

### MeetingRelay

Local-first Windows meeting transcription with on-device speech recognition and optional translation.

- Transcript segments are marked saved only after a successful SQLite commit.
- Translation runs independently, so provider failures cannot overwrite or delay the original transcript.

[Source](https://github.com/AsaZhou923/MeetingRelay) · [Latest release](https://github.com/AsaZhou923/MeetingRelay/releases/latest)

## Other projects

- [TokSync](https://github.com/AsaZhou923/toksync): Metrics-only AI coding usage sync, local reports, and opt-in public sharing.
- [PromptCrate](https://github.com/AsaZhou923/PromptCrate): Local-first browser extension that inserts reusable prompt templates with variables at the cursor.
- [Dual Agent System](https://github.com/AsaZhou923/dual-agent-system): Version-pinned Windows-to-Mac agent orchestration with explicit contracts and policy boundaries. Cross-machine runtime validation is still pending.

## Stack in these projects

- **Python / FastAPI** for PicSpeak and SeaweedFS Console backends; **TypeScript / Next.js** for PicSpeak's web app.
- **Rust / Tauri** for MeetingRelay; **PostgreSQL, SQLite, and S3-compatible storage** for application data, local state, and images.

## Open source contributions

Selected contributions merged into other projects:

- **Concurrent device authentication** · [tokscale #546](https://github.com/junhoyeo/tokscale/pull/546)<br>
  Prevented duplicate token issuance by locking the device-code row and issuing the token in one database transaction.
- **Correct filtered leaderboards** · [tokscale #1390](https://github.com/junhoyeo/tokscale/pull/1390)<br>
  Aggregated matching usage in PostgreSQL instead of lifetime totals, with a bounded scoped cache and database regression tests.
- **Partial cache updates** · [cpa-usage-keeper #593](https://github.com/Willxup/cpa-usage-keeper/pull/593)<br>
  Preserved separate Claude usage windows when partial headers arrive out of order, with per-window timestamps and regression coverage checked under Go's race detector.

Also merged: [OpenAI Fast pricing](https://github.com/junhoyeo/tokscale/pull/1391) in tokscale; [legacy Discord configuration](https://github.com/ZhuLinsen/daily_stock_analysis/pull/659) and [current-filter alert refreshes](https://github.com/ZhuLinsen/daily_stock_analysis/pull/2378) in daily_stock_analysis.

<details>
<summary>AI coding tool usage</summary>

[![AI coding tool usage tracked by Tokscale](https://tokscale.ai/api/embed/AsaZhou923/svg?theme=light&template=graph&rank=percent&tokens=full&cost=full)](https://tokscale.ai/u/AsaZhou923)

</details>
