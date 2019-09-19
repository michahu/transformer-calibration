# Readings

Mostly chose readings this week that related to prior calibration approaches.

### Dawid 1985
- Uses weather as the motivating example.
- "well calibrated" - giving predictions whose properties match that of the 
data.
- Proposed calibration works with sequential data with feedback.

### Platt 1999
- Obtaining calibrated probability from SVM using a sigmoid.
- Step 1: Train SVM. Step 2: Train parameters of an additional sigmoid function.
Result: an uncalibrated, binary function (SVM) is transformed into a posterior
probability.

### Elkan 2002 

Obtaining probability estimates for multiclass problems, as opposed
to binary classifications.

### Caruana 2005 

Applications of Platt 1999 and Elkan 2002.

### Guo 2017
- defines confidence calibration as predicting probability estimates 
representative of the true correctness likelihood.
- Claim: ML systems should also provide a calibrated confidence measure - a 
probability associated with the output label that reflects its ground truth
correctness likelihood.
- Issue: Current neural networks have confidences much higher than their 
actual accuracies, indicating that the latest techniques are miscalibrated.

Thoughts after reading Guo:
- Can we say that a higher entropy difference (when generated text has a higher
entropy compared to the sample text) is indicative of incorrectness?
    - Is this qualitiatively true? Can we observe that a generated text of 
higher entropy than ground truth is noticeably bad when comparing it to the 
actual text?

# Misc

Entropy - average number of bits needed to encode info
Perplexity - how well a probability model predicts a sample
Cross-entropy loss - measures how off a prediction is from the true label (0 or 1)
KL divergence - how different two probability distributions are from each other
High perplexity = the model is "confused"
