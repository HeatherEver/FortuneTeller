# FortuneTeller
One of my first solo projects about a chatbot that tells you your future based on a couple of inputs by the user. I wanted to show my understanding of inputs and using if loops to create something the user can play around with


# A chatbot based game in which a fortune teller gives you a fortune based on your answers
import random

print("Why hello, and welcome to Gypsy Rose\'s Fortune Telling!")
name = input("What is your name? ")
print("I just knew you looked like a " + name + " when you entered!")

fortune = input("Firstly tell me what you would like to know about (money/travel/love/lucky month/lucky numbers)? ")
answer = " "

if fortune == "money":
    random_num = random.randint(1, 5)
    if random_num == 1:
        answer = "you have a large sum of money heading your way."
    elif random_num == 2:
        answer = "it looks like you could be heading for a big promotion ££."
    elif random_num == 3:
        answer = "splash out on that car you've been thinking about."
    elif random_num == 4:
        answer = "wouldn't think about quitting the day job anytime soon."
    elif random_num == 5:
        answer = "don't put that bet on this weekend, big losses are in your future."
    else:
        answer = "error, even crystal balls break sometimes."
    print("My crystal ball says " + answer)

if fortune == "travel":
    random_num = random.randint(1, 5)
    if random_num == 1:
        answer = "you will see all the world's wonders."
    elif random_num == 2:
        answer = "there looks to be sun, sea and sand in your future."
    elif random_num == 3:
        answer = "a big city looks to be in your future."
    elif random_num == 4:
        answer = "maybe a camping trip but it looks like rain."
    elif random_num == 5:
        answer = "looks like you're not even leaving the house, a possible pandemic is on its way."
    else:
        answer = "error, even crystal balls break sometimes."
    print("My crystal ball says " + answer)

if fortune == "love":
    random_num = random.randint(1, 5)
    if random_num == 1:
        answer = "there is wedding bells in your near future."
    elif random_num == 2:
        answer = "you're going to find your perfect match in due course."
    elif random_num == 3:
        answer = "try a dating app, I see a new lover."
    elif random_num == 4:
        answer = "no one new is on your horizon just yet."
    elif random_num == 5:
        answer = "it's not looking good. Maybe focus on your career instead."
    else:
        answer = "error, even crystal balls break sometimes."
    print("My crystal ball says " + answer)

if fortune == "lucky month":
    months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October",
              "November", "December", "every month, very well done", "none, sorry it's just not your year"]
    lucky_month = random.choice(months)
    print("My crystal ball predicts your lucky month is: " + lucky_month + ".")

if fortune == "lucky numbers":
    lucky_numbers = []
    for i in range(0, 5):
        n = random.randint(0, 50)
        lucky_numbers.append(n)
    print("My crystal ball says your lucky numbers are: " + str(lucky_numbers) + ".")
