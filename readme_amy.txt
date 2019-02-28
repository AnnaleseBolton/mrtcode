##index 3

Amy

2 issues:

 1. In var Training_Feedback I can't get the jsPsych.timlineVariable('expert_reasoning') image to display. The code runs, but for this image it just says "undefined" on the screen.
  
  
 2. On the feedback screen I need to also display the scenario. I attempted this in  var PreTest_Feedback, but also ended up with this image being "undefined".


TODD: 
I have created all the arrays except for the PostTest_Trained_Array array where we randomly select 2 objects per category that were used in the "Training_Array" . Not sure the best way to do this but it may be useful to use a filter function (e.g. jsObject.filter(obj=>{return obj.correct_response ===2}). Then we need to create an array called "PostTest_New" by creating an array  by selecting objects 7 & 8 from EACH of the Shuffled arrays. The create a combined array called "PostTest_combined" where each of the obects are recorded as either trained or new.


 
        
