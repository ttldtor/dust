# The Dust

An automatically reconfigurable, extensible network of processes, each with a small neural network.

The goal of the project is to determine the possibility of self-learning distributed neural networks.

Each neural network/process ("mote") will be given access to various devices and data sources and consumers. Also, a 
"mote" can interact with other "motes" and generate other "motes" with common properties (selection is applied here 
according to some "successful" parameters)

# Also TODO:

- Create a base58 encoder\decoder (D language)
  - See https://github.com/codingteam/emulsion/blob/7936682904ad7f530a5113d15c5e64d4a1c28afa/Emulsion.ContentProxy/FileCache.fs#L24 
  - @lru_cache UDA (see https://docs.python.org/3/library/functools.html#functools.lru_cache) 