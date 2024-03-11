# Out of memory

1. case 1 :

is caused by storing tensors attached to a computation graph by mistake and is thus expected.
This can happen e.g. if you are accumulating the outputs of your model or the loss via:

`running_loss += loss`

without detaching the loss tensor beforehand or by storing these tensors in e.g. a list.
Check your code if this could be the case, too. `.detach()`

