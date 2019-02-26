##index 3

Need to create the arrays needed for the 3 phases of the experiment. 

1) I  created the following category arrays:
    var NotCP_scenarios
    var Prob_scenarios
    var HRN_scenarios
    var ROSH_scenarios
    var iROSH_scenarios
    
2) I then shuffled each of these
     var Shuffled_NotCP_Scenarios = jsPsych.randomization.shuffleNoRepeats(NotCP_scenarios);
     var Shuffled_Prob_Scenarios = jsPsych.randomization.shuffleNoRepeats(Prob_scenarios);
     var Shuffled_HRN_Scenarios = jsPsych.randomization.shuffleNoRepeats(HRN_scenarios);
     var Shuffled_ROSH_Scenarios = jsPsych.randomization.shuffleNoRepeats(ROSH_scenarios);
     var Shuffled_iROSH_Scenarios = jsPsych.randomization.shuffleNoRepeats(iROSH_scenarios);
     
 3) Then Create an Array for each phase (perhaps also create CSV files of each of these arrays?). This is the section that I am unsure of how to go about. i think I have the logic, but having issues actually coding it. i.e. 
    
        Pre-test phase: create an array ("PreTest_Array") by selecting objects 0 & 1 from EACH of the shuffled arrays
        
        Training phase: create an array ("Training_Array") by selecting objects 2-5 from EACH of the Shuffled arrays
        
        Post-test phase: creating this one is more complex and involves a few steps. First - we need to make a new array called "PostTest_Trained" by randomly selecting 2 objects per category  from the "Training_Array" . Not sure the best way to do this but it may be useful to use a filter function (e.g. jsObject.filter(obj=>{return obj.correct_response ===2}). Then we need to create an array called "PostTest_New" by creating an array  by selecting objects 7 & 8 from EACH of the Shuffled arrays. The create a combined array called "PostTest_combined" where each of the obects are recorded as either trained or new.
        
