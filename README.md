This is test code for AWS Lambda Layer with Amplify Gen1.<br>
I could do successfully.
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
