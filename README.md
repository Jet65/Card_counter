#! Python 3
# Card_counter
#Counts cards for Blakjak 21

card_werth = {"a":-1,"k":-1,"q":-1,"j":-1,"10":-1,"9":0,"8":0,"7":0,"6":+1,"5":+1,"4":+1,"3":+1,"2":+1,"":0}
totle_count = []
list_cards = []
count = 0

print('Welcom the Card Counting')
print('To star press enter')
input('')

while True:
    #gets the counnt
    #gets the number of players and number of cards
    player_num = int(input("Enter the number of players "))
    card_num = (player_num+1)*5
    
    print('enter a blak when there is no card')
    
    for i in range(card_num):
        #gets as meney cards as needed
        card = input("Enter card ")
        if card in card_werth:
            #gets the counta and ads it to the count list
            count += card_werth[card]
            totle_count.append(count)
    
    #prinrs the totle cunt and recomended act
    print('count = ',totle_count[-1])
    if totle_count[-1] >= 2:
        print('Bet big')
    if totle_count[-1] <= 1:
        print('Bet small')
        
    #sees if the user wonts to quit or continu
    print('To quit enter Q')
    print('To cntinu press enter')
    x = input('Enter Q or press enter: ')
    if x.upper() == 'Q':
        break
    
print('Thanks for useing the card counter')
