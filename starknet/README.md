# StarkNet development guidelines

This page presents the internal StarkNet development guidelines at OnlyDust. Please read them before contributing to our projects.

# Naming convention

Generally speaking, namespaces, structs, functions, variables, etc. should be named with care to be as clear as possible. 
Someone reading the code should understand what a variable holds, or what a function does, just by reading its name.

We avoid abbreviations, unless it is explicitly defined in the [Known abbreviations](https://www.notion.so/Naming-convention-e02e496b5c364c55af96aa9540942924) table.

| Object | Visibility | Pattern | Example |
| --- | --- | --- | --- |
| Contract (file) name | N/A | snake case | only_dust |
| Interface name | N/A | CamelCase starting with an uppercase I | IShip |
| Contract attribute | N/A | snake case suffixed by an underscore | tournament_name_ |
| Contract constant | All | capital letters separated with underscores | ERC1820_MAGIC_NUMBER |
| Function name | view/external | snake case | is_interested() |
| Function name | internal | snake case, inside a namespace internal | prepare_next_round() |
| Function parameter | N/A | snake case | funding_prize |
| Function return parameter | N/A | snake case | funding_prize |
| Local variable | N/A | snake case | bounty_beneficiary |
| Namespace | N/A | snake case, excepted for interfaces | tournament |

### Specific naming

| Object | Pattern | Example | Comment |
| --- | --- | --- | --- |
| Recursive function | snake case suffixed by _loop | move_dust_loop() | should never be view/external |
| Array | must be in the plural form | ships |  |
| Array length | name of the array, suffixed by _len | ships_len |  |

### Known abbreviations

| What? | Abbreviation |
| --- | --- |
| Identifier | id |

# Design patterns

We are adopting some conventions and patterns at OnlyDust that are described in a few articles. 
Please read them carefully. They will help you understand the existing code base of our repositories, 
and contribute in a way that follows the same principles and integrate nicely with the rest of the code.

TODO: PUBLISH ARTICLES

[https://mirror.xyz/0xBa9E280B752B09eA866E9Cc0C8fE0fCef241B63c/uHOrdw780uaOSP-pNgIDiEPqvTT1eL0W1QJpPZuhdPw](https://mirror.xyz/0xBa9E280B752B09eA866E9Cc0C8fE0fCef241B63c/uHOrdw780uaOSP-pNgIDiEPqvTT1eL0W1QJpPZuhdPw)

[https://mirror.xyz/0xBa9E280B752B09eA866E9Cc0C8fE0fCef241B63c/ekwvUpolvVtZBVutk2D-hoxgCh0AtiK8QM_zfnvJ1fE](https://mirror.xyz/0xBa9E280B752B09eA866E9Cc0C8fE0fCef241B63c/ekwvUpolvVtZBVutk2D-hoxgCh0AtiK8QM_zfnvJ1fE)
