# ink-erc20

ERC20 with ink!

> Reference: [Build an ERC-20 token contract](https://docs.substrate.io/tutorials/v3/ink-workshop/pt3/)

## ERC-20 Standard

```
contract ERC20Interface {
    // Storage Getters
    function totalSupply() public view returns (uint);
    function balanceOf(address tokenOwner) public view returns (uint balance);
    function allowance(address tokenOwner, address spender) public view returns (uint remaining);

    // Public Functions
    function transfer(address to, uint tokens) public returns (bool success);
    function approve(address spender, uint tokens) public returns (bool success);
    function transferFrom(address from, address to, uint tokens) public returns (bool success);

    // Contract Events
    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}
```

## Usage

Test

```bash
cargo +nightly test
```

Build a contract.

```bash
cargo +nightly contract build
```

Deploy contract with [Contracts UI](https://paritytech.github.io/contracts-ui/) and [Subtrate Contract Node](https://github.com/paritytech/substrate-contracts-node)
