# WATERFOOTPRINT
It used to calculate water foot print
def display():
    with open(r"C:\Users\Inbavel\Desktop\water.txt",'r')as f:
        
        l=f.readlines()
        for r in l:
            print(r)
def add():
    n=input("ENTER THING =")
    w=int(input("ENTER FOOTPRINT ="))
    with open(r"C:\Users\Inbavel\Desktop\water.txt",'a')as f:
        a="\n"
        f.write(a)
        f.write(n)
        f.write(" = ")
        f.write(str(w))
        f.close()
        
def calci():
     n=input("ENTER THING =")
     y=int(input("ENTER NO ="))
     with open(r"C:\Users\Inbavel\Desktop\water.txt",'r') as f:
         l=f.readlines()
         for r in l:
             if r.find(n)!=-1:
                 print("FOOT PRINT=",int(r.split()[-1])*y)
         else:
             print("add this item")
             add()
i=100
while (i!=0):
    i=int(input("1-ADD\n2-DISPLAY\n3-CALCI\n0-QUIT\nENTER OPTION="))
    if i==1:
        add()
        
    elif (i==2):
        display()
    elif i==3:
        calci()
    else:
        print("wrong option")
