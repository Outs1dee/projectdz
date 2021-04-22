# projectdz
#Зимин Клявин
#5)Список назначенных на стипендию
name = ['Иванов Степан','Смирнова Мария','Кравец Наталья','Семенов Петр','Фоменко Николай','Коровин']
x = [[2,4,4,5],[5,5,2,5],[3,3,3,4],[4,4,4,5],[5,3,4,5],[2,3,4,4]]
w = ['Математика','Русский язык','История','Химия']
y = 0
print('Получают стипендию:')
for i in range(len(name)):
    k = 0
    for j in range(len(x[i])):
        if (x[i][j] == 5) or (x[i][j] == 4):
            k+=1
    if k == 4:
        y+=1
print(y, 'человека')

#6)Список неуспевающих
print('Не успевают по заданной дисциплине:')
for i in range(len(name)):
    k = 0
    for j in range(len(x[i])):
        if x[i][j] == 2:
            k+=1
    if k >= 1:
        print(name[i])

#4)Список назначенных на повышенную стипендию
print('Получают повышенную стипендию: ')
for i in range(len(name)):
    k = 0
    for j in range(len(x[i])):
        if x[i][j] == 5:
            k+=1
    if k == 4:
        print(name[i])

#1)Список группы с оценками
for i in range(len(name)):
    summ = 0
    for j in range(len(x[i])):
        summ += x[i][j]
    print(name[i],':',x[i])

#2)Средний балл каждого студента
for i in range(len(name)):
    summ = 0
    for j in range(len(x[i])):
        summ += x[i][j]
        sred = summ/4
    print(name[i],':','Средняя оценка: ',sred)

#3)Средний балл группы по предмету
for q in range(len(x[i])):
    sr=0
    for u in range(len(x)):
        sr+=x[u][q]
    print(w[q],':',round(sr/6,2))
