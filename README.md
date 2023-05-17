# simple-neuralNetwork
Our NN will have a simple two-layer architecture. Input layer  𝑎[0]
  will have 784 units corresponding to the 784 pixels in each 28x28 input image. A hidden layer  𝑎[1]
  will have 10 units with ReLU activation, and finally our output layer  𝑎[2]
  will have 10 units corresponding to the ten digit classes with softmax activation.

Forward propagation
                       𝑍[1]=𝑊[1]𝑋+𝑏[1]
                       𝐴[1]=𝑔ReLU(𝑍[1]))
                       𝑍[2]=𝑊[2]𝐴[1]+𝑏[2]
                       𝐴[2]=𝑔softmax(𝑍[2])
 
Backward propagation
                        𝑑𝑍[2]=𝐴[2]−𝑌
                        𝑑𝑊[2]=1𝑚𝑑𝑍[2]𝐴[1]𝑇
                        𝑑𝐵[2]=1𝑚Σ𝑑𝑍[2]
                        𝑑𝑍[1]=𝑊[2]𝑇𝑑𝑍[2].∗𝑔[1]′(𝑧[1])
                        𝑑𝑊[1]=1𝑚𝑑𝑍[1]𝐴[0]𝑇
                        𝑑𝐵[1]=1𝑚Σ𝑑𝑍[1]
 
Parameter updates
                    𝑊[2]:=𝑊[2]−𝛼𝑑𝑊[2] 
                    𝑏[2]:=𝑏[2]−𝛼𝑑𝑏[2]
                    𝑊[1]:=𝑊[1]−𝛼𝑑𝑊[1]
                    𝑏[1]:=𝑏[1]−𝛼𝑑𝑏[1]
