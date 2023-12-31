# Parsers
- _The majority of the comments in this section will be comments written inline, along with the code_

## Functional Parsing
- Functional parsing is essentially when you have a function (parser combinator) that takes in other functions (parsers) as input and outputs a function (a more complex parser)

## The Parsec Library
- The Parsec library defines a set of common combinations much like the operators defined in NanoParsec.hs
- 'char': Match the given character
- 'string': Match the given string
- '<|>': The choice operator tries to parse the first argument before proceeding to the second
- 'many': Consumes an arbitrary number of patterns matching the given pattern and returns them as a list
- 'many1': Like many but requires at least one match
- 'sepBy': Match an arbitrary length sequence of patterns, delimited by a given pattern
- 'optional': Optionally parse a given pattern returning its value as a 'Maybe' monad
- 'try': Backtracking operator will let us parse ambiguous matching expressions and restart with a different pattern
- 'parens': Parses the given pattern surrounded by parenthesis