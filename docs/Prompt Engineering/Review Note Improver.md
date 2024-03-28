# Review Note Improver Template

This template is designed to guide users in transforming their audit file review notes into clearer, more actionable, and professionally polished insights. Leveraging advanced NLP techniques, this template facilitates the refinement of review notes to meet professional auditing standards.

<div align="center">
    <img src="/assets/images/ai_woman.png" alt="Review Note Improver" style="width:50%;">
</div>

## Objective

The primary aim is to aid auditors and audit teams in elevating the quality of their review notes. By doing so, we strive to enhance audit quality and efficiency, fostering better communication and comprehension among team members.

## How to Use the Template

The template serves as a framework for inputting original audit file review notes and receiving an improved version. The enhancement process includes:

- **Clarity and Readability**: Making the note easier to understand.
- **Technical Accuracy**: Ensuring all technical points are correct.
- **Key Findings**: Highlighting the most important points and recommendations.
- **Conciseness**: Removing unnecessary information.
- **Professional Tone**: Adopting a formal and professional language style.

## Prompt Format

To utilize this template effectively, submit your original audit file review note in the following markdown format:

```markdown
# Original Review Note:
> {>>Insert your original review note here<<}

## Instructions for Improvement of {original}:
- Enhance clarity and conciseness.
- Ensure technical accuracy.
- Highlight key findings and recommendations.
- Remove any redundant or non-essential information.
- Maintain a professional tone.

### Examples
[
  {
    "original": "This section could be better. Please check.",
    "improved": "This section would benefit from more detailed examples to support the audit findings. Could you please elaborate further for clarity?"
  },
  {
    "original": "Kind of confusing. Might want to look at it again.",
    "improved": "The argument presented in this section is somewhat unclear. Revising for coherence and adding supporting data could enhance its effectiveness."
  }
]
```


## Improved Review Note Example (input)
```markdown
# Original Review Note:
> {The expenses for this quarter seem off. Check again?}

## Instructions for Improvement of {original}:
- Enhance clarity and conciseness.
- Ensure technical accuracy.
- Highlight key findings and recommendations.
- Remove any redundant or non-essential information.
- Maintain a professional tone.

### Examples
[
  {
    "original": "This section could be better. Please check.",
    "improved": "This section would benefit from more detailed examples to support the audit findings. Could you please elaborate further for clarity?"
  },
  {
    "original": "Kind of confusing. Might want to look at it again.",
    "improved": "The argument presented in this section is somewhat unclear. Revising for coherence and adding supporting data could enhance its effectiveness."
  }
]
```

## Improved Review Note Example (output):
```markdown
[
  {
    "original": "The expenses for this quarter seem off. Check again?",
    "improved": "The recorded expenses for this quarter appear to be inaccurate. Please conduct a thorough review to ensure all expenses are correctly accounted for and align with the financial documentation."
  }
]
```
