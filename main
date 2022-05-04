import random

def stick_with_door_odds():

    # list of wins and losses to be returned
    wins_and_losses = []
    # possible values for 3 doors to chose from
    truths = [True, False, False]
    # randomises doors
    door1 = truths.pop(random.randint(0,2))
    door2 = truths.pop(random.randint(0,1))
    door3 = truths.pop()
    
    # simulate choices
    for i in range(100):
        
        choices = [door1, door2, door3]
        my_door = random.choice(choices)
        # removes choice like gameshow host would
        choices.remove(False)

        if my_door == True:
            wins_and_losses.append('Win')
        else:
            wins_and_losses.append('Loss')
        
    return wins_and_losses.count('Win')


def switch_to_other_door_odds():
    
    # list of wins and losses to be returned
    wins_and_losses = []
    # possible values for 3 doors to chose from
    truths = [True, False, False]
    # randomises doors
    door1 = truths.pop(random.randint(0,2))
    door2 = truths.pop(random.randint(0,1))
    door3 = truths.pop()
    
    # simulates choices
    for i in range(100):
        
        choices = [door1, door2, door3]
        my_door = random.choice(choices)
        
        # removes choice like gameshow host would
        choices.remove(False)
        
        # swaps the remaining doors as per the mathematical advice
        if my_door == choices[0]:
            my_door = choices[1]
        else:
            my_door = choices[0]

        # checks wins
        if my_door == True:
            wins_and_losses.append('Win')
        else:
            wins_and_losses.append('Loss')        
        
    return wins_and_losses.count('Win')



def results_final(stick_or_switch):
    """Runs stick or switch funcs 100 times to get average probability"""
    stick_or_switch_results = []
    for i in range(100):
        stick_or_switch_results.append(stick_or_switch)
    # print(stick_results)
    stick_results_average = sum(stick_or_switch_results) / len(stick_or_switch_results)
    return stick_results_average


sticking_results = []
for i in range(10000):
    sticking_results.append(results_final(stick_with_door_odds()))

switching_results = []
for i in range(10000):
    switching_results.append(results_final(switch_to_other_door_odds()))

print('The results show: Sticking {} vs Switching {}'.format(sum(sticking_results), sum(switching_results)))




