# **STOCK CLOSING PRICE PREDICTOR**

**------------------------------------------------------------------------------------------------------------------------------------**
                **   STEPS INVOLVED **
                ** USING LSTM NETWORKD PREDICTING THE CLOSING PRICE OF A STOCK ON A CERTAIN DATE **
                ** USING PLOTLYDASH TO CREATE A WEB APP **
                **P ARTICIPANTS::BUSSA SAI SANTHOSH,HIMANGSHU DEKA **

**--------------------------------------------------------------------------------------------------------------------------------------**PART-1**::CREATING  MODEL TO PREDICT THE PRICE OF A STOCK ON A PARTICULAR DAY**(DONE BY HIMANGSHU DEKA,BUSSA SAI SANTHOSH)
(LSTM(Long Short Term Memory) IS A Recurrent Neural Network,RNNs are used in Deep Learning Tasks where memory of the past is important as well,However RNNs are bad at long term memory,which is overcome by LSTMs.)

**Basic Working of LSTM:**
The LSTM network architecture consists of three parts, as shown in the image below, and each part performs an individual function.

<img width="629" alt="Screenshot 0005-07-29 at 15 22 53" src="https://github.com/KewangZhili/StockPrizePredictor/assets/111041497/5bf530e3-ea96-4463-9c65-23b056b5425c">

The first part chooses whether the information coming from the previous timestamp is to be remembered or is irrelevant and can be forgotten. In the second part, the cell tries to learn new information from the input to this cell. At last, in the third part, the cell passes the updated information from the current timestamp to the next timestamp. This one cycle of LSTM is considered a single-time step.

These three parts of an LSTM unit are known as gates. They control the flow of information in and out of the memory cell or lstm cell. The first gate is called Forget gate, the second gate is known as the Input gate, and the last one is the Output gate. An LSTM unit that consists of these three gates and a memory cell or lstm cell can be considered as a layer of neurons in traditional feedforward neural network, with each neuron having a hidden layer and a current state.

**2.WE ARE USING THE NSE-TATA DATA SET DOWNLOADED FROM THE INTERNET TO TRAIN OUR MODEL**
  -->From this we have the info regarding the opening,closing,high ,low and the turnover of the stock on a given date.
  
  <img width="900" alt="Screenshot 0005-07-29 at 15 25 38" src="https://github.com/KewangZhili/StockPrizePredictor/assets/111041497/79b98695-9f32-4724-8b83-d130a66a60b3">

**AFTER FURTHER PROCESSING,SCALING,AND CLEANING OUR DATASET WE PREPARE OUR CV,TRAIN AND TEST SETS**

**3.THEN WE BUILD OUR MODEL AS FOLLOWS::**
<img width="875" alt="Screenshot 0005-07-29 at 15 29 40" src="https://github.com/KewangZhili/StockPrizePredictor/assets/111041497/87d6fd2d-e5eb-4cc8-8004-b7ab5e017554">

**NOTE::WE FACED AN ISSUE WITH THE PREDICTED PRICES ON OUR DATES,WHICH SEEMED WAYWARD **BUT AFTER ANALYZING CLOSELY WE FOUND THAT WE HAD FORGOTTEN TO INVERT OUR SCALED DATA,AS THIS WAS AN UNFORGBETTABLE STEP THIS NEEDS MENTIONING HERE** **
<img width="1164" alt="Screenshot 0005-07-29 at 15 30 36" src="https://github.com/KewangZhili/StockPrizePredictor/assets/111041497/447e8c78-1406-4845-9a4a-7c0e5c982dd9">

**4.THEN SAVED THE MODEL AS stock_price_pred.hf**


**------------------------------------------------------------------------------------------------------------------------------------**

**PART-2::DEPLOYED USING PLOTLY DASH**(DONE BY BUSSA SAI SANTHOSH)

    


