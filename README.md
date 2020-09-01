# making a dictionary and getting inputs from user and give him its meaning 
# Problem given by Harry from Code with Harry Youtube Channel (HarisAK) 
# Coder - Praveen Singh Chauhan (Technology Video Network - Youtube Channel , GAMP Aaryawarti Films - Film Production & Youtube Channel)
# Link of Youtube - https://www.youtube.com/TechnologyVideoNetwork , https://www.youtube.com/gampaaryawartifilms
# Facebook - https://www.facebook.com/praveen13c
# Twitter - https://twitter.com/praveen13c , https://twitter.com/tvnutube 
# Linkdin -  https://www.linkedin.com/in/impraveenchauhan

d1 = {"abandoned": "something left alone",
      "mutable": "in python we can change value",
      "immutable": "in python we can not change value",
      "concatenate": "when we add two things in python",
      "iterate": "when we use again and again"
      }
word = ""
help_word = ""
cou_num = 1


def p_head1():
    print("*" * 75)
    print(" [ Type A Key Word for its Meaning ]  [ Type 'Exit' to end the program ]")
    print("*" * 75)


def p_head2():
    print('-' * 75)
    print(" [ Type A Key Word for its Meaning ]  [ Type 'Exit' to end the program ]")
    print("-" * 75)


while word != "exit":
    if cou_num < 2:
        p_head1()
    else:
        p_head2()

    word = input("Give a word to 'SEARCH MEANING' of the same in dictionary >   ").lower()

    if word in d1.keys():

        print(f'{word.upper()} meaning =  " {d1[word]} "')
    elif word == "exit":
        break
    else:
        print("-" * 35)
        print(f"it seems you have no key words , You type '{word}' ")
        w_c = len(word)
        print("-" * (45 + w_c))
        print("[ Type 'help' to get right 'Key Words' ]")
        help_word = input("type 'help' to get right key word >  ").lower()
        cou_num += 1

        while help_word == "help":
            print("")
            print(f'here are right word for you {d1.keys()}')
            break
        else:
            print(f"it seems you missed the point ' {help_word} ' is wrong ")
            break
# End of the Program
