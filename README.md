COS 397: Junior Independent Work  
Princeton University, Fall 2019  
Michael Hu  
Advisor: [Karthik Narasimhan](https://www.cs.princeton.edu/~karthikn/ "Karthik's Homepage")

# Introduction

This independent work extends the work of [Braverman et. al.](https://arxiv.org/abs/1906.05664)
We are interested in fixing entropy rate drift, where the entropy rates of language 
model generations drift upwards over time. Qualitatively, the generations become
gibberish.

The original technique proposed by Braverman et. al. is computationally 
inefficient. Here, we propose some techniques to speed the technique up.

For the code, pull my fork of HuggingFace's lovely [Transformers repo](https://github.com/mikkyhu/transformers).
