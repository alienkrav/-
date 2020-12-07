def multiply(x, y):
    return(x*y)
print(multiply(4,5))
print(multiply(x=2, y=75))
def multiply_three_args(*args):
    rezult=1
    if (len(args)>1) and (len(args)<=3):
        for num in args:
            rezult*=num
        return rezult
    else:
        return;
print(multiply_three_args())
print(multiply_three_args(3))
print(multiply_three_args(4,5))
print(multiply_three_args(5,6,7))
print(multiply_three_args(4,5,6,7))
def multiply_three_args(*args):
    rezult=1
    if (len(args)>1) and (len(args)<=3):
        for num in args:
            rezult*=num
        return rezult
    else:
        return;
a1=(15, 10, 5)
a2=(3, 1)
a3=[2, 35, 55]
a4=(5, 10, 15, 20)
print(multiply_three_args(a1))
print(multiply_three_args(a2))
print(multiply_three_args(a3))
print(multiply_three_args(a4[0],a4[1],a4[2]))
print(multiply_three_args(a4[1],a4[2],a4[3]))
def multiply_max_num(*args):
    rezult=1
    if len(args) > 1:
      for num in args:
        rezult*=num
      return rezult
    else:
        return;
a1=(15, 10, 5)
a2=(3, 1)
a3=[2, 35, 55]
a4=(5, 10, 15, 20)
print(multiply_max_num(a1))
print(multiply_max_num(a2))
print(multiply_max_num(a3))
print(multiply_max_num(a4[0],a4[1],a4[2]))
print(multiply_max_num(a4[1],a4[2],a4[3]))
print(multiply_max_num(1,2,3,4,5,6,7,8,8))
def plus (x, y):
    return x+y
def minus (x, y): 
    return x-y
def multiply (x, y): 
    return x*y
def mod (x, y): 
    return x%y

operation={
    '+':plus(25,4),
    '-':minus(25,4),
    '*':multiply(25,4),
    '%':mod(25,4)
}
x=input()
print(operation[x])
    


def calc(s):
  pos = 0
  c = s[pos]
  while ((c != '+') and (c !='-') and (c !='*') and (c!='^') and (c!='%') and (c!='/')):
    c = s[pos]
    pos+=1
  word_list = s.split()
  num_list = []
  for word in word_list:
    if word.isnumeric():
      num_list.append(int(word))

  if (c == '+'):
    return num_list[0] + num_list[1]
  if (c == '*'):
    return num_list[0] * num_list[1]
  if (c == '-'):
    return num_list[0] - num_list[1]
  if (c == '/'):
    return num_list[0] / num_list[1]
  if (c == '%'):
    return num_list[0] % num_list[1]
  if (c == '^'):
    return num_list[0] ** num_list[1]
print(calc('35 ^ 20'))

def Car(**kwargs):
  dict = {
      'mark' : 'lada',
      'model' : '112',
      'color' : 'gray',
      'year' : '1999',
      'probeg' : '1000',
      'number' : 'k233lk',
      'price' : '100000'
  }
  for name, value in kwargs.items():
    dict[name] = value
  newname = dict['mark']
  newmodel = dict['model']
  newcolor = dict['color']
  newyear = dict['year']
  newprobeg = dict['probeg']
  newnumber = dict['number']
  newprice = dict['price']
  row = f'Автомобиль марки: {newname}, модели: {newmodel}, цвета: {newcolor}, {newyear} года выпуска, с пробегом: {newprobeg} км, c номерным знаком: {newnumber}, цена: {newprice} руб.'
  return row;
print(Car(mark='lada', color='red', year='1999', probeg='1000000'))
print(Car(mark='bmw', color='black', probeg='10000000', price='1000000'))
def to_str(num):
  x = str(num)
  dict_second = {
      '0' : ' Ноль',
      '1' : ' Один',
      '2' : ' Два',
      '3' : ' Три',
      '4' : ' Четыре',
      '5' : ' Пять',
      '6' : ' Шесть',
      '7' : ' Семь',
      '8' : ' Восемь',
      '9' : ' Девять'
  }
  dict_first = {
      '2' : 'Двадцать',
      '3' : 'Тридцать',
      '4' : 'Сорок',
      '5' : 'Пятьдесят',
      '6' : 'Шестьдесят',
      '7' : 'Семьдесят',
      '8' : 'Восемьдесят',
      '9' : 'Девяносто'
  }
  dict_surprise = {
      '10' : 'Десять',
      '11' : 'Одиннадцать',
      '12' : 'Двенадцать',
      '13' : 'Тринадцать',
      '14' : 'Четырнадцать',
      '15' : 'Пятнадцать',
      '16' : 'Шестнадцать',
      '17' : 'Семнадцать',
      '18' : 'Восемнадцать',
      '19' : 'Девятнадцать'
  }
  if (num < 10):
    return dict_second[x]
  if ((num >= 10) and (num < 20)):
    return dict_surprise[x]
  if ((num >= 20) and (num < 100)):
    if (num % 10 == 0): return dict_first[x[0]]
    else: return dict_first[x[0]] + dict_second[x[1]]
  else:
    return 'error'
print(to_str(40))
def to_int(s):
  dict_num = {
      'ноль' : 0,
      'один' : 1,
      'два' : 2,
      'три' : 3,
      'четыре' : 4,
      'пять' : 5,
      'шесть' : 6,
      'семь' : 7,
      'восемь' : 8,
      'девять' : 9,
      'десять' : 10,
      'одиннадцать' : 11,
      'двенадцать' : 12,
      'тринадцать' : 13,
      'четырнадцать' : 14,
      'пятнадцать' : 15,
      'шестнадцать' : 16,
      'семнадцать' : 17,
      'восемнадцать' : 18,
      'девятнадцать' : 19,
      'двадцать' : 20,
      'тридцать' : 30,
      'сорок' : 40,
      'пятьдесят' : 50,
      'шестьдесят' : 60,
      'семьдесят' : 70,
      'восемьдесят' : 80,
      'девяносто' : 90,
      'сто' : 100,
      'двести' : 200,
      'триста' : 300,
      'четыреста' : 400,
      'пятьсот' : 500,
      'шестьсот' : 600,
      'семьсот' : 700,
      'восемьсот' : 800,
      'девятьсот' : 900,
      'двадцать' : 20,
      'тридцать' : 30,
      'сорок' : 40,
      'пятьдесят' : 50,
      'шестьдесят' : 60,
      'семьдесят' : 70,
      'восемьдесят' : 80,
      'девяносто' : 90,
  }
  num_list = s.split()
  if (len(num_list) == 1): return dict_num[num_list[0]]
  if (len(num_list) == 2): return dict_num[num_list[0]] + dict_num[num_list[1]]
  if (len(num_list) == 3): return dict_num[num_list[0]] + dict_num[num_list[1]] + dict_num[num_list[2]]  
print(to_int('сто одиннадцать'))

dl = [ {'a': 5, 'b': 10, 'z': 10}, {'a': 10, 'b': 20, 'c': 1}, {'a': 3, 'y': 7}]
sorted(dl, key=lambda dict: dict['a'])
