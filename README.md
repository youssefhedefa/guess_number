import random
y = int(input('write the minimum number : '))
x = int(input('write the maximum number : '))
def geuss(x):
    random_number = random.randint(y, x)
    geuss = 0
    while geuss != random_number:
        geuss = int(input(f'Geuss a number between {y} and {x} : '))
        if geuss < y:
            print(f"please write number between {y} and {x} ")
        if geuss > x:
            print(f"please write number between {y} and {x} ")
        elif geuss < random_number:
            print("sorry it is too low ")
        elif geuss > random_number:
            print("sorry it is too high ")
    print(f'good one {random_number} is the right number ')
    print('****now computer turn****')
    low = y
    high = x
    feedback = ''
    while feedback != 'c':
        if low != high :
            geuss = random.randint(y, x)
        else:
            geuss = low
        feedback = input(f'if {geuss} is high write (h), low (l), correct (c): ')
        if feedback == 'h':
            high = geuss - 1
        elif feedback == 'l':
            low = geuss +1
    print("computer win")
geuss(x)
