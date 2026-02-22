# Overview
This is test code for AWS Lambda Layer with Amplify Gen1.<br>
I could do successfully.
## Without using Layer
```mermaid
flowchart TD
    AA[myFunc1<br>hello（）<br>goodbye（）<br>thankyou（）]
    AB[myFunc2<br>hello（）<br>goodbye（）]
```
if you update hello(), you need to update both func1 and func2.

## Using Layer
```mermaid
flowchart TD
    AA[myFunc1]
    AB[myFunc2]
    BA[myLayer1<br>hello（）<br>goodbye（）]
    BB[myLayer2<br>thankyou（）]
    AA --> BA
    AA --> BB
    AB --> BA
```
By introducing a Layer, you only need to update the code in one place.

# Step
```
amplify add function // myFunc1 myFunc2
```
```
amplify add function // myLayer1 myLayer2
```
```
amplify update function // relating function to layer
```
```
amplify push // local -> cloud
```
You will confirm related in Lambda Console.
