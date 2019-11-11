# Proposal 1:

Proposal 1 consists of 2 files: run_generation.py and calibrate.py. This separates generation and calibration.

## run_generation.py:

    def set_seed():

    def filtering(logits, **args):
    # return: filtered logits
    
    def get_candidates(model, context, **args):
    # return: list of candidate logits

    def get_probabilities(model, context, **args):
    # return: probability distribution given context

    def sample(logits, context, **args):
    # return: context + next token. Only generates the next sample.

## calibrate.py:
    
    def get_lookahead_entropies(candidate_logits, **args):
    # Calls run_generation.get_probabilities() for each candidate
    # return: lookahead entropies

    def get_calibrated_model(candidate_logits, **args):
    # Calls get_lookahead_entropies on (a subset of the) candidates. 
    # Calibrates the distribution.
    # return: calibrated conditional probability distribution

I hand-waved through the arguments a bit, but the upshot is that calibration only depends on candidate logits and the conditional probability distribution. So calibration can be separated into another file, and calibrate.py can call down to functions in run_generation.py as needed. 

To generate the next token, we can feed the calibrated distribution into `run_generation.sample()` to obtain the next word. 

A drawback here is that we need to pass arguments such as context back and forth between the two files. When generation and calibration are done in the same file, this is not an issue.

# Proposal 2:

Use one script, like Cyril's. More difficult to plug and play.
