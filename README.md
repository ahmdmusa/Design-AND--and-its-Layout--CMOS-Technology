# Design a logic AND and its LAYOUT CMOS-technology using cadence virtuoso 
AND using CMOS technology and its Layout 
## circuit diagram 
![image](https://user-images.githubusercontent.com/66570093/170685542-194a52c9-6797-4e2b-9003-d18096402bf9.png)

### First we may build inventer and build nand then use the two cells to build our AND


## INVERTER : 

### schematic: 
 ![image](https://user-images.githubusercontent.com/66570093/170685948-44c732ea-d910-40a5-b965-14a902e674c5.png)
### symbol:
![image](https://user-images.githubusercontent.com/66570093/170686019-a4df954a-eccd-4a7f-b119-24da9d3e7a01.png)



### Sizing using cadence and dc sweep tool:


According to tech used (tcmc65n) we find minimum W/L ratio ..


![image](https://user-images.githubusercontent.com/66570093/170686173-404fb29a-fb5e-4c30-94a4-ce1a1c08884d.png)


![image](https://user-images.githubusercontent.com/66570093/170686209-e50d0df1-8a7e-47d4-9376-f34aa87719a2.png)


![image](https://user-images.githubusercontent.com/66570093/170686258-507875c7-e90f-4d8e-8dd1-751745d8c168.png)
 


The main problem is that Bn>Bp that makes the transfer from logic 1 to logic 0 , ( region 3  ) taking more time than expected.
 
 
 
![image](https://user-images.githubusercontent.com/66570093/170686345-8d2f2c0f-9dae-4c30-bdd2-cddd91cda7f8.png)

So, we make W/L for nmos = 120n/60n and Lp=60n and sweep the value of wp in vin-vout ch/s
 We find wp at Vo=Vi=0.5vdd , that makes Bn=Bp



![image](https://user-images.githubusercontent.com/66570093/170686369-d207b2ea-22e2-4688-9532-965b9ccdc0fa.png)


 ### inverter layout:
 ![image](https://user-images.githubusercontent.com/66570093/170686482-13ab8a3d-3a7e-43cc-8dd0-c9d041bbbc79.png)

 
### DRC :
 ![image](https://user-images.githubusercontent.com/66570093/170686540-4c2d71d3-2b42-465c-ba2b-165c9dac63c7.png)
### LVS: 
![image](https://user-images.githubusercontent.com/66570093/170686565-b5584421-cfbb-4571-a5d5-cc24f6164576.png)


## NAND : 

### schematic: 
![image](https://user-images.githubusercontent.com/66570093/170686692-b2e3d4e7-07af-4c94-9905-070851461a59.png)

### symbol:

![image](https://user-images.githubusercontent.com/66570093/170686724-14b8e207-b42f-487a-9844-97b724a23c00.png)


#### NAND layout:
![image](https://user-images.githubusercontent.com/66570093/170686795-8009dacc-f5bf-4ead-afdf-1ee73fea896a.png)
### DRC:
![image](https://user-images.githubusercontent.com/66570093/170686830-d45d3017-0fd8-4178-869a-b96d1d46cd5f.png)
# FULL AND CIRCUIT :
![image](https://user-images.githubusercontent.com/66570093/170687033-59f00aa4-4cc5-4cba-9c55-3d2c7ad819eb.png)

### symbol:
![image](https://user-images.githubusercontent.com/66570093/170687084-1de1e395-7f52-4ec8-bbac-5c6661ff0cc4.png)

### AND LAYOUT 

![image](https://user-images.githubusercontent.com/66570093/170687154-573d90bf-7faa-4107-a0bf-8a377a0b396f.png)


### DRC:
![image](https://user-images.githubusercontent.com/66570093/170687191-7fe5d78a-2071-4744-9249-2d756a22139d.png)


## TEST BUNCH :
Trans simulation: 


![image](https://user-images.githubusercontent.com/66570093/170687306-96765bb3-7bd2-45c6-9aec-80c542ebe67c.png)
Results:

![image](https://user-images.githubusercontent.com/66570093/170687330-5830617b-c6db-460a-a12b-a5dbb00814e6.png)

### Dc response :
![image](https://user-images.githubusercontent.com/66570093/170687448-bab13000-42a8-4014-beae-c42e35040183.png)


### Result:
![image](https://user-images.githubusercontent.com/66570093/170687485-ccde200a-1e10-48fc-916e-7bb571b6b649.png)






### final layout:



![image](https://user-images.githubusercontent.com/66570093/170687551-8e54fc3d-4479-43c0-8c03-aa12636e8ff1.png)



























 
