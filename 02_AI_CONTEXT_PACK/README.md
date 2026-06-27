# AI Context Pack

## Pack Identity

- Upstream: https://github.com/milvus-io/milvus
- Pack type: Vector Database Context Pack
- Doramagic canonical: https://doramagic.ai/en/projects/milvus/
- Relationship: independent pack; not affiliated or endorsed unless explicitly stated.

## Operating Rules

- Evidence first.
- No official endorsement claim.
- Run evals before claiming success.
- Use pitfall and risk files for recovery.

## Host Files

- `../AGENTS.md`
- `../CLAUDE.md`

## Doramagic Source Extract

# milvus - Doramagic AI Context Pack

> Purpose: pre-work context for the user's host AI. This pack does not prove that the project has been installed, run, or validated.

## Project

- canonical_name: `milvus-io/milvus`
- capability: Milvus is a high-performance, cloud-native vector database built for scalable vector ANN search
- expected_user_outcome: Milvus is a high-performance, cloud-native vector database built for scalable vector ANN search

## Operating Boundaries

- Do not claim that the project has been installed, run, called through an API, or used on local files unless separate evidence proves it.
- Project facts must come from repo evidence, Claim Graph, or explicit source references.
- When a capability is not verified, mark it as unverified instead of completing it as fact.
- publish_status: `publishable`
- blocking_gaps: none

---

## Doramagic Context Augmentation

The following sections strengthen the repository context for a host AI. Human Manual data is a reading route, and pitfall notes become operating constraints.

## Human Manual Outline

Usage rule: this is only a reading route and salience signal, not factual authority. Concrete claims must still return to repo evidence or Claim Graph.

Host AI hard rules:
- Do not treat page titles, section order, summaries, or importance values as factual project evidence.
- When explaining the Human Manual outline, state that it is only a reading route or salience signal.
- Capability, installation, compatibility, runtime state, and risk claims must cite repo evidence, source paths, or Claim Graph.

- **Milvus Overview and Distributed Architecture**: importance `high`
  - source_paths: README.md, cmd/main.go, cmd/components/proxy.go, cmd/components/query_node.go, cmd/components/data_node.go
- **Data Management, Storage Engine, and Indexing**: importance `high`
  - source_paths: internal/core/src/segcore/ChunkedSegmentSealedImpl.cpp, internal/core/src/segcore/SegmentGrowingImpl.cpp, internal/core/src/storage/DataCodec.cpp, internal/storagev2/packed/packed_writer.go, internal/storagev2/packed/manifest_commit.go
- **Query, Search Execution, and Streaming**: importance `high`
  - source_paths: internal/core/src/query/PlanNode.cpp, internal/core/src/exec/expression/Expr.cpp, internal/core/src/exec/operator/VectorSearchNode.cpp, internal/core/src/exec/operator/SearchGroupByNode.cpp, internal/core/src/exec/operator/QueryOrderByNode.cpp
- **Client SDKs, Deployment, and Common Operational Issues**: importance `high`
  - source_paths: client/milvusclient/client.go, client/milvusclient/client_config.go, client/entity/schema.go, client/entity/field.go, client/index/ann_param.go

## Repo Inspection Evidence

- repo_clone_verified: true
- repo_inspection_verified: true
- repo_commit: `eab9690fa56822eb85ef795063cc3d15572efd60`
- inspected_files: `README.md`, `docker-compose.yml`, `docs/jaeger_guides/opentracing_user_guide.md`, `docs/user_guides/tls_proxy.md`, `docs/user_guides/snapshot_user_guide.md`, `docs/user_guides/external_table.md`, `docs/user_guides/collection_ttl.md`, `docs/user_guides/clustering_compaction.md`, `docs/developer_guides/appendix_b_api_reference.md`, `docs/developer_guides/chap01_system_overview.md`, `docs/developer_guides/developer_guides.md`, `docs/developer_guides/chap08_binlog.md`, `docs/developer_guides/how_to_develop_with_local_milvus_proto.md`, `docs/developer_guides/chap06_root_coordinator.md`, `docs/developer_guides/appendix_a_basic_components.md`, `docs/developer_guides/chap05_proxy.md`, `docs/developer_guides/chap03_index_service.md`, `docs/developer_guides/appendix_d_error_code.md`, `docs/developer_guides/chap09_data_coord.md`, `docs/developer_guides/chap07_query_coordinator.md`

Host AI hard rules:
- Without repo_clone_verified=true, do not claim that the source code has been read.
- Without repo_inspection_verified=true, do not write README, docs, or package-file conclusions as facts.
- Without quick_start_verified=true, do not claim that the Quick Start path has run successfully.

## Doramagic Pitfall Constraints

These rules come from Doramagic discovery, validation, or compilation findings. The host AI must treat them as operating constraints, not background notes.

### Constraint 1: Installation risk requires verification

- Trigger: Project evidence flags a installation risk. Review the linked source before relying on this workflow.
- Host AI rule: Reproduce the official install and quickstart path in an isolated environment.
- Why it matters: May increase setup, validation, or first-run risk for the user.
- Evidence: community_evidence:github | https://github.com/milvus-io/milvus/issues/50333
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 2: Installation risk requires verification

- Trigger: Developers should check this installation risk before relying on the project: client/v2.6.3
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: client/v2.6.3. Context: Observed during version upgrade or migration.
- Why it matters: Upgrade or migration may change expected behavior: client/v2.6.3
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/client/v2.6.3
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 3: Installation risk requires verification

- Trigger: Project evidence flags a installation risk. Review the linked source before relying on this workflow.
- Host AI rule: Reproduce the official install and quickstart path in an isolated environment.
- Why it matters: May increase setup, validation, or first-run risk for the user.
- Evidence: community_evidence:github | https://github.com/milvus-io/milvus/issues/50282
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 4: Installation risk requires verification

- Trigger: Project evidence flags a installation risk. Review the linked source before relying on this workflow.
- Host AI rule: Reproduce the official install and quickstart path in an isolated environment.
- Why it matters: May increase setup, validation, or first-run risk for the user.
- Evidence: community_evidence:github | https://github.com/milvus-io/milvus/issues/50384
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 5: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: client/v2.6.4
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: client/v2.6.4. Context: Source discussion did not expose a precise runtime context.
- Why it matters: Upgrade or migration may change expected behavior: client/v2.6.4
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/client/v2.6.4
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 6: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: milvus-2.6.13
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: milvus-2.6.13. Context: Observed when using node, python
- Why it matters: Upgrade or migration may change expected behavior: milvus-2.6.13
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/v2.6.13
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 7: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: milvus-2.6.14
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: milvus-2.6.14. Context: Observed when using node, python
- Why it matters: Upgrade or migration may change expected behavior: milvus-2.6.14
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/v2.6.14
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 8: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: milvus-2.6.15
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: milvus-2.6.15. Context: Observed when using node, python, cuda
- Why it matters: Upgrade or migration may change expected behavior: milvus-2.6.15
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/v2.6.15
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 9: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: milvus-2.6.16
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: milvus-2.6.16. Context: Observed when using node, python
- Why it matters: Upgrade or migration may change expected behavior: milvus-2.6.16
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/v2.6.16
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

### Constraint 10: Configuration risk requires verification

- Trigger: Developers should check this configuration risk before relying on the project: milvus-2.6.17
- Host AI rule: Before packaging this project, run the relevant install/config/quickstart check for: milvus-2.6.17. Context: Observed when using node, python
- Why it matters: Upgrade or migration may change expected behavior: milvus-2.6.17
- Evidence: failure_mode_cluster:github_release | https://github.com/milvus-io/milvus/releases/tag/v2.6.17
- Hard boundary: Do not present this pitfall as solved, verified, or ignorable unless later evidence explicitly closes it.

