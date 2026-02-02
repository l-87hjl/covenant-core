# AI Emergence Under Constraint

A structured framework for systematic comparison of AI safety architectures, emergence scenarios, and constraint factors.

## Purpose

This repository provides a taxonomy and comparison methodology for analyzing how different AI system designs might behave under various emergence conditions. It is **not a prediction system**—it's a tool for organizing and comparing architectural approaches to AI safety.

## Key Features

- **Multiple Architecture Families**: Comparative analysis of shard systems, mesh designs, governance layers, and traditional approaches
- **Scenario Mapping**: Structured catalog of failure narratives with triggers, indicators, and mitigations
- **Design Primitives Library**: Reusable components that work across architectures
- **Constraint Awareness**: Physics, economics, and systems limits as first-class factors
- **Documentation-First**: Thinking framework before simulation framework

## Organization

- `docs/` - Conceptual foundations and terminology
- `frameworks/` - Named AI architecture approaches (Shard, Mesh, etc.)
- `primitives/` - Cross-cutting design components (shards, eval loops, etc.)
- `scenarios/` - Failure narratives and test conditions
- `references/` - Cultural anchors and analogies
- `sim/` - Simulation schemas (future capability)
- `reports/` - Generated comparison matrices and analyses

See [INDEX.md](INDEX.md) for complete navigation.

## Getting Started

1. Read [PROJECT_SPEC.md](PROJECT_SPEC.md) for detailed project goals
2. Review [docs/taxonomy_overview.md](docs/taxonomy_overview.md) for conceptual map
3. Explore individual frameworks in `frameworks/`
4. Check [INDEX.md](INDEX.md) for complete file listing

## Contributing

This is a living research framework. When adding content:
- Follow folder taxonomy (never dump in root)
- Include metadata headers in key files
- Cross-reference between frameworks, primitives, and scenarios
- Document assumptions explicitly

## License

MIT License - See [LICENSE](LICENSE) for details
