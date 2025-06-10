tasks=[]
def show():
    print("\nTo-Do List:")
    for i,t in enumerate(tasks,1):
        print(f"{i}. {t}")
def add():
    t=input("Enter task: ")
    tasks.append(t)
def remove():
    i=int(input("Enter task number to remove: "))
    if 0<i<=len(tasks):
        tasks.pop(i-1)
def main():
    while True:
        print("\n1.Add 2.Remove 3.Show 4.Exit")
        c=input("Choose: ")
        if c=="1":
            add()
        elif c=="2":
            remove()
        elif c=="3":
            show()
        elif c=="4":
            break
main()
