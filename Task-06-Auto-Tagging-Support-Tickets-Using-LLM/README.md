## Auto Tagging Support Tickets Using LLM

### Objective

Automatically classify support tickets into categories using a Large Language Model (LLM).
The system predicts the top 3 most probable tags for each ticket and compares zero-shot and few-shot learning approaches.

### Dataset

A sample free-text support ticket dataset (tickets.csv) with the following columns:

text	tag
I cannot login to my account	account_access
Password reset not working	account_access
My payment failed	billing
Money deducted but order not placed	billing
App crashes on startup	technical_issue
I want refund	refund
How to change email	general_query

### Labels Used:

account_access
billing
technical_issue
refund
general_query

## Methodology

### 1. Zero-shot Classification

Used HuggingFace facebook/bart-large-mnli model.
Provided only the labels as possible categories.
Model predicts probability for each label and returns top 3 tags.

### 2. Few-shot Classification

Added few example tickets in the prompt for context.
The model uses these examples to better understand ticket-label patterns.
Still predicts top 3 tags for each ticket.

## Accuracy Results
Method	Top-1 Accuracy	Top-3 Accuracy
Zero-shot	0.49	0.93
Few-shot	0.49	0.93

### Observations:

Zero-shot already performs very well for Top-3 predictions.
Few-shot examples did not significantly change Top-3 accuracy for this dataset.
This demonstrates that LLM can effectively suggest relevant tags for support tickets, even with minimal examples.

## Skills Gained
Prompt engineering for LLMs
Zero-shot and few-shot text classification
Multi-class prediction and ranking
Evaluating LLM performance using Top-1 and Top-3 accuracy

### conclusion:
The project demonstrates that LLMs can automatically tag support tickets with high reliability. Even in a small dataset, top-3 suggestions include the correct category 93% of the time, making this approach practical for real-world customer support workflows.