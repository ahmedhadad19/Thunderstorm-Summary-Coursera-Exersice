# Thunderstorm-Summary-Coursera-Exersice
load('stormData'); 
%stormData.Total_Cost(ismissing(stormData.Total_Cost))=0;
summaryRegionCosts = groupsummary(stormData,"Region",["min","median","mean","max"],"Total_Cost")
stormData =stormData(stormData.Total_Cost > 0,:);
%stormData.stormDataPos =stormData.Total_Cost(stormData.Total_Cost > 0,:);
stormDataPos=stormData(stormData.Total_Cost > 0,:)
summaryRegionPosCosts =groupsummary(stormData,"Region",["min","median","mean","max"],"Total_Cost")


