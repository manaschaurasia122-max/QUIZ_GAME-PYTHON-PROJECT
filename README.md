# QUIZ_GAME-PYTHON-PROJECT
I recently developed a Quiz Game using Python, designed to test users’ knowledge in an interactive and engaging way. This project helped me strengthen my understanding of core programming concepts and logical thinking.


print("Welcome to the quiz game!!")

question_bank=[
    {"text": "In the Indian Premier League in 2015, which bowler won the Purple Cap, awarded to the player with the highest number of wickets taken during the season?", "answer": "A"},
    {"text":"Which colour cap is awarded to the player scoring the most runs in the tournament?", "answer": "D"},
    {"text":"Which team won the inaugural IPL in 2008?", "answer": "C"},
    {"text":"Which colour cap is awarded to the player taking the most wickets in the tournament?", "answer": "B"},
    {"text":"In the Indian Premier League in 2015, which player hit the highest number of sixes in the tournament?", "answer": "A"}
]


options=[["A. Dwayne Smith", "B. Lasith Malinga", "C. Bhuvneshwar Kumar", "D. Imran Tahir"],
         ["A. Red Cap", "B. Green Cap", "C. Blue Cap", "D. Orange Cap"],
         ["A. Chennai Super Kings", "B. Mumbai Indians", "C. Rajasthan Royals", "D. Kolkata Knight Riders"],
         ["A. Red Cap", "B. Purple Cap", "C. Green Cap", "D. Blue Cap"],
         ["A. Chris Gayle", "B. AB de Villiers", "C. Virat Kohli", "D. David Warner"]

]

score=0
def check_answer(user_guess, correct_answer):
    if user_guess == correct_answer:
        return True
    else:
        return False
        
for question_num in range(len(question_bank)):
    print("**********************")
    print(question_bank[question_num]["text"])
    for i in options[question_num]:
        print(i)

   guess=input("Enter your answer (A/B/C/D): ").upper()
    is_correct=check_answer(guess,question_bank[question_num]["answer"])
    if is_correct:
        print("Correct answer!")
        score+=1
    else:
        print("Wrong answer!")
        print(f"The correct answer is {question_bank[question_num]['answer']}")
    print(f"Your current score is {score}/{question_num+1}")
print(f"Your have given {score} correct answers")        
print(f"Your score is {(score/len(question_bank))*100}%")




