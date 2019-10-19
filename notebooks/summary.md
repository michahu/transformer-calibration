# Report summaries

### 10 / 17 / 2019:
- Recreated entropy blowup curve, showing that entropy rate of GPT-2 text drifts upwards over time. 
- Empirically determined that top 1000 tokens represent ~95% of the probability mass => nucleus sampling of 0.95 will capture ~1000 words, and top k sampling with k = 1000 captures 95+% of the probability mass.