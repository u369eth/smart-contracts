# uToken (Function wise functionality is described in Code)

Description of working of Smart Contract is as follows:

## Functionalities

- Decentralized Lock/Wrap of Tokens or Coins
- Transfer uTokens
- Unlocking Native Tokens and Coins
- Fee Collection System (Benefaction-fee)
- Reward System
- Whitelist Mechanism
- Concealed Private Master Key (i.e., Private Master Key) and Sign Key Mechanism to perform any action
- Smart Contract(s) Whitelist Mechanism (for u369.eth/v2)

### Decentralized Lock/Wrap of Tokens or Coins:

**_Definition:_** Locking/wrapping (i.e., safeguarding) tokens or coins and receiving uToken(s) which is/are equal in numbers to respective tokens or coins after benefaction-fee.

Example: end-user wraps 10 GHO, end-user protects 10 GHO and the u369 smart contract automatically takes a benefaction-fee of 0.369% to fund public goods, reward end-users, contribute to the comunity, developers and to sustain itself.

10 GHO - 0.369% = 9.9631 GHO; thus the u369 smart contract mints 9.9631 uGHO tokens into end-user's account and they can add the minted uTokens to their wallet.

**_Procedure_**

- Enter desired amount to lock/wrap/safeguard.
- System will check if end-user is new to the system or not. In case of new user, the system will provide a Concealed Private Master Key.
- The system prompts the end-user to set and confirm Sign Key (i.e., a strong password or PIN).
- End-user signs an on-chain transaction to set Sign Key.
- Smart contract will save user's Private Master Key and Sign Key.
- Smart contract will collect 0.369% benefaction-fee and will mint respective amount of uTokens into the end-user's account.
- End-user can use the u369 permissionless and decentralized interface any time to perform the operations: Protect (i.e., lock native token(s) and mint uToken(s)). Transfer (i.e., send uToken(s)). Claim (i.e., burn uToken(s) and unlock/unprotect native tokens).

Note: The Concealed Private Master Key will be shown only once and must be kept someplace safe (preferably offline). The Private Master Key helps the end-user to reset their Sign Key.

If the end-user has already set Sign Key and connects their wallet to the u369 smart contract decentralized User Interface (UI) to effect any operation (Protect / Transfer / Claim), the system will show the form to take end-user's desired amount of token(s) to be used in the operation and user must input their Sign Key to make the operation.

The u369 smart contract does not collect any benefaction-fee for transfering or unwrapping uTokens (end-user will only paid the gas network fee).

### Transfer uTokens

**_Description:_** uTokens can only be transfered if end-user enters their Sign Key. Any time any end-user can permissionlessly transfer uTokens to anyone.

**_Procedure_**

- Select uToken and click on transfer button.
- Enter recipient address and amount.
- Enter password Click on transfer button.
- Smart contract will transfer uTokens from sender to recipient.
- Now recipient can come to UI and transfer or unwrap any time.

U369 Smart contract will transfer uTokens from sender to recipient.

The recipient of uTokens can visit the u369.eth decentralized interface and transfer their uTokens any time.

### Unlocking Native Tokens and Coins

**_Definition:_** Unlocking native token(s) or coin(s) from the u369 smart contract to receive native token(s) or coin(s) back to your wallet.

Example: end-user wants to unwrap 9.9631 uGHO, they will enter 9.9631 uGHO and u369 smart contract will burn 9.9631 uGHO and return 9.9631 GHO to the end-user's wallet.

**_Procedure_**

- Enter desired amount to be unlocked/unprotected.
- Input Sign key and click "Unprotect" button.
- Confirm transaction in your wallet.

Smart contract will burn entered amount of uTokens and the respective tokens or coins at will be transferred back to the end-user's wallet at 1:1 ratio.

End-users can claim their native token at any time.

### Fee Collection System

**_Description:_** Each time an end-user locks tokens or coins, a specific and fix percentage (0.369%) will be deducted from the entered amount and remaining amount will be locked/safeguarded.

**_0.369% Benefaction-Fee Collection:_**

- 30% of 0.369% will be transferred to u369gift.eth to reward a randomly selected winner every 369 hours.
- 30% of 0.369% will be transferred to u369impact.eth to fund public goods (10% to Protocol Guild, 10% to Giveth and 10% to Valley Dao).
- 30% of 0.369% will be transferred to u369.eth address.
- 10% of 0.369% will be transferred to u369community-dev.eth for the u369 Community & Developers Benefit Fund.

**_Procedure_**

- Benefaction-fee will be deducted at the time of locking native tokens (i.e., issuing uTokens).

### Reward System

**_Description:_** There are 2 types of reward systems.

**(A) Gift Pool**

Description: Every 369 hours a "Recipient" candidate will be randomly selected. The candidate can receive the full amount of rewards if proper conditions are met.

**_Procedure_**

- Each detail will be shown on the "Rewards" page regarding collectable assets.

The randomly selected "Recipient" candidate's address will be shown in the "Rewards" page.

- Reward will be sent from the u369gift.eth address to the randomly selected winner's address within 72 hours of being selected as winner.

Gift Pool Conditions can be seen in the u369.eth decentralized UI (Rewards page). These conditions are outside of the code's scope as those are bound to a game theoretical approach and are performed manually. The transparency nature of the blockchain(s) where uTokens would be deployed attest for its fullfilment.

Note: The Impact Pool (u369impact.eth) is a supplementary receiver of funds, it does not have its own timer per se; however, it works in parallel with the 369 hours timer. Funds within this pool are used for public goods funding.

**(B) Stateless Pool**

**_Description:_** A "Recipient" candidate is randomly selected every 369 days.

**_Procedure_**

- The random selection every 369 days works within the same conditions as the random selection every 369 hours. Please see "Rewards" page >> Stateless Pool Conditions.

Note: After the reward is sent to the randomly selected winner, any remaining funds inside the Stateless Prize address is sent to the u369fractal.eth smart contract address to be distributed like this:

- 10% to the u369 Community & Developers Benefit Fund
- 30% to fund public goods
- 30% to randomly reward u369.eth end-users
- 30% to u369.eth

### Private Master Key and Sign Key Mechanism to perform any action

**_Description:_** To prevent users from transferring funds directly from any wallet, for example Metamask, the following feature has been implemented: On each uToken(s) operation (transfer or claim/unprotect) the end-user must enter their Sign Key on the decentralized u369.eth interface, otherwise transaction will fail.

In case of losing or forgetting Sign key, a recovery phrase functionality mechanism is implemented:

If end-user wants/has to change their Sign Key, the Private Master Key will be used.

### Smart-Contract(s) Whitelist Mechanism (for u369.eth/V2)

**_Definition:_** For whitelisted smart-contracts the end-users needs to enter their password in the u369 decentralized interface to transfer funds to a smart contract protocol. Once funds are transferred to another smart contract protocol, the smart contract protocol can transfer uTokens without needing to input a password to move the uTokens.

If the uTokens would be transferred from the smart contract protocol to an end-user's address, then the new recipient of uTokens must input their Sign key (or set their Sign key if they would not have one) in the u369 decentralized interface to move the received uTokens.

**Implementation Guide:**

To transfer uTokens to a smart contract, for example AAVE or Uniswap, the end-user must enter Sign key.

If sender of uTokens is Uniswap or AAVE: u369 will check if the sender is a contract address, and then u369 will allow the whitelisted contract address to transfer uTokens without any end-user Sign key.

**Strategy to Implement Whitelist Functionality:**

There are two ways to check that caller is a contract address or not:

- if(msg.sender == tx.origin): in case of true, caller is EOA otherwise caller is a contract.

- if(msg.sender.code.length == 0): in case of true, caller is an EOA otherwise caller is a contract.

**_Note:_**

(i) Any of the above can be used to check whether caller is an EOA or a contract.

(ii) isContract() function of Address Library is deprecated due to security reasons.

(iii) New library added, exempt of security concerns.
