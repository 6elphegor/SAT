# SAT
An SAT solver powered by interaction combinators. It enumerates the entire input space and finds all solutions.

## Requirements
- [HVM3](https://github.com/HigherOrderCO/HVM3/tree/main)

## Installation
1. Install HVM3 following the instructions in their repository
2. Clone this repository

## Usage
Run the solver using the HVM virtual machine:
```shell
hvml run sat.hvml -C
```

### Example Run
```shell
$ time hvml run sat.hvml -C
[1 0 0 0 0 1 0 0 1 0 0 0 0 1 1 0 1 0 0 1]
[1 0 0 0 0 1 0 0 0 0 0 0 1 1 1 0 1 0 0 1]
[1 0 0 0 0 1 0 0 1 0 0 0 1 1 1 0 1 0 0 1]
[1 0 0 1 0 1 0 0 0 0 0 0 1 1 1 0 1 0 0 1]
[1 0 0 1 0 0 0 0 0 1 0 0 1 1 1 0 1 0 0 1]
[1 0 0 1 0 0 0 1 0 1 0 0 1 1 1 0 1 0 0 1]
[1 0 0 1 0 1 0 0 0 1 0 0 1 1 1 0 1 0 0 1]
[0 1 1 1 0 0 0 1 1 1 1 0 0 1 1 0 1 1 1 1]

real    0m0.133s
user    0m0.118s
sys     0m0.014s
```

## How It Works
The solver uses interaction combinators to achieve beta optimal evaluation. By leveraging superpositions, it can explore multiple solution paths simultaneously, significantly reducing the time needed to find all satisfying assignments.

## License
MIT
