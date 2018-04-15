# pyblight

Works with percentages so the value should be either a fixed percentage or a change.

### Example

* pyblight display set 40%
* pyblight display set +10%
* pyblight display get

or

* pyblight keyboard set 30%
* pyblight keyboard set -10%
* pyblight keyboard get 


### Syntax

pyblight [device] [action] [value]  
[device]  
display  
keyboard  
  
[actions]  
get           - get current value  
set           - set new value  
  
[value]  
+X            - increase backlightning  
-X            - decrease backlightning  
 X            - set fixed value. 0-100  
  
