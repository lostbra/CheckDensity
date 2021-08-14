# CheckDensity
<PW>
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
  
  
  
  
