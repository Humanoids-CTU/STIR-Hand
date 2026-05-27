# STIR-Hand

This is the repository for the analysis conducted for the STIR-Hand paper, currently under review. [TODO: Add link to paper after publication]. The STIR-Hand is an underactuated, safe, tendon-driven, two-finger robotic hand actuated by two independent motors. 

![STIR-Hand Design](STIR-Hand_design.png)

The two .ipynb files provide self-contained code for the analysis and results reported in the paper. The file STIR-Hand-Analysis provides code for the unsupervised analysis and object classification experiments. The file STIR-Hahnd-LSTM provides an LSTM model for learning the classification task on raw data rather than on extracted features.
---

## Setup

Requires Python 3.10. Install [virtualenv](https://virtualenv.pypa.io/en/latest/) if you don't have it:

```bash
pip install virtualenv
```

Create and activate a virtual environment:

```bash
virtualenv -p /usr/bin/python3.10 STIRHand_env
source STIRHand_env/bin/activate
```

Install dependencies:

```bash
# CPU only
pip install -r requirements-cpu.txt

# GPU/CUDA (Required for running the LSTM model) (adjust cu121 to match your driver — check https://pytorch.org/get-started/locally/)
pip install -r requirements-cuda.txt
```
