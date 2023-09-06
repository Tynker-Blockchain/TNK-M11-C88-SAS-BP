Validate the Block on Terminal
======================


In this activity, you will learn to validate the blocks in the blockchain by verifying the hash values for the previous and current blocks.




<img src= "https://s3-whjr-curriculum-uploads.whjr.online/3a577a42-b791-4264-a81d-3ef6bea5560e.gif" width = "100%" height = "320">




Follow the given steps to complete this activity:
1. Validate the Blocks


* Open the file `blockchain.py`.


* Define a function to validate the block added.


        def validateBlock(self, currentBlock):


* Find the previous block from the block chain by reducing the index position by `1`.


        previousBlock = self.chain[currentBlock.index - 1]
   
* Check if the index number of the current block matches that of the next one of the previous block.
 
        if(currentBlock.index != previousBlock.index + 1):
            return False


* Calculate hash for previousBlock and store it in `previousBlockhash`.


        previousBlockHash = previousBlock.calculateHash()
       
* Check whether the previous block hash and current block hash is equal or not and return `true` or `false` accordingly.


        if(previousBlockHash != currentBlock.previousHash):
            return False
        return True


* Validate the new block using the chain.`validateBlock()` method and store it in a variable.


        isValid = chain.validateBlock(newBlock)

* Change the validation attribute, i.e., `isValid` for the newBlock to the returned value.

        newBlock.isValid = isValid

* Save and run the code to check the output.
