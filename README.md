https://www.sidefx.com/forum/topic/26762/?page=1#post-336027

# CheckDensity

# Polygon Density
<PW> run over primitive
  
int pc[] = pcfind(0,"P",v@P,ch("maxdist"),chi("maxpt"));
@Cd = float(len(pc))/chi("maxpt"); 
@Cd = fit01(@Cd, 0, 1);

float thresh = chf("threshhold");


if(f@Cd > thresh){

@group_body = 1;

}  
  
int pc[] = pcfind(0,"P",v@P,ch("maxdist"),chi("maxpt"));
  
@Cd = float(len(pc))/chi("maxpt"); 

Group Opt1: 
  
  
int pc[] = pcfind(0,"P",v@P,ch("maxdist"),chi("maxpt"));
  
@Cd = float(len(pc))/chi("maxpt"); 

  
vector thresh = chv("threshhold");

@group_edge = (@Cd <= thresh);
                             
@group_edge = (@Cd > thresh);
  
  
 
Group Opt2: 
int pc[] = pcfind(0,"P",v@P,ch("maxdist"),chi("maxpt"));
  
@Cd = float(len(pc))/chi("maxpt"); 
  

vector thresh = chf("threshhold");
  
if (@Cd < thresh){

@group_edge = 1;
                  

}  
  
                  
Group Opt3:  
  
int pc[] = pcfind(0,"P",v@P,ch("maxdist"),chi("maxpt"));
@Cd = float(len(pc))/chi("maxpt"); 

float thresh = chf("threshhold");
if(f@Cd > thresh){

@group_body = 1;

}

if(f@Cd < thresh){
@group_edge = 1;

}

if(f@Cd = thresh){
@group_exact = 1;

}  
     
# Volume Density
                  
![屏幕截图 2021-09-03 003440](https://user-images.githubusercontent.com/63625631/131882741-a79fe55a-645b-439c-b5ef-95dafd44799f.jpg)
              
![屏幕截图 2021-09-03 003458](https://user-images.githubusercontent.com/63625631/131882748-dfb16445-2291-4b6f-bd6e-63a5f2998618.jpg)
                  
                  
