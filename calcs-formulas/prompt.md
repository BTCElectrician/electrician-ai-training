PROMPT FOR ELECTRICAL CALCULATIONS KNOWLEDGE BASE STRUCTURE

When creating JSON structures for electrical calculations and code references, follow this standardized format designed to teach both the "how" and "why" of electrical work. Each calculation topic should be organized as follows:

1. TOP LEVEL STRUCTURE
{
  "electrical_calculations": {
    "[calculation_type]": {
      "title": "Clear, descriptive title of the calculation type",
      "description": "Thorough explanation of what this calculation is used for and why it matters in electrical work"
    }
  }
}

2. CODE REFERENCES SECTION
Include as an array of objects that each contain:
- title: Clear description of the code requirement
- section: Specific NEC reference
- description: Plain-language explanation of why this code requirement exists
- key_points: Array of crucial requirements and considerations

3. CALCULATION METHODS SECTION
For each calculation type, include:
- basic_formula: The fundamental equation with clear variable definitions
- variables: Detailed explanation of each variable including units and special considerations
- steps: Step-by-step process for performing the calculation
- example: Real-world scenario with detailed solution steps
- common_pitfalls: What to watch out for

4. PRACTICAL CONSIDERATIONS
Include:
- installation_tips: Real-world guidance for applying the calculations
- common_mistakes: What apprentices often get wrong and how to avoid it
- troubleshooting_guide: How to identify and fix common issues

Example structure for a calculation topic:
{
  "electrical_calculations": {
    "motor_circuits": {
      "title": "Motor Circuit Calculations",
      "description": "...",
      "code_references": [
        {
          "title": "Branch Circuit Conductor Sizing",
          "section": "NEC 430.22",
          "description": "...",
          "key_points": [...]
        }
      ],
      "calculation_methods": {
        "branch_circuit_sizing": {
          "basic_formula": {
            "equation": "...",
            "variables": {...},
            "steps": [...]
          },
          "example": {
            "scenario": "...",
            "solution": {
              "step1": {...},
              "step2": {...}
            }
          }
        }
      },
      "practical_considerations": {
        "installation_tips": [...],
        "common_mistakes": [...],
        "troubleshooting_guide": {...}
      }
    }
  }
}

IMPORTANT GUIDELINES:
1. Always include real-world examples with step-by-step solutions
2. Explain the reasoning behind each calculation step
3. Reference specific NEC code sections for requirements
4. Include common mistakes and troubleshooting guidance
5. Use clear, consistent terminology
6. Provide practical installation tips
7. Include both basic and advanced scenarios when relevant

This structure ensures the GPT can effectively:
- Teach calculation methods step-by-step
- Explain code requirements clearly
- Provide practical guidance
- Help troubleshoot common issues
- Guide users through real-world applications

When adding new electrical calculation topics, follow this same structure to maintain consistency and educational value throughout the knowledge base.