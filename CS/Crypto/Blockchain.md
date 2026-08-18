---
onenote-id: 0-02db5bc56a224619970f28e65ca58b64!1-D084F068F621FF9!3718
---
![Block 10 HashO TxO Block 11 Hash23 Hash2 Tx2 Block...](../../img/OneNote/Blockchain%20image%2070dfde54f9996e5e.png)

- List of records
	- _Blocks_
- Linked using cryptography
- Resistant to modification
	- Not unalterable
	- But secure by design
	- High [Byzantine fault](https://en.wikipedia.org/wiki/Byzantine_fault) tolerance
- Type of payment rail

[![Exported image](../../img/OneNote/Blockchain%20image%208df5e081f4d15c74.png)](https://en.wikipedia.org/wiki/File:Blockchain.svg)

# Block Completion

- Point of transaction

Fork
 
- Chain is formed in parallel over the distributed network
- Based on same rules
- Can sometimes deviate in state
 
- Most forks are short-lived
	- Reaching consensus over the distributed network
- Some permanent
 
- **Accidental**
	- Two or more miners find block at the same time
	- Both have chains where they are next
	- Resolved when one chain gets higher score
		- Another block, longer chain
		- Abandons shorter chain
			- Orphaned block
- **Intentional**
	- Hard Fork
		- Rule change
		- Software validating old blocks will find blocks validated by new software invalid
		- Software update required
	- Soft Fork
		- Old nodes not following a rule that new nodes do
		- Old nodes could accept data that new nodes would find invalid

[Wasabi](https://docs.wasabiwallet.io/using-wasabi/)