# Concept of Tensor

Tensor in Chinese is 张量, which means a multidimensional array. It can be a high-dimensional extension of scalars. vectors, and matrices.

Scalars can be reffered to as 0-dimensional tensors, vectors can be reffered to as 1-dimensional tensors, matrices can be referred to as 2-dimensional tensors, and RGB images can represent 3-dimensional tensors.

1. in PyTorch, Tensors are similar to ndarrays in NumPy, while Tensors can be compited using GPUs.
```
from __future__ import print_function
import torch
```
2. Construct Tensor


```
# Construct a tensor directly with the data:
# torch.tensor(data, dtype=None, device=None, requires_grad=False, pin_memory=False)
x = torch.tensor([6.12, 4])
```

```
# Construct a matrix without initialization:
x = torch.empty(6,12)

# Construct a matrix randomly:
x = torch.rand(6, 12)

# Construct a matrix that is all 0:
x = torch.zeros(6,12)

# Construct a matrix that is all 1:
x = torch.ones(6,12)

# Create a tensor based on an existing tensor.
x = x.new_ones(6, 12, dtype=torch.double)   # new_* methods take in sizes   

x = torch.randn_like(x, dtype=torch.float)   # override dtype

# result has the same size

```
3. size
```
x.size()
```

4. Operate
```
#add
torch.add(x, y)

y.add_(x)

x + y
```

5. Change size
```
x = torch.randn(4, 4)
y = x.view(16)
z = x.view(2, 8)  # the size -1 is inferred from other dimensions
print(x.size(), y.size(), z.size())
```
