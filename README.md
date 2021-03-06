# Solving Puzzles with Constraint Programming

## Clojure and Loco

> A number of puzzles solved in Clojure using
[Loco](https://github.com/aengelberg/loco)

To work with any of these puzzle solvers, you'll want to boot up a lein
repl:

```bash
$ lein repl
```

### Sudoku

Load the formulation of the sudoku puzzle

```clojure
(load-file "./sudoku.clj")
```

Get a solution with

```clojure
(solution model)
```

### 4 Queens

Load the formulation of the 4 Queens puzzle

```clojure
(load-file "./4-queens.clj")
```

No solution at the moment.

### 4 Queens (Numeric)

Load the formulation of the 4 Queens puzzle

```clojure
(load-file "./4-queens-numeric.clj")
```

Get all the solutions with

```clojure
(solutions model)
```

### [8 Queens](https://en.wikipedia.org/wiki/Eight_queens_puzzle)

Load the formulation of the 8 Queens puzzle

```clojure
(load-file "./8-queens.clj")
```

Get all the solutions with

```clojure
(solutions model)
```

Check how many solutions were found (there should be 92)

```clojure
(count (solutions model))
```

## Z3

> Constraint programming with Microsoft's [Z3](http://rise4fun.com/Z3)
> Theorem Prover

Use Z3 in the browser at [rise4fun/z3](http://rise4fun.com/Z3).

```
(declare-fun x () Int)
(declare-fun y () Int)
(declare-fun z () Int)

(assert (> x y))
(assert (> y z))
(assert (> z x))
(check-sat)
```

## License

&copy; 2016 Josh Branchaud

Licensed under the MIT license
