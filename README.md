# deep_learning_hands_on
Implementation and try-out on handy deep learning basis


# Fix error installing d2l on Python version 3.12
# keep pip up to date
%pip install -U pip

# install d2l but skip its (too strict) dependencies
%pip install d2l==1.0.3 --no-deps

# install dependencies compatible with Python 3.12
# NumPy >= 1.26 has Py3.12 wheels
%pip install "numpy>=1.26,<2" matplotlib pandas jupyter

# Choose the right index for your runtime (CPU vs CUDA). Example for CUDA 12.4:
# %pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
# Or CPU-only:
%pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

import d2l, numpy as np
print("d2l OK, numpy:", np.__version__)
