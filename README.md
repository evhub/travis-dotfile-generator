# [Travis CI](https://travis-ci.org/) Dotfile Generator

Generates `.travis.yml` files from Python/Coconut scripts. Travis Dotfile Generator is written in [Coconut](https://github.com/evhub/coconut).

## Installation

```
pip install coconut
git clone https://github.com/evhub/travis-dotfile-generator.git
coconut travis-dotfile-generator
pip install travis-dotfile-generator
```

## Usage

```python
import travisgen

@functools.partial(travisgen.builder, ".", "python", ["2.7", "3.4"])
# or in Coconut, @travisgen.builder$(".", "python", ["2.7", "3.4"])
def travismaker(version):
    ...
    return install_cmds, script_cmds

if __name__ == "__main__":
    travismaker()
```
