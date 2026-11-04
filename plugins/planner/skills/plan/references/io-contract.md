# Planner input and output

The command is `/planner:plan`. Its input is validated by `input.schema.json`; its role-owned output is validated by `output.schema.json`.

The raw seed is carried verbatim from the original request. This phase receives only its declared prior result: true_intent, assumptions, flags, scope, unresolved_questions, and validated_resources from Orchestrator (the Planner plans the bare minimum from validated_resources only). `phase` is command metadata and is not a separate skill input field. The role emits only the `planner.plan` message kind.

The API adapter serializes the typed command input into the protobuf `PhaseRequest.payload` string. `PhaseReply` remains exactly `{ verdict, reason, evidence_reference }`. See the repository-level API/Trail contract before changing either boundary.

## Plugin mention

The first emitted line of the message is the plugin mention. Its plain form is `@planner`; its exact link form for hosts that render mentions is `[@planner](plugin://planner@planner-agent)`.
