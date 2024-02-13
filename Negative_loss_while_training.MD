# Negative loss while Training

Today i faced a problem,i keep getting negative loss values while training which drove me crazy

negative loss numbers so i searched alot and i found some blog post on internet talks that i think is helpful, based on the specific problem 

so my problem was that while i used `BCEwithlogitloss()` as a loss function it should be given values within range of [0,1] which im case wasn't since im using images not normalized with a range 

sol : after normalizing my images to be within range of [0,1] my loss started with positive values and gradually decreased as a normal loss function
