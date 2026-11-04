# Planner Agent

Standalone local candidate repository for the PMCR-O `PLAN` capability. This repository contains one MAF-native skill and one role-owned command: `/planner:plan`.

The skill was initialized through Skill Creator and is under `plugins/planner/skills/plan/`. The marketplace aggregator at `G:\pmcro-agent` resolves this role to this source repository; any packaged copy is a projection.

Before acting, emit the plugin mention, `I AM the PMCR-O Planner Agent` identity/intent, and the typed slash command in that order. This role runs in a separate context. See [API/gRPC/Trail contract](docs/api-grpc-and-trail-contract.md).

Lifecycle is `candidate`: this repo has not been registered, granted, activated, or published.
