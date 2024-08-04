# uToken (Function wise functionality is described in Code)

Description of working of Smart Contract is as follows:

## Functionalities

- Decentralized Lock/Mint of Tokens
- Transfer uTokens
- Unlocking Native Tokens
- Fee Collection System (Benefaction-fee)
- Reward System
- Whitelist Mechanism
- Concealed Master Key (Master Key) and Sign Key Mechanism to perform any action
- Smart Contract(s) Whitelist Mechanism (for u369.eth/v2)

### Decentralized Lock/Mint of Tokens:

**_Definition:_** Locking/Minting (locking: safeguarding native tokens) and (minting: receiving uTokens) which are equal in numbers to respective native tokens after benefaction-fee (1:1 ratio).

Example: end-user protects/locks 10 GHO, and the u369 smart contract automatically takes a benefaction-fee of 0.369% (the benefaction-fee is previously displayed to the user to exert full transparency and for the user to become aware of it) the benefaction-fee is used to fund public goods, reward end-users, contribute to the comunity, developers and to sustain u369.eth (the social good).

10 GHO - 0.369% = 9.9631 GHO; thus the u369 smart contract mints 9.9631 uGHO tokens into end-user's account and they can add the minted uTokens to their wallet.

**_Procedure_**

- Enter desired amount of token(s) to lock/safeguard.
- System will check if end-user is new to the system or not. In case of new user, the system will provide a Concealed Master Key.
- The system prompts the end-user to set and confirm Sign Key (i.e., a strong password or PIN).
- End-user signs an on-chain transaction to set Sign Key.
- Smart contract will save user's Master Key and Sign Key.
- Smart contract will collect 0.369% benefaction-fee and will mint respective amount of uTokens into the end-user's account.
- End-user can use the u369 permissionless / decentralized interface any time to perform the operations: Protect (i.e., lock native token(s) and mint uToken(s)). Transfer (i.e., send uToken(s)). Claim (i.e., burn uToken(s) and unlock/unprotect native tokens).

Note: The Concealed Master Key will be presented only once and must be kept someplace safe (preferably offline). The Master Key is randomly generated and issued with separators (-) to facilitate its migration from online to off-line with near-zero possibility of mispelling it. The Master Key helps the end-user to reset their Sign Key.

If the end-user has already set Sign Key and connects their wallet to the u369 smart contract -decentralized User Interface (UI)- to effect any operation (Protect / Transfer / Claim), the system will show the form for the end-user to input the desired amount of token(s) to be used in the operation and user must input their Sign Key to make the operation.

The u369 smart contract does not collect any benefaction-fee for transfering or burning uTokens (end-user will only paid the gas network fee to validators).

### Transfer uTokens

**_Description:_** uTokens can only be transfered if end-user enters their Sign Key. Any time the end-user can permissionlessly transfer uTokens to anyone.

**_Procedure_**

- Click on "Transfer" button for the respective uToken to populate the transfer form (pop-up/modal).
- Enter amount and recipient address.
- Enter Sign Key and click on "Transfer" button.
- Confirm transaction in wallet.
- Smart contract will transfer uTokens from sender to recipient.

u369 Smart contract will transfer uTokens from sender to recipient.

The recipient(s) of uTokens can use the permissionless / decentralized u369.eth interface at any time to transfer their uTokens and/or to claim native tokens.

### Unlocking Native Tokens

**_Definition:_** Unlocking native token(s) from the u369 smart contract to receive native token(s) to your wallet.

Example: end-user wants to burn 9.9631 uGHO, they will enter 9.9631 uGHO and the u369 smart contract will burn 9.9631 uGHO and return 9.9631 GHO to the end-user's wallet.

**_Procedure_**

- Enter desired amount of uTokens to burn in order to unlock/unprotect the respective amount of native tokens.
- Input Sign key and click "Unprotect" button.
- Confirm transaction in your wallet.

Smart contract will burn entered amount of uTokens and the respective native tokens will be automatically unlocked and transferred back to the end-user's wallet at 1:1 ratio.

End-users can claim their native token at any time.

### Fee Collection System

**_Description:_** Each time an end-user locks tokens, a specific and fix percentage (0.369%) will be deducted from the entered amount and remaining amount will be locked/safeguarded.

**_0.369% Benefaction-Fee Collection:_**

- 30% of 0.369% will be transferred to u369gift.eth to reward a randomly selected "Recipient" candidate every 369 hours.
- 30% of 0.369% will be transferred to u369impact.eth to fund public goods (10% to Protocol Guild, 10% to Giveth and 10% to Valley Dao).
- 30% of 0.369% will be transferred to u369.eth address to self sustain u369.eth (the social good).
- 10% of 0.369% will be transferred to u369community-dev.eth for the u369 Community & Developers Benefit Fund.

**_Procedure_**

- Benefaction-fee will be deducted at the time of locking native tokens (i.e., minting uTokens).

### Reward System (Timeless Pools)

**_Description:_** There are 2 types of reward systems. The Gift Pool and the Stateless Pool. In each pool a "Recipient" candidate is randomly selected.

To implement this the u369 system uses the following formula:

`uint randomNumber = uint(keccak256 (abi.encodePacked (previousTimePeriod, deployTime))) % depositorsLength;`

In simple words, the procedure is defined in the following steps:

1. A keccak hash (hashing algorithm) is applied on the previous time period and contract deploy time.
2. Hash is converted to integer value.
3. A modulus operation performs on the converted integer and number of addresses in the last time period.

**(A) Gift Pool**

Description: Every 369 hours a "Recipient" candidate will be randomly selected. The candidate can receive the full amount of rewards if proper conditions are met.

**_Procedure_**

- Each detail will be shown on the "Rewards" page regarding collectable assets.

The randomly selected "Recipient" candidate's address (6 first and 6 last carachters) will be shown in the "Rewards" page.

- If the "Recipient" candidate fulfils the Gift Pool's stated conditions, the award will be sent from the u369gift.eth address to the randomly selected "Recipient" candidate's address. The "Recipient" candidate has 3 days, 6 hours and 9 minutes to fulfill their part after being selected, if fulfilled the "Recipient" candidate will receive their award within 72 hours after the 3 days, 6 hours and 9 minutes have elapsed.

Gift Pool Conditions can be seen in the u369.eth permissionless UI (Rewards page). These conditions are outside of the code's scope as those are bound to a game theoretical approach and are performed manually.

Note: The Impact Pool (u369impact.eth) is a supplementary receiver of funds, it does not have its own timer per se; however, it works in parallel with the 369 hours timer. Funds within this pool are used for public goods funding.

**(B) Stateless Pool**

**_Description:_** A "Recipient" candidate is randomly selected every 369 days.

**_Procedure_**

- The random selection every 369 days works within the same conditions as the random selection every 369 hours. Please see "Rewards" page >> Stateless Pool Conditions.

Note: After the award is sent to the randomly selected "Recipient" candidate, any remaining funds inside the Stateless Pool address is sent to the u369fractal.eth smart contract to be distributed as follows:

- 10% to the u369 Community & Developers Benefit Fund
- 30% to fund public goods
- 30% to randomly reward u369.eth end-users
- 30% to u369.eth (the social good)

### Master Key and Sign Key Mechanism to perform any action

**_Description:_** To prevent users from transferring funds directly from any wallet, for example Metamask, the following feature has been implemented: On each uToken(s) operation (transfer or claim/unprotect) the end-user must enter their Sign Key on the permissionless u369.eth interface, otherwise transaction will fail.

In case of losing or forgetting Sign key, a recovery phrase functionality mechanism is implemented:

If end-user wants/has to change their Sign Key, the Master Key will be used.

### Smart-Contract(s) Whitelist Mechanism (for u369.eth/V2)

**_Definition:_** For whitelisted smart-contracts the end-users needs to enter their Sign Key in the u369 permissionless interface to transfer funds to a smart contract protocol. Once funds are transferred to another smart contract protocol, the smart contract protocol receiving the uTokens can transfer uTokens internally or externally without needing to input a Sign Key to move the uTokens.

If the uTokens would be transferred from the smart contract protocol to an end-user's address, then the new recipient of uTokens must input their Sign key (or set their Sign key via u369.eth if they would not have a Sign Key).

**Implementation Guide:**

To transfer uTokens to a smart contract, for example AAVE or Uniswap, the end-user must enter Sign Key.

For example, if AAVE or Uniswap receives uTokens and AAVE or Uniswap is now the sender of uTokens: u369 will check if the sender is a contract address, and then u369 will allow the whitelisted contract address to transfer uTokens internally or externally without any end-user Sign key.

**Strategy to Implement Whitelist Functionality:**

There are two ways to check that caller is a contract address or not:

- if(msg.sender == tx.origin): in case of true, caller is EOA otherwise caller is a contract.

- if(msg.sender.code.length == 0): in case of true, caller is an EOA otherwise caller is a contract.

**_Note:_**

(i) Any of the above can be used to check whether caller is an EOA or a contract.

(ii) isContract() function of Address. 

Library is deprecated due to security reasons.

New library added, exempt of security concerns.
