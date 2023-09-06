Remove the Invalid Block
=====================


In this activity, you will learn to remove the highlighted invalid block.


* Open the file `blockchain.py`.
* Define a function to remove the invalid block.


	    def removeInavlidBlocks(self):


* Create a variable to store all the invalid block lists.

	    blockList = []


* Loop through each block in the chain and append the block to `blockList` list if invalid.

        for block in self.chain:
            if block.isValid == False:          
                blockList.append(block)


* Open the file app.py.


* Call the function to remove the invalid block and store it in a variable.
	
        invalidBlocks = chain.removeInavlidBlocks()


* Return the invalid block details.

	    return render_template('index.html', blockData = chain.chain, len= chain.length(), invalidBlocks = invalidBlocks)




* Open the file index.html.
* Add the `<div>` section to display all the block data of invalid blocks from the list as written for the blockData.

        <div>

* Save and run the code to check the output.
