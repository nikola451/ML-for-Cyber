# ML-for-Cyber

***
## How to run my code
all models are under primeModel file
modelX=2.h5, modelX=4.h5, modelX=10.h5 are saved when acc first dropped 2%, 4%, and 10%
modelXX=10.h5 is saved when acc first dropped 20% (it should be named as modelX=20.h5)

## Lab2 report

In Lab 2, 
I first load the data from the cloud file. Then I read the data using data loader. After that, I inspect the structure of model B, and found the index of the cov_3 is 5. After that, I do pruning iteratively and save the model when the accuracy first drops to{2%, 4%, 10%}and I also saved the model for X = 20%, and saved them as “modelX=2.h5”,” modelX=2_Weights.h5, “modelX=4.h5” “modelX=4_Weights.h5” , “”modelX=10.h5” “modelX=10_Weights.h5” ”modelXX=10.h5” “modelXX=10_Weights.h5”.   
After that, I test the performance of the models, which shows that:   

**Clean Classification accuracy for B2_prime: 95.90023382696803  
Attack Success Rate for B2_prime: 100.0**

**Clean Classification accuracy for B4_prime: 92.29150428682775  
Attack Success Rate for B4_prime: 99.98441153546376**

**Clean Classification accuracy for BX_prime: 84.54403741231489  
Attack Success Rate for BX_prime: 77.20966484801247**

**Clean Classification accuracy for BXX_prime: 76.30553390491036  
Attack Success Rate for BXX_prime: 36.26656274356976**

And the CCA and ASR for the original model B is 

**Clean Classification accuracy for B: 98.62042088854248  
Attack Success Rate for B: 100.0**

As we can see, the first B2_prime, B4_prime, and BX_prime  BXX_prime  still perform well for the data. But ASR is still high for B2_prime and B4_prime.

After that, I created goodNet “repaired_net2”, ”repaired_net4”, ”repaired_netX”. And ”repaired_netXX.” I evaluated them, and the data shows:

**Clean Classification accuracy for repaired net 2: 95.74434918160561  
Attack Success Rate for repaired net 2: 100.0  
Clean Classification accuracy for repaired net 4: 92.1278254091972  
Attack Success Rate for repaired net 4: 99.98441153546376  
Clean Classification accuracy for repaired net X: 84.3335931410756  
Attack Success Rate for repaired net X: 77.20966484801247  
Clean Classification accuracy for repaired net XX: 76.16523772408418  
Attack Success Rate for repaired net XX: 36.26656274356976**

As we can see, repaired net XX **(saved when validation accuracy drops at least 20%)** significantly reduces the success rate of attack while ensuring the accuracy of classification.



