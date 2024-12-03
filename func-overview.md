Notes
* Unlike Solidity in FunC we don't have predefined functions in the contract that users can call, but one function that parses the message, gets the neccessary flag and triggers neccessary instructions from inside

# Types
* `int` is the type of 257-bit signed integers. By default, overflow checks are enabled and lead to integer overflow exceptions.
* `cell` is the type of TVM cells. All persistent data in TON Blockchain is stored in trees of cells. Every cell has up to 1023 bits of arbitrary data and up to four references, 256 bits each, to other cells. Cells serve as memory in stack-based TVMs.
* `slice` is the type of cell slices. A cell can be transformed into a slice, and then the data bits and references to other cells from the cell can be obtained by loading them from the slice.
* `builder` is the type of cell builders. Data bits and references to other cells can be stored in a builder, and then the builder can be finalized to a new cell.
* `tuple` is the type of TVM tuples. Tuple is an ordered collection of up to 255 components with arbitrary value types that are possibly distinct.
* `cont` is the type of TVM continuations. Continuations are used for controlling the flow of the TVM program execution. It is rather low-level object from the perspective of FunC, although paradoxically quite general.
* 

`cell::begin_parse()` - Extracts whole message data and returns it in a `slice` type
`slice::load_uint(int n)` - Reads first `n` and returns it after converting into `int` type

# Base Functions

```funC
() recv_internal(cell in_msg_full, slice in_msg_body) impure {

}
```

*TON FunC* smart contract's `recv_internal()` function is called when message is passed to it. 
It is important to keep the signature correct `(cell in_msg_full, slice in_msg_body) impure`
* `cell in_msg_full` - Whole messasge sent to the contract
* `slice in_msg_body` - Main part of the message in a form of slice extracted from `in_msg_full`




