# Udacity Course on Secure and Private AI

Completed first 2 sections of the course.
- Section 1: Introducing Differential Privacy
- Section 2: Evaluating the Privacy of a Function

Here are my learnings...  
**Note**: Jupyter Notebook Code can be found in the directory `Udacity_Secure_and_Private_AI`

## What is Differential Privacy?
Differential privacy is a mathematical framework that guarantees privacy in data analysis:
- Born in 2003 for statistical databases
- Recently adapted for machine learning
- Core promise: Your data inclusion won't harm you, regardless of external factors

## In Deep Learning Context
The goal is two-fold:
1. Enable neural networks to learn intended patterns
2. Prevent accidental learning of private/sensitive information

## Why It Matters: The Netflix Case Study
A real-world privacy failure:
- Netflix released "anonymized" user ratings
- Researchers could de-anonymize users by:
  - Cross-referencing with public IMDB ratings
  - Using statistical analysis
- Proved that simple anonymization isn't enough

## How Privacy is Measured
Using a simple database example:
1. **Setup**:
   - Database with 5000 users
   - One column of true/false values
   - Represents sensitive information (like medical data)

2. **Privacy Test**:
   - Remove one person from database
   - Run analysis/query
   - If results don't change significantly:
     - That person's privacy is protected
     - No statistical information leaked

3. **Practical Experiment**:
   - Create 5000 database copies
   - Each copy missing one different person
   - Compare query results across all versions
   - Look for changes in outputs

## Key Insight
True privacy means: 
- Your data inclusion shouldn't significantly affect analysis results
- Even with access to other datasets or information sources
- While still allowing meaningful statistical insights

This framework helps us build AI systems that learn from sensitive data while protecting individual privacy.