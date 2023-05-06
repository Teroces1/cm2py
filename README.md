# cm2py

cm2py is a Python package for generating and manipulating save strings for the roblox game [Circuit Maker 2](https://www.roblox.com/games/6652606416/Circuit-Maker-2).

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install cm2py.

```bash
pip install cm2py
```

## Usage

Basic program to generate a line of 8 looping OR gates:

```python
import cm2py as cm2

save = cm2.save()

blocks = []
connections = []

for i in range(8):
	blocks.append(save.addBlock(cm2.OR, (i, 0, 0)))

for i in range(8):
	connections.append(save.addConnection(blocks[i-1], blocks[i]))

save.exportSave()
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)