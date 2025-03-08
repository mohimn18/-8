import random

def guess_the_number():
    print("مرحبًا بك في لعبة تخمين الرقم!")
    print("لقد اخترت رقمًا بين 1 و 100. حاول تخمينه.")
    
    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("أدخل تخمينك: "))
            attempts += 1

            if guess < secret_number:
                print("الرقم أكبر! حاول مرة أخرى.")
            elif guess > secret_number:
                print("الرقم أصغر! حاول مرة أخرى.")
            else:
                print(f"مبروك! لقد خمنت الرقم الصحيح {secret_number} في {attempts} محاولات.")
                break
        except ValueError:
            print("من فضلك أدخل رقمًا صحيحًا.")

if __name__ == "__main__":
    guess_the_number()
