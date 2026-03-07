# ALICE-DevOps

Container orchestration with DNS, CDN, queue, and observability

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-container, alice-dns, alice-cdn, alice-queue, alice-semantic-telemetry

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/deploy` | コンテナデプロイ |
| `POST` | `/api/v1/scale` | オートスケール設定 |
| `GET ` | `/api/v1/services` | サービス一覧・ステータス |
| `GET ` | `/api/v1/observability` | オブザーバビリティダッシュボード |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
