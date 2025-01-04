# part (a)
global QueueHead
global QueueTail
global QueueData

QueueHead = -1
QueueTail = -1
QueueData = [ "" for i in range (20)]

#part (b)
def Enqueue(InData):
    global QueueData
    global QueueHead
    global QueueTail
    if QueueTail == len(QueueData) - 1:
        return False
    elif QueueHead == -1:
        QueueHead = 0
    QueueTail += 1
    QueueData[QueueTail] = InData
    return True


# part (c)
def Dequeue():
    global QueueData
    global QueueHead
    global QueueTail
    if QueueHead < 0 or QueueHead > 20 or QueueHead > QueueTail:
        return "false"
    else:
        return QueueData[QueueHead]
        QueueHead += 1


#part (d)(i)
def StoreItems():

    global QueueData
    global InvalidCount
    global CheckDigitInt
    global CheckDigit
    global Value

    InvalidCount = 0

    for i in range(0,10):
        Value = input("Input a value.")
        CheckDigitInt = int(Value[0]) + int(Value[2]) + int(Value[4])
        CheckDigitInt = CheckDigitInt + (int(Value[1]) * 3)
        CheckDigitInt = CheckDigitInt + (int(Value[3]) * 3)
        CheckDigitInt = CheckDigitInt + (int(Value[5]) * 3)
        CheckDigitInt = CheckDigitInt//10


        if CheckDigitInt == 10:
            CheckDigit = "X"
        else:
            CheckDigit = str(CheckDigitInt)


        if CheckDigit == Value[6]:
            if Enqueue(Value[0:5]):
                print("The value was successfully stored.")
            else:
                print("The queue is already full.")
        else:
            InvalidCount += 1

    print("There were", InvalidCount, "invalid values input.")



#part (d)(ii)

StoreItems()

Result = Dequeue()
if Result == "false":
    print("The queue is empty.")
else:
    print(Result)
