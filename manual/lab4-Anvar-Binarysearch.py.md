def answer(list, key):
    if len(list) <= 0:
       return -1
    if len(list) == 1:
       return 0
    if key == list[0]:
       return 1
    length = len(list)
    if key == list[length -1]:
       return length-1
    length = len(list)
    low = 0
    high = length-1
    mid = int(length/2)
    if key <list[mid]:
        for low in range(mid):
           if list[low] == key:
              return low
        return -1
    if key >= list[mid]:
        for mid in range(high):
           if list[mid] == key:
              return mid
        return -1
