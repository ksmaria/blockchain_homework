# PyChain Ledger

![alt=""](Images/application-image.png)

You’re a fintech engineer who’s working at one of the five largest banks in the world. You were recently promoted to act as the lead developer on their decentralized finance team. Your task is to build a blockchain-based ledger system, complete with a user-friendly web interface. This ledger should allow partner banks to conduct financial transactions (that is, to transfer money between senders and receivers) and to verify the integrity of the data in the ledger.

You’ll make the following updates to the provided Python file for this assignment, which already contains the basic `PyChain` ledger structure that you created throughout the module:

1. Create a new data class named `Record`. This class will serve as the blueprint for the financial transaction records that the blocks of the ledger will store.

2. Modify the existing `Block` data class to store `Record` data.

3. Add Relevant User Inputs to the Streamlit interface.

4. Test the PyChain Ledger by Storing Records.

---
## Files

Download the following files to help you get started:

[Module 18 Homework files](Starter_Code/pychain.py)

---

## Instructions

Open the [`pychain.py` file](Starter_Code/pychain.py) included in the Homework's `Starter_code` folder. You’ll use this file to complete the steps for this assignment. Notice that the `PyChain` ledger that you built throughout this unit already includes the functionality to create blocks, perform the proof of work consensus protocol, and validate blocks in the chain.

The steps for this assignment are divided into the following sections:

1. Create a Record Data Class

2. Modify the Existing Block Data Class to Store Record Data

3. Add Relevant User Inputs to the Streamlit Interface

4. Test the PyChain Ledger by Storing Records

### Step 1: Create a Record Data Class

Define a new Python data class named `Record`. Give this new class a formalized data structure that consists of the `sender`, `receiver`, and `amount` attributes. To do so, complete the following steps:

1. Define a new class named `Record`.

2. Add the `@dataclass` decorator immediately before the `Record` class definition.

3. Add an attribute named `sender` of type `str`.

4. Add an attribute named `receiver` of type `str`.

5. Add an attribute named `amount` of type `float`.

Note that you’ll use this new `Record` class as the data type of your `record` attribute in the next section.

### Step 2: Modify the Existing Block Data Class to Store Record Data

Rename the `data` attribute in your `Block` class to `record`, and then set it to use an instance of the new `Record` class that you created in the previous section. To do so, complete the following steps:

1. In the `Block` class, rename the `data` attribute to `record`.

2. Set the data type of the `record` attribute to `Record`.

### Step 3: Add Relevant User Inputs to the Streamlit Interface

Code additional input areas for the user interface of your Streamlit application. Create these input areas to capture the sender, receiver, and amount for each transaction that you’ll store in the `Block` record. To do so, complete the following steps:

1. Delete the `input_data` variable from the Streamlit interface.

2. Add an input area where you can get a value for `sender` from the user.

3. Add an input area where you can get a value for `receiver` from the user.

4. Add an input area where you can get a value for `amount` from the user.

5. As part of the “Add Block” button functionality, update `new_block` so that `Block` consists of an attribute named `record`, which is set equal to a `Record` that contains the `sender`, `receiver`, and `amount` values. The updated `Block` should also include the attributes for `creator_id` and `prev_hash`.

### Step 4: Test the PyChain Ledger by Storing Records

Test your complete `PyChain` ledger and user interface by running your Streamlit application and storing some mined blocks in your `PyChain` ledger. Then test the blockchain validation process by using your `PyChain` ledger. To do so, complete the following steps:

1. In the terminal, navigate to the project folder where you've coded this assignment.

2. In the terminal, run the Streamlit application by using `streamlit run pychain.py`.

3. Enter values for the sender, receiver, and amount, and then click the Add Block button. Do this several times to store several blocks in the ledger.

4. Verify the block contents and hashes in the Streamlit dropdown menu. Take a screenshot of the Streamlit application page, which should detail a blockchain that consists of multiple blocks. Include the screenshot in the `README.md` file for your GitHub repository.

5. Test the blockchain validation process by using the web interface. Take a screenshot of the Streamlit application page, which should indicate the validity of the blockchain. Include the screenshot in the `README.md` file for your homework repository.

---
## Submission

You’ll upload the Python file for this assignment to your GitHub repository.

* Make sure to update the `README.md` file to include an explanation of the Steamlit application, a screenshot or video of your deployed Streamlit application, and any other information that’s needed to interact with your project.

* Submit the link to your GitHub project to Bootcamp Spot.

## Submission Notes:

This application builds a decenterilized ledger system (blockchain-based). It displays a user friendly web interface to enter details (such as sender, receiver and amount to transfer). By using the 'Add Block' button we add the transaction correscponding to the details entered to the blockchain. The integrity of the ledger can be checked at any time using the 'Validate Chain' button.

1. To run this application, clone the code from GitHub link [git@github.com:ksmaria/blockchain_homework.git] and type 'streamlit app pychain.py' in bash once you are in the correct folder ('Starter_Code'). This will open a browser window and display input fields as shown below:
![alt=""](Images/InitialRun_Genesis.jpg)

2. To add a transaction to the ledger; you need to specify a sender, receiver and amount and press 'Add Block' show below.
![alt=""](Images/AddOneBlock.jpg). You can set a diffiulty level to be higher for a transaction that is worth more but defualt in this application is 2. Once you click 'Add Block', the pychain ledger will be updated to contain the transaction you just added.

3. To verify a block's contents and hash you can use the 'Block Inspector' and use the drop-down to got to a particular block(transaction). This is shown on the left panel in above image.

4. Add additional blocks (transactions) to build the ledger.
![alt=""](Images/AddFourthBlock.jpg)

5. You can validate the chain using the 'Validate Chain' which returned True for my run as shown below. This gives us the assurity that integrity of the ledger is intact.
![alt=""](Images/ValidateChain.jpg)

6. Note for self: You can also tally the hash displayed in the table for each transaction with the "Wining Hash" shown in the bash window. Bash window also shows the results of the Validation on the ledger.
![alt=""](Images/BashMessages.jpg)
---

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
