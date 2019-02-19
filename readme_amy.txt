## Index file modifications

I have created two variables, scenarios and correctResponse (lines 166, 167)

'''
var scenarios = ["HRN_32","HRN_25"];
    
var correctResponse = [2,0];
'''

where correctResponse represents the correct button press position (e.g.,2 would be category_button_HRN


the feedback trial (from line 179) uses a conditional statement; if the position  of the last click is the same as the position 
we specified for correct response (e.g., 2)show image representing last chosen category, and the green tick.
otherwise, show image representing last chosen category, and the RED CROSS.


## index2.html

I have tried creating an accumulating variable, i, to give the code more flexibility.
with every new block, I want the variable i to increase by one, so that in testTrial,
the first block displays scenarios[0] as stimulus, the second block displays scenarios[1], the third scenarios [2],
and so on.
similarly, with each new block, I want a different correct response to be considered
so that the correct button position to press in first block is 2, second block is 0, and so on


it's currently working for testFeedback (i.e., program will give you the green tick if you click
on position no. 2 for first block, position 0 for second block, position 1 for third, and position 3 for fourth,
as specified in var correctResponse.

However it's not working for testTrial, which means that instead of a new scenario being displayed each time
(i.e., scenarios[i+1]), it's staying at scenarios[i] where i=0 for every block.