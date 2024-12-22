import random

number_to_guess = random.randint(1, 100)
attempts = 0
guessed = False
print("Я загадал число от 1 до 100. Попробуй угадать!")

while not guessed:
    user_guess = input("Введите ваше предположение: ")
    
    # Проверка, является ли ввод числом
    if not user_guess.isdigit():
        print("Пожалуйста, введите целое число.")
        continue
    
    user_guess = int(user_guess)
    attempts += 1
    if user_guess < number_to_guess:
        print("Слишком мало 🥶! Попробуйте еще раз.")
    elif user_guess > number_to_guess:
        print("Слишком много 🥵! Попробуйте еще раз.")
    else:
        guessed = True
        print(f"Поздравляю! Вы угадали число  {number_to_guess} за {attempts} попыток.")

if __name__ == "__main__":
    guess_the_number()
