# POST Call/TableNO

property | description
-------- | -----------
tableNO  | This specifies what the command meal order the customer request. in this case the post for the POC will be the burger meal that needs to be documented.

## Description
curl -H "Content-Type: application/json" -X POST -d'{


<!-- post- used to get the command  meal order from the customer.in this case the Post for the POC will be the burger meal that needs to be documented. -->

<!-- Enter a short description. What is it for, and what can it do? -->

Parameters

property | Description
-------- | -----------
orderNum |  this specifies the order number that customers regenerates everday 
timestamp |this is a unique identification. that specifies the time and date the order is recieved 
item1 |  this specifies the number of order in the whole meal 
itemOrdered | this specifies the item ordered , the type"buger meal" and cost 18.00 nis.


<!-- Replace the two example rows and include rows for all your parameters. -->
<!-- If one of the parameters has a set of sub-parameters, create a table or bulleted list for that, but proceed with caution. If the API is complex, there might be an easier way to do your reference section than writing markup by hand. -->


## Examples
this section containes code snippet
### Request

```HTTP

   
curl -H "Content-Type: application/json" -X POST -d'{
   "mealType":"lunch",
   "mealCat":{
  	"main":"burgerMeal",
  	"burger":{
     	"pattyType":"”beef”",
     	"pattyQty":1,
     	"pattyWeightG":300,
     	"pattyCook":"MR",
     	"bunType":"wholeWheat",
     	"condiment1":"ketchup",
     	"condiment2":"secretSauce",
     	"topping1":"lettuce",
     	"topping2":"pickles",
     	"topping3":"None",
     	"topping4":"None"
  	},
  	"sides":{
     	"side1":{
        	"type":"frenchFries",
        	"size":"large"
     	},
     	"side2":{
        	"type":"none",
        	"size":""
     	}
  	},
  	"drink":{
     	"type":"Coke",
     	"size":"large",
     	"ice":"yes"
  	}
   }
}'
http://URL/


 For the purpose of the POC, only the burger meal needs to be documented. The burger JSON object is included in the POST request which is sent to the kitchen. When an OK           response is received, the order is printed in the kitchen so the cook can start cooking. 


<!-- Follow with comments to explain what each part of the request is doing -->

### Response

```HTTP

 200 OK 


```
   When a correct order is placed, the server replies to the app with an acknowledgement. This is not displayed to the user.    
