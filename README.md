# Animal-identification-game-
import random

animals = {
    "Lion": "King of the Jungle",
    "Elephant": "Largest land animal",
    "Tiger": "Striped big cat",
    "Giraffe": "Tallest animal",
    "Zebra": "Black and white striped animal",
    "Monkey": "Loves bananas",
    "Kangaroo": "Has a pouch",
    "Penguin": "Flightless bird that swims"
}

score = 0
questions = list(animals.items())
random.shuffle(questions)

print("🐾 Welcome to the Animal Identification Game! 🐾")
print("Guess the animal from the clue.\n")

for animal, clue in questions:
    answer = input(f"Clue: {clue}\nYour answer: ").strip()

    if answer.lower() == animal.lower():
        print("✅ Correct!\n")
        score += 1
    else:
        print(f"❌ Wrong! The correct answer is {animal}.\n")

print("=" * 30)
print(f"Game Over! Your Score: {score}/{len(questions)}")

if score == len(questions):
    print("🏆 Excellent! Perfect score!")
elif score >= len(questions) // 2:
    print("👍 Well done!")
else:
    print("😊 Keep practicing and try again!")
