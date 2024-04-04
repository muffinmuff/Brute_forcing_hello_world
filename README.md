**-Little thing i saw while scrolling Instgram and want it to try**

**-It Should work like this**




https://github.com/muffinmuff/Brute_forcing_hello_world/assets/40132528/8bb2135f-6354-4c1d-879b-7d635cd3b1cf

**-And if you want to loop it infinitely**
**-Use this code**

    from random import randint
    from time import sleep

    target_phrase = 'Hello, World!'
    build_phrase = ''

    def generate_random_character():
    return chr(randint(32, 126))

    while True:
      current_index = 0
      while current_index < len(target_phrase): 
          guess_letter = generate_random_character()   
          print(build_phrase + guess_letter, end='\r')
          if guess_letter == target_phrase[current_index]:
              build_phrase += guess_letter
              current_index += 1    
          sleep(.005)
    
      print("\nTarget sentence found! Starting over again...")
      sleep(1)
      build_phrase = ''
