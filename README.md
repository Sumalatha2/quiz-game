# quiz-game
questions =[["What is telangana capital ?","warangal","karimnagar","cyberabad","Hyderabad",4],
            ["'Aprajita' Bill was passed by which State Assembly?","Kerala" ,"Odisha","Assam" ,"West Bengal", 4],
            ["Recently, the Ministry of Home Affairs has approved of five new districts in which of the following Union Territory?","NCT of Delhi"," Puducherry","Ladakh","Jammu & Kashmir",3],
            ["India, as a signatory to the United Nations Sustainable Development Goals (UN-SDGs), has pledged to achieve the 'End TB' targets by -","2025"," 2030","2035","2040",1],
            ["India opened a new Consulate General of India in Australia in which city?","Perth","Canberra","Adelaide","Brisbane",4],
            ["Who built the famous Sri Vaikunta-Perumal temple at Kanchipuram?","Aparajita","Nandi Varman-II","Narasimha Varman-I","Danti Varman",2],
            ["The term 'Gond' is derived from the Telugu word 'Kond', which means -","Hill","Warrior","Forest","River",1],
            ["Where was Atal Bihari Vajpayee born?","Bhopal","Indore","Gwalior","Jabalpur",3],]
levels = [1000,2000,3000,5000,10000,20000,40000,80000,160000,320000,640000,1250000,2500000,5000000,10000000]
money = 0
for i in range(0,len(questions)):
  question = questions[i]
  print(f"question for rs: {levels[i]}")
  print(f"question is \n {question[0]}")
  print(f"A.{question[1]}")
  print(f"B.{question[2]}")
  print(f"C.{question[3]}")
  print(f"D.{question[4]}")
  reply = int(input("Enter your answer (1 - 4) or if you want to quit press 0: \n"))
  if(reply == 0):
    money = levels[i - 1]
    break 
  if(reply == question[-1]):
    print(f"Correct answer , you have Won Rs.{levels[i]}")
    if (i == 4):
      money = 10000
    elif (i == 9):
      money = 320000
    elif (i == 14):
      money = 10000000
  else:
    print("Wrong Answer!")
    break 

print(f"you won the money of {money}")
  
