# CheckDensity
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
