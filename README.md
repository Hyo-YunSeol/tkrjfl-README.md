'''
#####################################
#       Basic Mission #1
#       신호등 컨트롤러 설계
#####################################


#start
start = input("start 입력하면 시작: ")

if start == "start":
    
    mode = int(input('mode를 선택하세요.\n 1: normal mode \n 2: monitor mode\n'))
    count = 0
    cnum = 0

    if mode == 1:  
        print('normal mode')
        full_cycle = 68
        
    elif mode == 2: 
        print('[monitor mode]\n')
        cnum = int(input('Traffic Monitor_cycle number: '))
        full_cycle = 1
        
    for i in range(full_cycle):
        
        if mode == 1:
            count = count + 1
            
        else:
            count = cnum
        
        cycle = (count - 1) % 68 + 1

        if 1 <= cycle <= 20:
            car ='green' 
            hmn ='red'
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")

        elif 21 <= cycle <= 22:
            car ='yellow' 
            hmn ='red'
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")

        elif 23 <= cycle <= 32:
            car ='left' 
            hmn ='red'
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")

        elif 33 <= cycle <= 34:
            car ='yellow' 
            hmn ='red'
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")

        elif 35 <= cycle <= 48:
            hmn ='green'      
            car ='red' 
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")
        
        elif 49 <= cycle <= 54:
            hmn ='blink'
            car ='red'
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")

        else:
            hmn ='red'
            car ='red' 
            print("Cycle:", count, "일때, 차도:", car, ", 보행자:", hmn,"입니다.")
else:
    print("컨트롤러 동작을 종료합니다.")


'''
