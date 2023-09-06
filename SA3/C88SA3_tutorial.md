Highlight the Invalid Block
=====================


In this activity, you will learn to display and highlight the invalid block in the blockchain.




<img src= "https://s3-whjr-curriculum-uploads.whjr.online/cd5fddf6-aed3-4658-ba2c-fbc8a502e49e.gif" width = "100%" height = "320">




Follow the given steps to complete this activity:


* Open the file `blockchain.py`.


* Set the `timestamp` parameter as `None` within the `calculateHash()` function.


    `'def calculateHash(self, timestamp = None):`


* Store the current `timestamp` only when `None` is passed as a parameter within the `calculateHash()` function.


`if(timestamp == None):
    timestamp = self.timestamp`


* Modify the previous block timestamp attribute value by passing the current timestamp `time()` within the `calculateHash()` function call.
 
`previousBlockHash = previousBlock.calculateHash(time())`


* Open the file `index.html`.
* Change the styling of the block if `invalid` and represent it by changing the background style of the block.


`<div class="box-back"{% if(block.isValid == False) %} style="background: linear-gradient(45deg, #ff7e7e, #ff0000);" {% endif %} ></div>
								<div class="box-right" {% if(block.isValid == False) %} style="background: linear-gradient(45deg, #ff7e7e, #ff0000);" {% endif %} ></div>
								<div class="box-left" {% if(block.isValid == False) %} style="background: linear-gradient(45deg, #ff7e7e, #ff0000);" {% endif %} ></div>
								<div class="box-top" {% if(block.isValid == False) %} style="background: linear-gradient(45deg, #ff7e7e, #ff0000);" {% endif %} ></div>
								<div class="box-bottom" {% if(block.isValid == False) %} style="background: linear-gradient(45deg, #ff7e7e, #ff0000);" {% endif %} ></div>
`
* Open the file `app.py`.
* Validate the block by calling a function from the chain and store the result in a variable.
	`isValid = chain.validateBlock(newBlock)`


* Store the result into a new block as to whether it is `valid` or not.
	`newBlock.isValid = isValid`


* Save and run the code to check the output.
