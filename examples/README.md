# Examples Directory

This directory contains real-world examples of prompts generated using **Promptor v3.1 Council Edition**.

## Available Examples

| File | Domain | Complexity | Council Recommended |
| --- | --- | --- | --- |
| [risk-analyst.md](risk-analyst.md) | Finance / Credit Scoring | High | ✅ Yes (compliance) |
| [warp-analyst.md](warp-analyst.md) | Software Engineering | Medium | ❌ No |
| [real-estate-strategist.md](real-estate-strategist.md) | Real Estate Investment | Medium | ⚠️ Optional |
| [github-auditor.md](github-auditor.md) | DevOps / Code Quality | Medium-High | ⚠️ Optional |
| [cloud-architect.md](cloud-architect.md) | Cloud Infrastructure | High | ✅ Yes (critical) |
| [cybersecurity-analyst.md](cybersecurity-analyst.md) | Security / Pentesting | High | ✅ Yes (security) |
| [devops-engineer.md](devops-engineer.md) | CI/CD Automation | Medium | ❌ No |
| [data-scientist.md](data-scientist.md) | Machine Learning | Medium-High | ⚠️ Optional |
| [product-manager.md](product-manager.md) | Product Strategy | Medium | ❌ No |
| [system-administrator.md](system-administrator.md) | Linux Administration | Medium | ❌ No |
| [ai-engineer.md](ai-engineer.md) | LLM Integration | High | ⚠️ Optional |

## Legend

- ✅ **Yes**: Council strongly recommended (security, compliance, or high-impact)
- ⚠️ **Optional**: Council beneficial for additional validation
- ❌ **No**: Standard generation sufficient

## How to Use These Examples

1. Read the **User Request** section to see the original requirement
2. Review the **Generated Prompt** to see Promptor's output
3. Check the **Hacks Applied** section to understand optimization techniques
4. Note the **Auto-Critique Score** and reasoning
5. Follow the **Council Recommendation** for critical use cases

## Contributing Examples

To add a new example:

1. Create a new `.md` file in this directory
2. Follow the structure of existing examples
3. Include all sections: User Request, Generated Prompt, Hacks Applied, Auto-Critique, Council Note
4. Update this README with the new entry
5. Submit a PR to the `dev` branch

## Testing Your Prompts

Before deploying generated prompts in production:

- Test with the provided self-validation checklists
- Run edge cases and adversarial inputs
- Consider activating `[COUNCIL]` for critical domains
- Iterate based on real-world feedback
