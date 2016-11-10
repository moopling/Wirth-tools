Wirth Tools
===========
Wirth is a set of tools to automate construction of a recursive-descent
parser in the Wirth style.

*	ffi2code takes the intermediate first and follow set definitions
	(.ffi file) and outputs header file definitions and array
	definitions for the FIRST() and FOLLOW() sets.




TODO/ideas:
-----------

*	Given an (optional) directory containing several files,
	it creates a table with the empirical correlation
	coefficients for all the language's tokens, and for
	non-reserved tokens (identifiers)

*	ebnf2ffi to take an EBNF grammar and output an intermediate
	form of first and follow set definitions (.w file).

*	ebnf2parser to take an EBNF grammar and outputs code (C,
	Noisy) for a skeletal parser. The entire flow is analogous
	to YACC and ANTLR, but with a focus on:
	(1)	The role of the FIRST() and FOLLOW() set generation,
		which is particularly useful for features such as
		code completion and useful error reporting
	(2)	Building a recursive descent parser rather than a
		bottom-up table-driven parser.
	(3)	The tools ebnf2ffi and ffi2code are largely independent
		of the language in which the parser will eventually be
		written, and can serve as intermediate stages for tools
		such as converting EBNF to graphviz visualizations.
