import time
def timer(seconds):
    while seconds:
        mins, secs = divmod(seconds, 60) 
        timer_format = '{:02d}:{:02d}'.format(mins, secs) 
        print(timer_format, end='\r') 
        time.sleep(1)  
        seconds -= 1  
try:
    total_seconds = int(input("Введите время в секундах: ")) 
    timer(total_seconds)
except ValueError:
    print("Пожалуйста, введите целое число.")
