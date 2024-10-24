Components used:  
- Brushed DC hobby motor  
  (the cheapest one!)
- $0.22 \Omega$ and $0.47 \Omega$ resistors  
  For sensing current. Should be small enough to not have a large voltage drop, but larger than noise. Current can go up to 3 A.

### Start up current
The power supply is turned on to give a voltage step. Current limiting feature of the power supply is used.
- Voltage affects the speed of rotation. Current affects the torque hence acceleration.
- Motor starts from rest, accelerates until reaching constant speed. 
- Current increases, reaches a maximum, then decreases.

#### Constant Voltage, Different Maximum Current
$R_{sense} = 0.22 \Omega$  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/6_30V_0_50A.jpg" width="300" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/6_30V_1_00A.jpg" width="300" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/6_30V_2_00A.jpg" width="100" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/6_30V_3_20A.jpg" width="100" >  

$R_{sense} = 0.47 \Omega$  

<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/6_30V_0_50A_0_47Ohm.jpg" width="100" >

#### Constant Maximum Current, Different Voltage
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/2_00A_1_00V.jpg" width="100" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/2_00A_2_00V.jpg" width="100" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/2_00A_4_00V.jpg" width="100" >  
<img src="https://github.com/yuchenglim04/bocchiTheHacker/blob/main/images/brushed_DC_motor/2_00A_6_30V.jpg" width="100" >  



