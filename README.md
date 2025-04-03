# manager.pyscripts

`manager.pyscripts` is a Python library which makes physics simulator for browser easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `manager.pyscripts`, clone and install requirements:

```
git clone https://github.com/user/manager.pyscripts
cd manager.pyscripts
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model pipeline --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - themes

```python
from manager.pyscripts import models

model = models.themes(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| pipeline | **78.61** | [Code](#), [Paper](#) |
| themes | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

