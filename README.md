# MNIST Dataset for Torch #

Please see [Yann LeCun's page](http://yann.lecun.com/exdb/mnist/) for the original MNIST dataset.

## Installation ##

torch-rocks install https://raw.github.com/andresy/mnist/master/rocks/mnist-scm-1.rockspec

## Usage ##

```lua
local mnist = require 'mnist'

local trainset = mnist.traindataset()
local testset = mnist.testdataset()

print(trainset.size) -- to retrieve the size
print(testset.size) -- to retrieve the size
```

Then, the i-th example is retrieved with:
```lua
local ex = trainset[i]
local x = ex.x -- the input (a 28x28 ByteTensor)
local y = ex.y -- the label (0--9)
```
